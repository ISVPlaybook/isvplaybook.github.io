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
The _flat rate pricing_ or the _per user pricing_ is charged autumatically by the Azure Marketplace upon the subscription activation. However, the charges for the custom billing dimensions are charged only when the publishers send usage events using the _Metered Billing APIs_.

### Custom Billing Dimensions 

