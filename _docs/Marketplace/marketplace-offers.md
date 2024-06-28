---
layout: default
title: Azure Marketplace Offer Types
nav_order: 1
parent: Azure Marketplace
permalink: /docs/marketplace/marketplace-offers/
---

# Azure Marketplace Offers
{: .no_toc }

Read on to learn about the Azure Marketplace, Microsoft AppSource and the offer types relvant to ISV partners.

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Overview

Azure Marketplace and Microsoft AppSource are two storefronts meants for different audiences. Azure Marketplace is for IT professionals and developers who are looking for cloud-based solutions. Microsoft AppSource is for business users (such as CxOs) who are looking for cloud-based solutions that can be used with Microsoft 365, Dynamics 365, and Power Platform among others.

These storefronts offer a variety of solutions, including software as a service (SaaS), platform as a service (PaaS), and infrastructure as a service (IaaS) solutions. You may have already been exposed to the Azure Marketplace if you have used the Azure Portal to provision resources.

The B2B solutions are the prime candidates for these storefronts. The solutions can be offered as a free trial, bring your own license (BYOL), or pay as you go (PAYG) models. The solutions can be offered as a single offer or as a solution template that includes multiple offers. However, to qualify for the active Go-To-Market (GTM) benefits, the offer must be transactable through the commercial marketplace. The transactable offers in the marketplace show [Get It Now](){: .btn .btn-blue } button on the offer page.

## Offer types

The following are the offer types that are relevant to ISV partners:

- **SaaS offer**: This is a software as a service (SaaS) offer that is hosted in the cloud. In this model, the publisher hosts the software and the customer accesses it over the internet. The customer pays a subscription fee to access the software which implicitly includes the cloud cost and the solution cost. The customer does not have to worry about the infrastructure or the software maintenance. The publisher is responsible for the software updates and the infrastructure maintenance as well as bearing the hosting costs.

- **Azure Application offer**: This offer type allows the customer to deploy the solution in their own Azure subscription. The customer pays for the Azure consumption costs. The publisher is responsible for the software updates and the solution maintenance. This offer type is suitable for solutions that require more complicated cloud infrastructure orchestration. Azure Application offers can be list as Azure Managed Applications or Solution Templates. The Azure Managed Application provide advanced monitoring and management capabilities to ISV publishers similar the Azure Lighthouse for SI partners while the Solution Templates are ARM templates that can be deployed in the customer's Azure subscription and require BYOL or PAYG licensing outside of marketplace.

- **Azure Virtual Machine offer**: This offer type allows publishers to list solutions that can be deployed as a virtual machine in the customer's Azure subscription. The customer pays for the Azure consumption costs. The publisher is responsible for the software updates and the solution maintenance.

- **Azure Container offer**: This offer type allows publishers to list solutions that can be deployed as a container in the customer's Azure subscription. The customer pays for the Azure consumption costs. The publisher is responsible for the software updates and the solution maintenance. This type differs from the Azure Application offers in that the solution is deployable as a container or container images which can be deployed in Kubernetes clusters, while the solutions that require more complicated cloud infrastructure orchestration are listed as Azure Application offers.

## Technical requirements

# SaaS offer

SaaS offers in the Azure Marketplace are the most common offer type. The technical requirements for a SaaS offer are as follows:

- **Landing page** - The landing page is the account configration page for customers after they purchase the offer. The landing page is a web page that is hosted by the publisher and is used to configure the customer's account. The landing page is a mandatory requirement for SaaS offers. This page should display the information about the purchase and request activation of the offer.

- **Single sign-on (SSO)** - The landing page is required to have multi-tenant single sign-on (SSO) integration with Microsoft Entra ID (formerly Azure Active Directory) for customer authentication.

- **API integration** - The offer should have API integration with the Azure Marketplace for transacting the offer. The API integration is used to manage the offer lifecycle, including the customer's purchase, subscription, and billing. Marketplace fulfillment APIs and the Billing APIs are used to manage the offer lifecycle and billing, respectively.

{: .note }
To learn more about planning, publishing and technica requirements for SaaS offer, see [Plan a SaaS offer for the commercial marketplace](https://learn.microsoft.com/en-us/partner-center/marketplace-offers/plan-saas-offer).

# Azure Application offer

Azure Application offers are suitable for solutions that require more complicated cloud infrastructure orchestration. The technical requirements for an Azure Application offer are as follows:

- **Azure Resource Manager (ARM) template** - The offer should have an ARM template that can be deployed in the customer's Azure subscription. The ARM template is used to deploy the solution in the customer's Azure subscription. The ARM template should be validated and tested before it is published to the marketplace.

- **UI definition** - The UI definition is used to define the user interface for the offer. It allows the pbulishers to request inputs from the customers during the deployment process such as regions, sizes, and configurations.

- **View definition** - THe optional View definitions can be used by the publishers to define the views that are displayed to the customers after the deployment of the Managed Application. It can be used by the customers to monitor and manage the deployed solution as defined by the publisher.

{: .note }
To learn more about planning, publishing and technical requirements for Azure Application offer, see [Plan an Azure Application offer](https://learn.microsoft.com/en-us/partner-center/marketplace-offers/plan-azure-application-offer).

# Azure Container offer

Azure Container offers are suitable for solutions that can be deployed as a container in the customer's Azure subscription. The technical requirements for an Azure Container offer are as follows:

- Your application must be Helm chart-based. If you have multiple charts, you can include other helm charts as subcharts aside from the main helm chart.

- All the image references and digest details must be included in the chart. No other charts or images can be downloaded at runtime.

- You must have created an Azure Container Registry (ACR) that belongs to the active publishing tenant above. The Cloud Native Application Bundle (CNAB) with uploaded to this ACR.

- The application must be deployable to Linux environment.

{. note}
To learn more about how to publish Azure Container offer, see [Plan an Azure Container offer](https://learn.microsoft.com/en-us/partner-center/marketplace-offers/marketplace-containers) and [Prepare Azure container technical assets for a Kubernetes app](https://learn.microsoft.com/en-us/partner-center/marketplace-offers/azure-container-technical-assets-kubernetes?tabs=windows%2Clinux2)

# Azure Virtual Machine offer

Azure Virtual Machine offers are suitable for solutions that can be deployed as a virtual machine in the customer's Azure subscription. The technical requirements for an Azure Virtual Machine offer are as follows:

- **Operating system virtual hard disk (VHD)** - The offer should have one one Operating System VHD and can contain one or more (up to 16, max) data disk VHDs. 

{: .note }
To learn more about the process of creating technical assets for Azure Virtual Machine Image offer, see [Create a virtual machine using an approved base](https://learn.microsoft.com/en-us/partner-center/marketplace-offers/azure-vm-use-approved-base) or [Create a virtual machine using your own image
](https://learn.microsoft.com/en-us/partner-center/marketplace-offers/azure-vm-use-own-image) 