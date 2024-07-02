---
layout: default
title: Understanding Metered Billing
nav_order: 2
parent: Azure Marketplace
permalink: /docs/marketplace/metered-billing/
---

# Understanding Metered Billing in Azure Marketplace
{: .no_toc }

This article explains the concept of metered billing in Azure Marketplace and how you can leverage it to offer your SaaS solutions to customers.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Overview

This article provide more details about the metered billing capabilities available in the Azure Marketplace. The metered billing is also known as usage-based pricing where the customer is billed based on the usage or the features of the solution. This usage can be measured in terms of the number of API calls, the number of transactions, the number of hours, the amount of data processed, or any other metric that is relevant to the solution and, is integral to the publisher's business model.

{: .note }
To learn more about the SaaS offer type in Azure Marketplace, refer to the [SaaS offer guide](/docs/guides/transactable-saas-offer/).

## Billing models

Azure Marketplace supports two billing models for SaaS offers -  _per-user pricing_ and _flat rate pricing_. When creating a plan in your SaaS offer, you can choose one of these pricing models based on your business model and the customer's requirements.

When you define a pricing based on either of these models, the marketplace automatically bills the customer based on the number of users subscribed to the plan or the billing frequency selected.

### Per-user pricing

In the per-user pricing model, the customer is billed based on the number of users subscribed to the plan. You can set the per-user price for your plans and the customer will be billed based on the number of users they have subscribed for automatically by the Azure Marketplace. This model is suitable for solutions where the usage is directly proportional to the number of users subscribed to the plan.

### Flat rate pricing

In the flat rate pricing model, the customer is billed a fixed amount for the plan irrespective of the usage. You can select this pricing model when the pricing of the solution is not based on the usage or when you want to offer a fixed price for the plan.

The flat rate pricing model also allows you to make use of the _metered billing_ capabilities by adding custom billing dimensions to the plans. These dimensions are essential to bill the customers on a more granular basis and to offer more flexible billing options.

{: .note }
The _flat rate pricing_ or the _per user pricing_ is charged autumatically by the Azure Marketplace upon the subscription activation. However, the charges for the custom billing dimensions are charged only when the publishers send usage events using the [_Metered Billing APIs_](https://learn.microsoft.com/en-us/partner-center/marketplace-offers/marketplace-metering-service-apis).

### Custom Billing Dimensions

B2B ISV partners often require more granular billing options and may not be met with the _flat rate_ or the _per user_ pricing models. The _custom billing dimensions_ in conjunction with _flat rate_, allow you to add additional dimensions to accomodate these requirements.

Custom billing dimensions are additional parameters that can be added to the plan to bill the customers based on the usage of these dimensions. These dimensions also provide flexibility to bill the customer on alternative frequencies, such as quaterly or half-yearly, apart from helping with consumption-based billing plans.

### Anatomy of a custom billing dimension

A custom billing dimension is defined with the following properties:

- _ID_: the ID field is used programmatically and should be small-case, alphanumeric, and unique across all the dimensions.

- _Display Name_: the display name shows up in the published offer and should be short and descriptive, for example "API Calls", "Blue-collar Users" or "Learing Management Module" etc.

- _Unit of Measure_: the description of the billing unit, for example "per 1000 API calls", "per user" or "per year", respectively. Shows up in the published offer.

- _Price per unit in USD_: the price for one unit of the dimension. It can be 0 but cannot be less than 1. Shows up in the published offer.

- _Included quantities in base_: quantity of dimension included in the base price if you have defined a _flat rate_ price **and** if you include any unit quantity in the base price. This should be defined for each billing term defined in the plan. If you have not defined a _flat rate_ price, this field should be 0.

#### Example

Consider a SaaS solution that offers a _flat rate_ pricing of $100 per month and charges $0.01 per API call. The solution also offers a _per user_ pricing of $10 per user per month. The solution can define the following custom billing dimensions:

- _API Calls_: with the unit of measure as "per 1000 API calls" and the price per unit as $10 ($0.0.1 x 1000).

- _Blue-collar Users_: with the unit of measure as "per user" and the price per unit as $10.

You can then define the _Included quantities in base_ for the _API Calls_ dimension as 10000 and for the _Blue-collar Users_ dimension as 0. The implication of this is that the customer will be billed $100 for the _flat rate_ pricing and $10 for each user subscribed to the plan. The customer will also be billed $10 for every 1000 API calls made beyond the included 10000 API calls.

### How to Bill the Custom Dimensions

The _Metered Billing APIs_ are used to send usage events to the Azure Marketplace for the custom billing dimensions. The usage events are used to calculate the charges for the custom billing dimensions and are billed to the customer based on the usage.

In the example above, a customer will be billed $100 per month as the _flat rate_ is defined as such. You, as a publisher, will have to maintain a meter for the _API Calls_ being placed by each customer and send usage events to the Azure Marketplace the number of API calls exceeding 10000 API calls per month. The Azure Marketplace will then calculate the charges for the _API Calls_ dimension based on the usage events sent by you.

A sample API call to send usage events for the _API Calls_ dimension is as follows:

```
{
  "resourceId": <guid>, // unique identifier of the resource against which usage is emitted. 
  "quantity": 7250, // how many units were consumed for the date and hour specified in effectiveStartTime, must be greater than 0 or a double integer, can include decimal points
  "dimension": "api-calls", // custom dimension identifier
  "effectiveStartTime": "2018-12-01T08:30:14", // time in UTC when the usage event occurred, from now and until 24 hours back
  "planId": "plan1", // id of the plan purchased for the offer
}
```

{: .note }
You can either use the [Single Usage event API](https://learn.microsoft.com/en-us/partner-center/marketplace-offers/marketplace-metering-service-apis#metered-billing-single-usage-event) or the [Batch Usage event API](https://learn.microsoft.com/en-us/partner-center/marketplace-offers/marketplace-metering-service-apis#metered-billing-batch-usage-event) to send the usage events to the Azure Marketplace. The Single Usage event API is used to send usage events for a single dimension and a single resource, while the Batch Usage event API is used to send usage events for multiple dimensions and multiple resources as well as multiple customer in a single API call.

A similar call can be placed for the _per user_ dimension since we added that as a custom dimension rather than using the _per user_ pricing model.

{: .note }
If you plan to charge your customers upfront for any of the custom dimension, you can send the usage event such custom dimension immediately after the subscription activation.
