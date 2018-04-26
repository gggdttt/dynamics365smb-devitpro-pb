---
title: "Development of a Localization Solution"
description: "Comply with regulatory requirementsin Dynamics 365 Business Central."
author: SusanneWindfeldPedersen
ms.custom: na
ms.date: 04/16/2018
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: "dynamics365-business-central"
ms.author: solsen
ms.assetID: be636361-9de8-4efb-ad50-445e4b7b3255
---

# Development of a Localization Solution
If you want to bring the capabilities of the [!INCLUDE[d365_bus_central_md](../includes/d365_bus_central_md.md)] Core to your local market, then there are several reasons why you would want to choose [!INCLUDE[d365_bus_central_md](../includes/d365_bus_central_md.md)]: 

- Easy to translate and strong base capabilities ready for localization.
- Reach more customers by showcasing your localization apps on Microsoft AppSource.
- [!INCLUDE[d365_bus_central_md](../includes/d365_bus_central_md.md)] provides a proven ERP platform and application for your localization apps which adapts functional areas to the requirements of the local market.  

If you are planning to build localization apps, you should pay attention to the following considerations and requirements:

## Localization apps functionality
Localization apps contain a set of functionalities addressing local requirements that fall within one of the categories below. Make sure to split up your localization apps at minimum according to these categories:  

 * **Regulatory requirements** - local functionality that helps businesses fulfill their legal requirements, such as tax reporting, local GAAP, and other regulatory requirements. 
 * **National standards requirement** – local functionality that address local standards, such as banking and payment formats, address formats, or local interpretations of global standards. 
 * **Market requirements**   - nice-to-have, competitive requirements – local functionality beneficial to the productivity business processes in a country and thereby adding value to business but are not required from a regulatory perspective. 

## Documentation and adoption 
Good and consistent tooltips and documentation will help users adopt your features fast and alleviate most of your support burden. 

An important part of your localization app will be setup data for the production company that will help users get up and running quickly and with minimum effort. 

## Service availability in countries
If you request [!INCLUDE[d365_bus_central_md](../includes/d365_bus_central_md.md)] availability in a country in which Microsoft has not built a localization, you will get access to the international (W1) version of [!INCLUDE[d365_bus_central_md](../includes/d365_bus_central_md.md)]. The availability of this version is by demand, so by requesting access as the first partner in a country there will be a lead time of minimum 3 months for Microsoft to: 

 * Make [!INCLUDE[d365_bus_central_md](../includes/d365_bus_central_md.md)] offers available on the CSP pricelist for the country. 
 * Ensure datacenter operations. 
 * Build platform translation for language(s) for the desired country.

## Submitting your localization app idea to AppSource 
Apart from the regular app details you fill out when [submitting your app idea](https://go.microsoft.com/fwlink/?linkid=869733) there are a few things to emphasize in the app idea submission process for localization apps. Remember to be explicit about: 
 * Country/countries of usage. 
 * Language(s) included in app. 
 * Describe and categorize each local regulatory functionality included in your localization app. 
 * (Optionally) Mark features to be considered part of global version. 

## Product scope for localization apps
Apart from [fulfilling the technical checklist for your app](../devenv-checklist-submission.md), the minimum viable product scope for localization app is: 

 * Local Regulatory Features. 
 * [Tests for Local Regulatory Features](../../compliance/apptest-testingyourextension.md). 
 * [Upgrade code for localization apps](../devenv-upgrading-extensions.md). 
 * Setup data RapidStart package for the localization app. 
 * [Translation of a localization app to local language(s)](../devenv-work-with-translation-files.md) and base app if you are the first partner enabling localization for the country (Learn more about [Dynamics Translation Services](/dynamics365/unified-operations/dev-itpro/lifecycle-services/translation-service-overview)). 
 * Translation of the localization app’s documentation. 
 * National Standard Features (local part) are recommended to be built as additional [add-on apps](readiness-add-on-apps.md) or [connect apps](readiness-connect-apps.md) – separate from the localization app. 
 * Market Required and Local Competitive Features are recommended to be built as additional [add-on apps](readiness-add-on-apps.md) or [connect apps](readiness-connect-apps.md) – separate from the localization app.
 * Using .NET assemblies in your localization app will fail in the technical validation of an app. Instead, contribute to [C/AL Open Library](https://github.com/Microsoft/cal-open-library) GitHub repository with requests you have for .NET. 
 * It is recommended to logically break down the full local functionality set, at a minimum within the above categories. This approach provides optimal flexibility for customers to choose what they really need in terms of local functionality while making sure critical pieces of local functionality do not break upgrade processes nor are upgrade heavy. 
 * The majority of customers in the local market will need most of the local regulatory features. In the category of local regulatory features there will be some features that, even though they are legally required, apply to companies of a certain size, revenue threshold etc. Such situations are opportunities to further logically break down localization apps into smaller focused-functionality sets. 
 * Consider separating localization functionality by the frequency of changes to smaller localization apps. If, for example, your local feature contains one part that is stable and one part that is frequently changed based on regulation changes, make sure to keep the stable part as one app and the changing part a separate localization app. This approach ensures better test coverage, faster response to changes and fewer upgrade issues. 
 * Use worldwide frameworks available in [!INCLUDE[d365_bus_central_md](../includes/d365_bus_central_md.md)] (W1) when building features for, for example, VAT Reports, banking formats, Data Exchange, and others where the majority of functionality is common to all countries but there are some local rules or business formats that are extensions of global frameworks or formats. Make sure to familiarize yourself with such frameworks to reduce effort, reuse code, and properly utilize extensibility points and integration events. If you notice opportunities for improvements in such frameworks or [missing extensibility points](https://github.com/Microsoft/AL/issues), make sure to [contact us](mailto:d365bcloc@microsoft.com) to work together in improving this. 
 * Prepare a setup data RapidStart package for the production company and translate to local language(s). 
 * Consider preparing a local demo data RapidStart package for the evaluation company and translate it to local language(s). 
 * Prepare setup guides (wizards) for areas that are complex to set up to help users enable, discover and have a good first experience using your localization app. 
 * Fork the [Dynamics 365 Business Central documentation from public GitHub repository](https://github.com/MicrosoftDocs/dynamics365smb-docs). Such an approach to documentation can help when other partners or ISVs take dependency on your localization app. 
 * Consider converting field-based documentation to task-based documentation using tooltips and [Dynamics 365 Business Central documentation Github repository](https://github.com/MicrosoftDocs/dynamics365smb-docs). [Rulesets](../devenv-rule-set-syntax-for-code-analysis-tools.md) can help you ensure, for example, that no fields or actions are missing [tooltips](https://worldready.cloudapp.net/Styleguide/Read?id=2748&topicid=38066) (link requires PartnerSource account). 

> [!NOTE]  
> If you have questions for building localization apps please contact the [Microsoft localization team](mailto:d365bcloc@microsoft.com). 

Also, consider joining the [Ready to Go](readiness-ready-to-go.md) program for assistance on bringing you localization apps to AppSource.

## See Also
[Build Your Business on Dynamics 365 Business Central](readiness-welcome.md)  
[Integrate a 3rd Party Solution](readiness-thirdparty-solution.md)  
[Development of a Vertical Solution](readiness-develop-vertical.md)  
[Development of a Horizontal Solution](readiness-develop-horizontal.md)  
[Resell Different Solutions](readiness-reseller.md)  