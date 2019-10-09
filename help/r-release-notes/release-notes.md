---
description: These release notes provide information about features, enhancements, fixes, and known issues for each Target Standard and Target Premium release.
keywords: Release notes;new features;releases;updates;update;release;enhancement;enhancements;fixes;bug fixes
seo-description: These release notes provide information about features, enhancements, fixes, and known issues for each Adobe Target Standard and Target Premium release.
seo-title: Adobe Target release notes (current) 
solution: Target
title: Target release notes (current)
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
---

# Target release notes (current){#target-release-notes-current}

These release notes provide information about features, enhancements, and fixes for each Target Standard and Target Premium release. In addition, release notes for Target APIs, SDKs, the JavaScript library (at.js), and other platform changes are also included, when applicable.

## Target platform (October 9, 2019)

|Feature / Enhancement|Description|
| --- | --- |
|Node.js SDK version 1.0|The Target Node.js SDK lets you deploy Target server-side.<br>This Node.js SDK helps you easily integrate Target with other Experience Cloud solutions, such as the Adobe Experience Cloud Identity Service, Adobe Analytics, and Adobe Audience Manager.<br>The Node.js SDK introduces best practices and removes complexities when integrating with Adobe Target via our delivery API so that your engineering teams can focus on business logic. The following are notable features that we are introducing in the latest version:<ul><li>Support for prefetching and notifications that allows you to optimize for performance via caching.</li><li>Support for optimizing performance when you have a hybrid integration of Target on both your web pages and server-side. We are introducing a setting called `serverState` that will be populated by experiences retrieved via the server-side so that at.js 2.2 will no longer make an additional server call to retrieve the experiences. This approach optimizes page load performance.</li><li> Support for retrieving VEC-created activities via the Node.js SDK, which is made possible by the new Delivery API.</li><li>Open sourced so your developers can contribute to the Node.js SDK.</li></ul>For more information, see [Release notes - Target Node.js SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md).|
|Delivery API|An entirely new delivery API endpoint (/v1/delivery) will be available in production. Notable features are:<ul><li>One endpoint to retrieve experiences for one or more mboxes.</li><li>Retrieve VEC-created activities via the API.</li><li>Support for an entirely new object called Views that is used for Single Page Applications (SPAs) and Mobile applications.</li></ul>For more information, see [Release notes - Target server-side APIs](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md).|

## Target Standard/Premium 19.9.2 (September 30, 2019)

This maintenance release includes the following enhancement:

* Several security fixes, including a security update to the Rich Text Editor (RTE) in the Visual Experience Composer (VEC). (TGT-35383)
* Recommendations Offers can now be added to elements other than DIV (e.g. P, UL, H1), in addition to DIV, in A/B Test and Experience Targeting activities. (TGT-34333)
* Event notifications (the bell icon in the Target UI) is no longer available. A new look for notifications is coming soon.

## Target Standard/Premium 19.9.1 (September 10, 2019)

|Feature / Enhancement|Description|
| --- | --- |
|![Premium badge](/help/assets/premium.png) Enterprise Permissions|With the Target September 2019 release, Enterprise Permissions provides customers with the following access controls:<UL><li>You can choose the workspaces to which the integration can be applied.</li><li>You can apply a role to the Adobe I/O integration: Approver, Editor, or Observer.</li></ul>For step-by-step instructions and more information, see [Grant Adobe I/O integrations access to workspaces and assign roles](/help/administrating-target/c-user-management/property-channel/configure-adobe-io-integration.md).|

## Additional release notes and version details

|Resource|Details|
|--- |--- |
|[Release notes - Target server-side APIs](/help/c-implementing-target/c-api-and-sdk-overview/releases-server-side.md)|Release notes related to Adobe Target's server-side APIs.|
|[Release notes - Target Node.js SDK](/help/c-implementing-target/c-api-and-sdk-overview/releases-nodejs.md)|Release notes related to Adobe Target's Node.js SDK.|
|[at.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/target-atjs-versions.md)|Details about changes in each version of the Adobe Target at.js JavaScript library.|
|[mbox.js version details](/help/c-implementing-target/c-implementing-target-for-client-side-web/t-mbox-download/mboxjs-change-log.md)|This page shows changes to each version of mbox.js.<br>Note that the mbox.js library is no longer being developed. All customers should migrate from mbox.js to at.js.
|

## Documentation Changes, Past Release Notes, and Experience Cloud Release Notes {#section_1BC5F5208DA548E9B4344A0836E4B943}

In addition to the notes for each release, the following resources provide additional information:

|Resource|Details|
|--- |--- |
|Documentation changes|View detailed information about updates to this guide that might not be included in these release notes.<br>For more information, see [Documentation Changes](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C).|
|Release notes for previous releases|View information about new features and enhancements in previous releases of Target Standard and Target Premium.<br>For more information, see [Release notes for previous releases](../r-release-notes/release-notes-for-previous-releases.md).|
|Adobe Experience Cloud release notes|View the latest release notes for the Adobe Experience Cloud solutions.<br>For more information, see [Experience Cloud Release Notes](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html).|

## Prerelease Information {#section_5D588F0415A2435B851A4D0113ACA3A0}

The following resources let you see what's coming in the next Target release.

|Resource|Details|
|--- |--- |
|Adobe Priority Product Update list|To receive advance notifications about upcoming product enhancements to Target and other Adobe Experience Cloud solutions, sign up for the Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)|
|Upcoming release notes|For information about the current month's Target releases, including prerelease information, see the [Target Release Notes - Prerelease](/help/r-release-notes/target-release-notes.md) page.|
