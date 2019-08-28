---
description: Information about working with Adobe Client Care to implement CNAME (Canonical Name) support in Adobe Target.
keywords: client care;cname;certificate program;canonical name;cookies;certificate;amc;adobe managed certificate
seo-description: Information about working with Adobe Client Care to implement CNAME (Canonical Name) support in Adobe Target.
seo-title: CNAME and Adobe Target
solution: Target
title: CNAME and Adobe Target
topic: Standard
uuid: 3fb0ea31-e91d-4359-a8cc-64c547e6314e
---

# CNAME and Adobe Target{#cname-and-adobe-target}

Information about working with Adobe Client Care to implement CNAME (Canonical Name) support in Adobe Target. To best handle ad blocking issues, a CNAME is used so calls are made to a domain owned by the customer rather than a domain owned by Adobe.

Perform the following steps to request CNAME support in Target:

1. Open a [Customer Care ticket](../../cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) requesting CNAME support for your Adobe Target calls. 
1. Enroll in the [Adobe Managed Certificate (AMC) program](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/adobe_managed_cert_pgm.html) and follow the implementation steps provided in the [!DNL Adobe Analytics] *First-Party Cookies* guide. [!DNL Target] uses the same method that [!DNL Analytics] CNAME support uses.

   The AMC program helps eliminate effort and confusion experienced by customers when implementing first-party cookies. After enrolling to this program, Adobe will purchase and issue the certificate to install on secure servers.

   >[!NOTE]
   >
   >CNAME must be configured before enrolling in the AMC program.

1. After completing the preceding tasks, you must update the `serverDomain` to the new CNAME in at.js.

## Training video: First Party Cookies & Using Adobe Managed Certificates

This video is a recording of [Office Hours](/help/cmp-resources-and-contact-information.md#concept_58EA30379D3B48C4848BA2A8C464A5B7), an initiative led by the Adobe Customer Care team. The Adobe Managed Certificate program discussion starts at 10:21.

[Adobe Analytics: First Party Cookies and Using Adobe Managed Certificates](https://helpx.adobe.com/customer-care-office-hours/analytics/first-party-cookies-adobe-managed-certificates.html)
