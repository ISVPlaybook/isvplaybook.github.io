---
layout: default
title: Installing SaaS Accelerator
nav_order: 2
parent: Guides
permalink: /docs/guides/saas-accelerator/
---

# Installing SaaS Accelerator
{: .no_toc }

This guide provides information on SaaS Accelerator and instructions on how to install it.
{: .fs-5 .fw-300 }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Overview

The SaaS Accelerator is a reference implementation that provides a set of reusable components and best practices for building a SaaS solution that can be transacted through the Azure Marketplace. It encompasses all the technical requirements to publish a transactable SaaS offer in the Azure Marketplace.

If you have already gone through the [Publishing a Transactable SaaS Offer](/docs/guides/transactable-saas-offer/) guide, you may recall that a transactable SaaS offers has certain technical integration requirements. The SaaS Accelerator provides a reference implementation that helps you meet these requirements and quickly publish a transactable SaaS offer in the Azure Marketplace.

{: .note }
To learn more about SaaS Accelerator, refer to the [SaaS Accelerator on GitHub](https://github.com/Azure/Commercial-Marketplace-SaaS-Accelerator).

## Installing SaaS Accelerator

The installation instructions for the SaaS Accelerator are provided in the SaaS Accelerator [documentation here](https://github.com/Azure/Commercial-Marketplace-SaaS-Accelerator/blob/main/docs/Installation-Instructions.md).

This page also documents the steps to update any existing installations of the SaaS Accelerator for cases where new features are added or any issues have been fixed.

## Required Privilges

The SaaS Accelerator installation script creates a number of resources in your Azure subscription. To run the installation script, you need to have the following privileges:

1. **Contributor Role**: You need to have at least, the Azure _Contributor_ role in the Azure subscription where you want to deploy the SaaS Accelerator.
2. **Application Developer**: This Microsoft Entra ID (formerly Azure Active Directory) role is required to create the application registration in the Azure Active Directory.

## Updating Technical Configuration

After the installation, the deployment script outputs the following information:

- _Landing Page URL_
- _Connection Webhook URL_
- _Microsoft Entra Tenant ID_
- _Microsoft Entra Application ID_

You will need to copy this information and paste them in the _Parter Center > Marketplace Offers > Your Offer > Technical Configuration_ section as shown below:

SaaS Offer Technical Configuration:
![SaaS Offer Technical Configuration](/assets/images/saas-accel-tech-config.png)

The offer is now ready to be published in the Azure Marketplace. You review the offer and proceed with the publishing process.

{: .note }
The SaaS Accelerator also provides a publisher admin portal that can be used to manage the customer subscriptions. Please see the SaaS Accelerator video tutorial linked in the _Additional Resources_ sections to learn more.

## Additional Resources
- [Add technical details for a SaaS offer](https://learn.microsoft.com/en-us/partner-center/marketplace-offers/create-new-saas-offer-technical)
- [Mastering the Marketplace - Mastering the SaaS Accelerator](https://microsoft.github.io/Mastering-the-Marketplace/saas-accelerator/)
