---
layout: default
title: Publishing a Transactable SaaS Offer
nav_order: 1
parent: Guides
permalink: /docs/guides/transactable-saas-offer/
---

# Publishing a Transactable SaaS Offer
{: .no_toc }

Go through this guide to understand the different stages of publishing a transactable SaaS offer in the commercial marketplace.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Overview

Publishing a transactable offer in the Azure Marketplace is a multi-step process that involves planning, gathering information, and publishing the offer. The process can be outlined in the following stages:

## Understanding the SaaS offer

The SaaS offer type in Azure Marketplace is meant for software publishers who want to offer their software as a service to customers. In this model, the publisher hosts the software and the customer accesses it over the internet. The customer pays a subscription fee to access the software which implicitly includes the cloud cost and the solution cost. The customer does not have to worry about the infrastructure or the software maintenance. The publisher is responsible for the software updates and the infrastructure maintenance as well as bearing the hosting costs.

### Pricing in Azure Marketplace

Another important aspect that you need to understand is the transactional capabilities availble in Azure Marketplace. **The transactable offers must include at least one plan**. Following is a high-level overview of how you can transact through the Azure Marketplace:

**Pricing model**: The pricing model for SaaS offer can be either a flat rate or per-user basis:
- _Per-user pricing_: When you select this pricing model, you can set the _per user_ price for your plans. The customer will be billed based on the number of users they have subscribed for automatically by the Azure Marketplace.
- _Flat rate pricing_: When you select this pricing model, you can set the _flat rate_ price for your plans. This option is suitable for solutions that do not fit the per-user pricing model. Selecting this model also allows you to make use of the _metered billing_ capabilities. You can add several custom dimensions to your plan to bill the customers on a more granular basis. Custom dimensions also allow you to bill the customers on frequencies other than monthly or yearly.

{: .note }
The SaaS Accelerator provides a reference integration with _Metered Billing APIs_ to facilitate the metered billing capabilities. You can refer to the [SaaS Accelerator on GitHub](https://github.com/Azure/Commercial-Marketplace-SaaS-Accelerator) for more information.

## Gathering information

Before you start creating the offer in Partner Center, you need to gather the following information:

- _Name_: The name of the offer that will be displayed in the Azure Marketplace and/or AppSource.

- _Search results summary_: A one-liner summary of the solution. This is used in the commercial marketplace listing search results.

- _Description_: The description should include a thorough value proposition, key benefits, intended user base, any category or industry associations, in-app purchase opportunities, any required disclosures, and links to learn more about the solution.

- _Getting Started instructions_: This field is required for transactable offers in the Azure Marketplace.

- _Search keywords (optional)_: Provide up to three search keywords that customers can use to find your offer in the online stores.

- _Privacy policy link_: The URL for your company's privacy policy. You must provide a valid privacy policy and are responsible for ensuring your app complies with privacy laws and regulations.

- _Contact information_: You must provide the following contacts from your organization:

  - _Support contact_: Provide the name, phone, and email for when your customers open tickets. You must also include the URL for your support website.
  - _Engineering contact_: Provide the name, phone, and email to use directly when there are problems with your offer. This contact information isn't listed in the commercial marketplace.
  - _CSP Program contact (optional)_: Provide the name, phone, and email if you opt in to the CSP program, so those partners can contact you with any questions. You can also include a URL to your marketing materials.
  - _Useful links (optional)_: You can provide links to various resources for users of your offer. For example, forums, FAQs, and release notes.

- _Supporting documents_: You can provide up to three customer-facing documents, such as whitepapers, brochures, checklists, or PowerPoint presentations.

- _Media_
  - _Logos_: Provide a PNG file for the Large logo. Partner Center uses this file to create a Small and a Medium logo. You can optionally replace these images later.
    - Large (from 216 x 216 to 350 x 350 px, required)
    - Medium (90 x 90 px, optional)
    - Small (48 x 48 px, optional)

  - _Screenshots_: You must add at least one and up to five screenshots with the following requirements, that show how your offer works:
    - 1280 x 720 pixels
    - PNG file type

  - _Videos (optional)_: You can add up to four videos with the following requirements, that demonstrate your offer:
    - Name.
    - URL: Must be hosted on YouTube or Vimeo only.
    - Thumbnail: 1280 x 720 PNG file.

- _Preview audience_: You can add Microsoft Account (MSA) or Microsoft Entra ID email addresses to preview your offer before it goes live. You can add up to 10 email addresses.

- _Plan details_: You must provide at least one plan for your offer. Each plan must include the following details:
  - _Plan name_: The name of the plan.
  - _Description_: A description of the plan.
  - _Markets_: Selection of markets where you want to make the plan available.
  - _Pricing details_: A choice between _Flat rate_ and _Per user_ pricing models. Additionally, you can add custom dimensions for metered billing.

## Publishing the offer

Once you gathered the details, you can proceed with creating the offer in Partner Center. At any point of time, you can click on **Review and publish** button to understand what details are missing or need to be updated.

If all the page on review screen are green, you can click on **Publish** button to submit the offer for validation.

## Offer validation

After submitting the offer, it will go through the automated validation process and will be available in _Preview_ stage. During this stage, only the users added in the _Preview Audience_ list, will be able to see this offer in the Azure Marketplace and/or AppSource and will be able to test the end-to-end flow.

{: .note }
We recommend creating a test offer with test plans to go through the entire process of creation and validation with 0 (zero) cost. Once the validation is completed, you can create the actual offer with the actual pricing.

## Go-live

After the offer has been tested and validated, you can click the _Go Live_ button to make the offer available to all the customers in the Azure Marketplace and/or AppSource.

{: .note }
Offers that include custom billing dimensions will only listed on the Azure Marketplace and not on AppSource.

A live offer will look like as following in the Partner Center > Commercial Marketplace > Overview > Offer name page:

Published SaaS Offer: 
![Published SaaS Offer](/assets/images/PublishedSaaSOffer.png)