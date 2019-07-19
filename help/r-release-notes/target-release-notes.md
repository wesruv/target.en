---
description: These release notes provide information about features, enhancements, and fixes for the latest or upcoming [!DNL Adobe Target] releases.
keywords: release notes
seo-description: These release notes provide information about features, enhancements, and fixes for the latest or upcoming [!DNL Adobe Target] releases.
seo-title: Adobe Target release notes (prerelease)
solution: Target
title: Target release notes (prerelease)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
---

# Target release notes (prerelease){#target-release-notes-prerelease}

These release notes provide information about features, enhancements, and fixes for the latest or upcoming [!DNL Adobe Target] releases.

**Last Updated: July 19, 2019**

>[!NOTE]
>
>These release notes contain prerelease information. Release dates, features, and other information are subject to change without notice. To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages might be the same or it might differ, depending on the timing of releases.
>
>The issue numbers in parentheses are for internal [!DNL Adobe] use.

## Target Standard/Premium 19.7.1 (July 24, 2019) {#tgt-19-7-1}

This release includes the following new features and enhancements:

|Feature / Enhancement|Description|
| --- | --- |
|Mobile App Visual Experience Composer|A new Modifications panel displays in the Mobile App VEC that displays the elements you have set up for click-tracking. (TGT-31741)|
|![Premium badge](/help/assets/premium.png)<br>Recommendations in A/B Test and Experience Targeting (XT) activities|The Recommendations offer (algorithm) status displays on the Overview page for A/B Test and XT activities that contain Recommendations offers. Statuses include: Results Ready, Results Not Ready, and Feed Failure. (TGT-33649)|
|Cross-domain tracking support for at.js 2.0+ via the Experience Cloud ID  (ECID) library|Previously, cross-domain tracking was not supported in at.js 2.*x*. With this release, customers using at.js 2.0 or above can now utilize cross-domain tracking through the ECID library. The ECID library must be installed on the page in conjunction with at.js 2.0 or above in order for cross-domain tracking to work. [Experience Cloud ID library 4.3.0+](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-release-notes.html) must be used.|
|Target support for Apple’s ITP 2.1 and ITP 2.2 via the Experience Cloud ID (ECID) library 4.3|Today, Target customers can mitigate Apple's ITP 2.1 and ITP 2.2 by leveraging Adobe’s CNAME certification program. With this release, Target introduces a seamless integration with the ECID library 4.3, which leverages a server-side cookie to mitigate ITP 2.1 and ITP 2.2. It is highly recommended that Target customers deploy [ECID library 4.3+](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-release-notes.html) in conjunction with Target’s JavaScript library to mitigate any future ITP releases. The ECID library will continue to roll out enhancements that provide a robust solution to the ever-changing cookie policies introduced by browsers.|

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

To receive advance notifications about upcoming product enhancements to Target and other Adobe Experience Cloud solutions, sign up for the Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) 
