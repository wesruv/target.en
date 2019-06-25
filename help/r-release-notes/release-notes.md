---
description: These release notes provide information about features, enhancements, fixes, and known issues for each Target Standard and Target Premium release.
keywords: Release notes;prerelease
seo-description: These release notes provide information about features, enhancements, fixes, and known issues for each Adobe Target Standard and Target Premium release.
seo-title: Target release notes (current)
solution: Target
title: Target release notes (current)
topic: Recommendations
uuid: f6c3e64d-de1e-416c-a56f-2122a58b613e
---

# Target release notes (current){#target-release-notes-current}

These release notes provide information about features, enhancements, and fixes for each Target Standard and Target Premium release.

## Announcements

Be aware of the following important announcements:

* On February 20, 2019, the Adobe Target infrastructure was upgraded in the EMEA, Japan, and APAC regions to no longer collect data from end users with older devices or web browsers that do not support TLS 1.1 or later. This same upgrade is planned for the North America region for **April 1, 2019**. Migrating to TLS 1.2 provides improved security. It is important that you go through the specifics and plan out the changes with your IT team for a smooth transition. For more information, see [TLS (Transport Layer Security) encryption changes](/help/c-implementing-target/c-considerations-before-you-implement-target/tls-transport-layer-security-encryption.md).
* [!DNL Target] and the [!DNL Adobe Marketing Cloud] will drop support for Microsoft Internet Explorer 11 starting in March 2019. This change affects [!DNL Target] authoring only; this change does not affect experience delivery. Please switch to Microsoft Edge or another browser. For more information, see [Supported browsers](/help/c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md).

## Target Standard/Premium 19.6.1 (June 26, 2019)

This release includes the following new features and enhancements:

