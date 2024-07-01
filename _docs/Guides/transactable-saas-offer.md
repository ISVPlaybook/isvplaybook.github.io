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

1. **Understanding the SaaS offer**: - During this stage, you will need to understand the SaaS offer type and the technical requirements for the offer. You will work with a Microsoft representative to understand the overall process and the requirements to go ahead with publishing a SaaS offer.

2. **Gathering information**: Publishing a SaaS offer involves gathering information about the offer, including the offer details, completing the technical requirements, and creating the offer in Partner Center. 

3. **Publishing the offer**: Once you all the information available, you can procced with creating a _Software as a Service (SaaS)_ offer in Partner Center.

4. **Offer validation**: After submitting the offer, it will go through the automated validation process and will be available in _Preview_ stage. During this stage, only the pre-defined users will be able to see this offer in the Azure Marketplace and/or AppSource and will be able to test the end-to-end flow.

5. **Go-live**: After the validation is satisfactory, you can click the _Go Live_ button to make the offer available to all the customers in the Azure Marketplace and/or AppSource.

## Understanding the SaaS offer

The SaaS offer type in Azure Marketplace is meant for software publishers who want to offer their software as a service to customers. In this model, the publisher hosts the software and the customer accesses it over the internet. The customer pays a subscription fee to access the software which implicitly includes the cloud cost and the solution cost. The customer does not have to worry about the infrastructure or the software maintenance. The publisher is responsible for the software updates and the infrastructure maintenance as well as bearing the hosting costs.

Another important aspect that you need to understand is the transactional capabilities availble in Azure Marketplace. Following is a high-level overview of how you can transact through the Azure Marketplace:

**Pricing model**: The pricing model for SaaS offer can be either a flat rate or per-user basis. While this sounds oversimplified, the pricing model can be more complex and can include multiple pricing tiers, metered billing, or a combination of both.
- Per-user pricing: When you select this pricing model, you can set the _per user_ price for your plans. The customer will be billed based on the number of users they have subscribed for automatically by the Azure Marketplace.
- Flat rate pricing: When you select this pricing model, you can set the _flat rate_ price for your plans. This option is suitable for solutions that do not fit the per-user pricing model. Selecting this model also allows you to make use of the _metered billing_ capabilities. You can add custom dimensions to your plan to bill the customers on a more granular basis. Custom dimensions also allow you to bill the customers on frequencies other than monthly or yearly.

{: .note }
The SaaS Accelerator provides a reference integration with _Metered Billing APIs_ to facilitate the metered billing capabilities. You can refer to the [SaaS Accelerator on GitHub](https://github.com/Azure/Commercial-Marketplace-SaaS-Accelerator) for more information.

## Gathering information

Before you start creating the offer in Partner Center, you need to gather the following information:

- Name: The name of the offer that will be displayed in the Azure Marketplace and/or AppSource.

- Search results summary: A one-liner summary of the solution. This is used in the commercial marketplace listing search results.

- Description: The description should include a thorough value proposition, key benefits, intended user base, any category or industry associations, in-app purchase opportunities, any required disclosures, and links to learn more about the solution. You get a rich text editor controls that allows use of HTML tags to beautify your description. You can enter up to 5,000 characters of text in this box, including HTML markup.

- Getting Started instructions: This field is required for transactable offers in the Azure Marketplace. The instructions are meant to help customers with onboarding. You can add up to 3,000 characters and  links to more detailed online documentation.

- Search keywords (optional): Provide up to three search keywords that customers can use to find your offer in the online stores.

- Privacy policy link: The URL for your company's privacy policy. You must provide a valid privacy policy and are responsible for ensuring your app complies with privacy laws and regulations.

- Contact information: You must provide the following contacts from your organization:

  - Support contact: Provide the name, phone, and email for when your customers open tickets. You must also include the URL for your support website.
  - Engineering contact: Provide the name, phone, and email to use directly when there are problems with your offer. This contact information isn't listed in the commercial marketplace.
 - CSP Program contact (optional): Provide the name, phone, and email if you opt in to the CSP program, so those partners can contact you with any questions. You can also include a URL to your marketing materials.
  - Useful links (optional): You can provide links to various resources for users of your offer. For example, forums, FAQs, and release notes.

- Supporting documents: You can provide up to three customer-facing documents, such as whitepapers, brochures, checklists, or PowerPoint presentations.

- Media – Logos: Provide a PNG file for the Large logo. Partner Center uses this file to create a Small and a Medium logo. You can optionally replace these images later.

  - Large (from 216 x 216 to 350 x 350 px, required)
  - Medium (90 x 90 px, optional)
  - Small (48 x 48 px, optional)

These logos are used in different places in the online stores:
  - The Small logo appears in Azure Marketplace search results and on the AppSource main page and search results page.
  - The Medium logo appears when you create a new resource in Microsoft Azure.
  - The Large logo appears on your offer listing page in Azure Marketplace and AppSource.

- Media - Screenshots: You must add at least one and up to five screenshots with the following requirements, that show how your offer works:
  - 1280 x 720 pixels
  - PNG file type
  - Must include a caption

- Media - Videos (optional): You can add up to four videos with the following requirements, that demonstrate your offer:
  - Name.
  - URL: Must be hosted on YouTube or Vimeo only.
  - Thumbnail: 1280 x 720 PNG file.

- Preview audience: You can add Microsoft Account (MSA) or Microsoft Entra ID email addresses to preview your offer before it goes live. You can add up to 10 email addresses.

## Publishing the offer


## Offer validation


## Go-live

