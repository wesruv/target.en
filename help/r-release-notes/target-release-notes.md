---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes
description: Release notes that provide information about features, enhancements, and fixes for the latest or upcoming DNL Adobe Target releases.
title: Adobe Target prerelease notes
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
---

# Target release notes (prerelease){#target-release-notes-prerelease}

These release notes provide information about features, enhancements, and fixes for the latest or upcoming [!DNL Adobe Target] releases.

**Last Updated: February 18, 2020**

>[!NOTE]
>
>* This article contains prerelease information. Release dates, features, and other information are subject to change without notice. To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages might be the same or it might differ, depending on the timing of releases.
>
>* The issue numbers in parentheses are for internal [!DNL Adobe] use.
>
>* **TLS support changes**: Starting on March 1, 2020, Target will disable support for TLS 1.1 and TLS 1.0 encryption. Transport Layer Security (TLS) is the most-widely deployed security protocol used today for web browsers and other applications that require data to be securely exchanged over a network. This change is needed to meet the generally accepted security compliance standard of TLS 1.2 or higher. Check which TLS version you are currently using. If your version is lower than 1.2, implement the required changes prior to March 1, 2020 in order to continue to use Target as expected.
>
>   For detailed information on the possible impact and the steps you might need to take to update your implementation, see [TLS (Transport Layer Security) encryption changes](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md).
>
>* **mbox.js deprecation**: On August 30, 2020, Adobe Target will no longer support the mbox.js library. Post August 30, 2020, all calls made from mbox.js will fail and impact your pages that have Target activities running. We recommend that all customers migrate to the most recent version of the at.js library before this date to avoid any potential issues with your sites. For more information, see [How At.js Works](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/how-atjs-works.md).
>
>   Although, mbox.js is currently supported, we have not provided feature updates to this library since July 2017. The newer at.js provides many advantages over mbox.js. Among other benefits, at.js improves page load times for web implementations, improves security, and provides better implementation options for single page applications.
>
>   By moving all customers to at.js, our engineers and support staff will be able to provide you with new functionality and offer the support you have come to expect from Adobe.

## Target Standard/Premium 20.2.1 (February 19, 2020)

>[!IMPORTANT]
>
>See the information above about the deprecation of mbox.js.

This release contains the following enhancements and fixes:

* Fixed an issue that prevented customers from selecting a collection when performing a catalog search. (TGT-36230)
* Fixed an issue in which a criteria created via API, but not referenced by an activity created in the Target UI, could be erroneously deleted from the UI. (TGT-35917)
* Implemented security improvements to the Content Security Policy (CSP). (TGT-36190)
* Fixed an issue that caused "NaN%" to display when sliding the Attribute Weighting percentage bar to the far left. (TGT-36211)
* Resolved localization issues so that UI text in various languages displays correctly. 

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to Target and other Adobe Experience Cloud solutions, sign up for the Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) 