|Feature / Enhancement|Description|
| --- | --- |
|Visual Experience Composer (VEC)|**New VEC menu options**: When you click a page element in the VEC, a menu shows the options that are available for that element type.<ul><li>You can now use the [!UICONTROL Styles > Background] option to change the background image and color for the selected element. (TGT-15001)</li></ul>See *Styles* in [Visual Experience Options](/help/c-experiences/c-visual-experience-composer/viztarget-options.md#styles).<br>**Click-tracking improvements**: We have improved the process for configuring click tracking within the VEC and the Single Page Application (SPA) VEC.<ul><li>While selecting elements to use in click tracking, the names of all available elements display in the Modifications panel on the right side, making it quick and easy to select the desired elements.</li><li>The [!UICONTROL Goals & Settings] page of the three-part guided activity workflow displays a number representing the number of elements selected for click tracking. You can hover over this number to see the names of all selected elements. (TGT-33878)</li></ul>See [Click tracking](/help/c-activities/r-success-metrics/click-tracking.md).|
|Single Page App Visual Experience Composer (SPA VEC)|**Guided workflow**: A new guided workflow helps you understand how page-delivery-rule settings should be configured to execute and run an activity successfully for your Single Page App. (TGT-33718)<br> See [Single Page App (SPA) Visual Experience Composer](/help/c-experiences/spa-visual-experience-composer.md#page-delivery-settings).<br>**Clone modifications**: You can now define a modification using the SPA VEC and then clone that modification for use in other views in your Single Page App. (TGT-33882)<br>See [Single Page App (SPA) Visual Experience Composer](/help/c-experiences/spa-visual-experience-composer.md).|
|Mobile Visual Experience Composer|**Multiple app versions**: You can now author activities for multiple versions of your mobile app. This saves you time and effort when the versions are similar and you don't need to significantly change the app's UI. (TGT-34231)<br>See "Manage multiple app versions" in [Mobile App Visual Experience Composer](/help/c-target-mobile-app/c-mobile-visual-experience-composer/mobile-visual-experience-composer.md#using-the-mobile-vec).|
|![Premium badge](/help/assets/premium.png) Automated Personalization (AP) & Auto-Target|**Specific experience as control**: You can select an experience to be used as control while creating an AP or Auto-Target activity. This feature lets you route the entire control traffic to a specific experience, based on the traffic allocation percentage configured in the activity. You can then evaluate the performance reports of the personalized traffic against control traffic to that one experience. The current control option (randomly served experiences) will continue to be available. (TGT-32801 & TGT-26572)<br>See [Use a specific experience as control](/help/c-activities/t-automated-personalization/experience-as-control.md).<br>**Personalization Insights reports**: The marketer-friendly naming for attributes when a visitor sees a specific piece of content in a specific location provides more meaningful information. (TGT-33326 & TGT-34957)<br>See [Data collection for the Target personalization algorithms](/help/c-activities/t-automated-personalization/ap-data.md).|
|Google Chrome SameSite cookie policies|Google recently announced that starting with Chrome 76, which is slated for a July 30, 2019 release, developers must explicitly specify which cookies can work across websites and which cookies can track users.<br>As the industry makes strides to create a more secure web for consumers, Target is absolutely committed to delivering personalized experiences while meeting and exceeding the privacy expectations of visitors.<br>See [Google Chrome SameSite cookie policies](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/google-chrome-samesite-cookie-policies.md).|

## at.js version 2.1.0 (June 3, 2019)

We are thrilled to announce the following exciting features in at.js 2.1.0:

|Feature / Enhancement|Description|
| --- | --- |
|Adobe Opt-in support|Adobe Opt-In is a way to simplify Adobe solutions integrations with consent management platforms.<br>For more information about Adobe Opt-in, see [Privacy and General Data Protection Regulation (GDPR)](/help/c-implementing-target/c-considerations-before-you-implement-target/c-privacy/cmp-privacy-and-general-data-protection-regulation.md).|
|Industry-standard CSP compliant|at.js no longer uses eval() to execute JavaScript.|
|Client-side analytics logging|Gives customers full control on how they want to send analytics data to Adobe Analytics, whether on the client-side or server-side.<br>For more information, see [Client-side Analytics logging](/help/c-integrating-target-with-mac/a4t/before-implement.md#client-side) in *Before you implement*.|
|Send notifications|Allows developers to send notifications when an experience is rendered by their code instead of using `applyOffer()` or `applyOffers()`.<br>For more information, see [adobe.target.sendNotifications(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe.target.sendnotifications-atjs-21.md).|
|Reduced file size|The size of at.js is reduced by ~24%. The smaller file size improves page load performance and reduces the time to download at.js on the page.|
|at.js documentation updates|For a full list of all articles updated due to the at.js 2.1.0 release, see the June 3, 2019 entries in [Documentation changes](/help/r-release-notes/doc-change.md).|

## Documentation Changes, Past Release Notes, and Experience Cloud Release Notes {#section_1BC5F5208DA548E9B4344A0836E4B943}

In addition to the notes for each release, the following resources provide additional information:

|Resource|Details|
|--- |--- |
|Documentation changes|View detailed information about updates to this guide that might not be included in these release notes.<br>For more information, see [Documentation Changes](../r-release-notes/doc-change.md#reference_366123CF00994BACBBF9BBDF2C4D840C).|
|Release notes for previous releases|View information about new features and enhancements in previous releases of Target Standard and Target Premium.<br>For more information, see [Release notes for previous releases](../r-release-notes/release-notes-for-previous-releases.md).|
|Adobe Experience Cloud release notes|View the latest release notes for the Adobe Experience Cloud solutions.<br>For more information, see [Experience Cloud Release Notes](https://marketing.adobe.com/resources/help/en_US/whatsnew/).|

## Prerelease Information {#section_5D588F0415A2435B851A4D0113ACA3A0}

The following resources let you see what's coming in the next Target release.

|Resource|Details|
|--- |--- |
|Adobe Priority Product Update list|To receive advance notifications about upcoming product enhancements to Target and other Adobe Experience Cloud solutions, sign up for the Adobe Priority Product Update:<br>[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html)|
|Upcoming release notes|For information about the current month's Target releases, including prerelease information, see the [Target Release Notes - Prerelease](/help/r-release-notes/target-release-notes.md) page.|