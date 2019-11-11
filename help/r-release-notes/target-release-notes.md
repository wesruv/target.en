---
keywords: release notes;releases;updates;future release;enhancements;new features;fixes
description: Release notes that provide information about features, enhancements, and fixes for the latest or upcoming DNL Adobe Target releases.
title: Adobe Target prerelease notes
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
---

# Target release notes (prerelease){#target-release-notes-prerelease}

These release notes provide information about features, enhancements, and fixes for the latest or upcoming [!DNL Adobe Target] releases.

**Last Updated: October 31, 2019**

>[!NOTE]
>
>These release notes contain prerelease information. Release dates, features, and other information are subject to change without notice. To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages might be the same or it might differ, depending on the timing of releases.
>
>The issue numbers in parentheses are for internal [!DNL Adobe] use.

## Target Java SDK version 1.0.1 (November 11, 2019)

The following issue was fixed in version 1.0.1:

* Send supplemental data ID in a Target request even when there is no Visitor API cookie present.

For more information, see [Release notes - Target Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md).

## Target platform (October 31, 2019)

|Feature / Enhancement|Description|
| --- | --- |
|Java SDK|The [!DNL Target] Java SDK lets you deploy [!DNL Target] server-side. This Java SDK helps you easily integrate [!DNL Target] with other [!DNL Adobe Experience Cloud] solutions, such as the [!DNL Adobe Experience Cloud Identity Service], [!DNL Adobe Analytics], and [!DNL Adobe Audience Manager].<br>The Java SDK introduces best practices and removes complexities when integrating with [!DNL Target] via our delivery API so that your engineering teams can focus on business logic. The following are notable features that we are introducing in the latest version:<ul><li>Support for prefetching and notifications that allows you to optimize for performance via caching.</li><li>Support for optimizing performance when you have a hybrid integration of [!DNL Target] on both your web pages and server-side. We are introducing a setting called `serverState` that is populated by experiences retrieved via the server-side so that at.js 2.2 will no longer make an additional server call to retrieve the experiences. This approach optimizes page load performance.</li><li>Support for retrieving VEC-created activities via the Java SDK, which is made possible by the new Delivery API.</li><li>Open sourced so your developers can contribute to the [Target Java SDK](https://github.com/adobe/target-java-sdk).</li></ul>For more information, see [Release notes - Target Java SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-target-java-sdk.md).<br>Learn more about the Target Java SDK on the Adobe Tech Blog - [Server-Side Optimization with the new Target Java SDK](https://medium.com/adobetech/server-side-optimization-with-the-new-target-java-sdk-421dc418a3f2).|

## Target Standard/Premium 19.10.2 (October 31, 2019)

|Feature / Enhancement|Description|
| --- | --- |
|![Premium badge](/help/assets/premium.png) Work with multi-value attribues|Sometimes you want to work with a multi-value field. Consider the following examples:<ul><li>You offer movies to users. A given movie has multiple actors.</li><li>You sell tickets to concerts. A given user has multiple favorite bands.</li><li>You sell clothing. A shirt is available in multiple sizes.</li></ul>To handle recommendations in these scenarios, you can pass multi-value data to Target Recommendations and use special multi-value operators.|

## Target Standard/Premium 20.1.1

The Target Standard/Premium 20.1.1 release will be in January 2020. Its exact date, features, and enhancements will be announced here.

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63} 

To receive advance notifications about upcoming product enhancements to Target and other Adobe Experience Cloud solutions, sign up for the Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) 
