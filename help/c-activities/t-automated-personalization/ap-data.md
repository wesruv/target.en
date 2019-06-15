---
description: Target automatically collects and uses a variety of data to build its personalization algorithms in Automated Personalization (AP) and Auto-Target (AT) activities. When a visitor enters the AP or AT activity, a snapshot of information is passed to a set of "training records" (the visitor data that the personalization algorithms will learn on).
seo-description: Target automatically collects and uses a variety of data to build its personalization algorithms in Automated Personalization (AP) and Auto-Target (AT) activities. When a visitor enters the AP or AT activity, a snapshot of information is passed to a set of "training records" (the visitor data that the personalization algorithms will learn on).
seo-title: Data collection for Target's personalization algorithms
solution: Target
title: Data collection for Target's personalization algorithms
title-outputclass: premium
topic: Premium
uuid: f5ca2d84-0016-4af5-a139-bca567a3d0e8
badge: premium
---

# ![PREMIUM](/help/assets/premium.png) Data collection for the Target personalization algorithms{#data-collection-for-the-target-personalization-algorithms}

Target automatically collects and uses a variety of data to build its personalization algorithms in Automated Personalization (AP) and Auto-Target (AT) activities. When a visitor enters the AP or AT activity, a snapshot of information is passed to a set of "training records" (the visitor data that the personalization algorithms will learn on).

To learn more about the Target personalization algorithms, see [Random Forest Algorithm](../../c-activities/t-automated-personalization/algo-random-forest.md#concept_48F3CDAA16A848D2A84CDCD19DAAE3AA).

The following table shows the data collected by Automated Personalization by default, without the marketer having to do anything, as well as the naming convention used to indicate these attributes in [Personalization Insights Reports](../../c-reports/c-personalization-insights-reports/personalization-insights-reports.md#concept_A897070E1EDC403EB84CFB7A6ECAD767). You can augment the input data set at any time. To learn more about how to upload additional data, see [Uploading Data for the Target Personalization Algorithms](../../c-activities/t-automated-personalization/uploading-data-for-the-target-personalization-algorithms.md#concept_85EA505B37E54514A1C8AB91553FEED6).

| Data Type | Description | Data Type Naming Convention | Example Attributes |
|--- |--- |--- |--- |
|URL Parameters|Target inspects the URL to extract the URL parameters.|`Custom - URL Parameter - [URL Parameter]`|Custom data|
|Referring URL Parameters|In general, the referring URL is the URL that referred to a particular page that initiated the mbox call.<br>Note that this variable can be impacted by the users' activity on your site as well as the technical implementation of your site.|`Custom - [Referring URL Parameter] - [Parameter value]`|Custom data|
|Environmental and Session data|Information about how and when the user is accessing the activity.|`Visitor Profile - [attribute name]`<br>`Browser - [browser attribute]`<br>`Operating System - [OS attribute]`|Visitor Profile - Start of Most Recent Visit<br>Visitor Profile -Total Visits<br>Visitor Profile - Average Time per Visit<br>Browser - Timezone<br>Browser - Day of Week<br>Browser - Language Setting<br>Browser - Type<br>Operating System - Version|
|Geography|Information on where the visitor is located.|`Geo - [geo attribute]`|City<br>Country<br>Region/State<br>Zip Code<br>Latitude<br>Longitude<br>ISP or Mobile Carrier|
|Device and Mobile Data|Device and mobile-specific information.|`Device - [device attribute]`<br>`Mobile - [mobile attribute]`|Mobile Device OS<br>Mobile Screen Size|

The following sections contain detailed information about the various data types, including attribute names, descriptions, and sample values.

Note that some of the values are rounded to the nearest integer or hour.

## Environmental and session data {#env-session}

|Attribute name|Attribute description|Sample values|
| --- | --- | --- |
|Browser - Day of Week|The day of the week when the visitor accessed the activity.|0 to 6.<br>(0 = Sunday)|
|Browser - Hour of Day|The hour of the day when the visitor accessed the activity.|0 to 23<br>(Rounded to the nearest hour)|
|Browser - Hour of Week|The hour of the week when the visitor accessed the activity.|0 to 168<br>(Sunday midnight = 0)|
|Browser - Language Setting|The language specified in the visitor's browser used to access the activity.|<ul><li>English</li><li>German</li></ul>|
|Browser - Screen Height (px)|The device's browser screen height (in pixels) the visitor used to access the activity.|1, 2, 3, etc.|
|Browser - Time of Day|The browser's time of day when the visitor accessed the activity.|0, 6, 12, 18<br>(0 = night, 6 = morning, 12 = afternoon, 18 = evening)|
|Browser - Timezone|The visitor's time zone while accessing the activity.|<ul><li>Pacific Time</li><li>Eastern Time</li><li>GMT</li></ul>|
|Browser - Type|The type of browser the visitor used while accessing the activity.|<ul><li>Chrome</li><li>Firefox</li><li>Internet Explorer 10</li><li>Safari</li><li>Other</li></ul>|
|Browser - Weekday/Weekend|The work status (weekend, work hours, or weekday free time) when the visitor accessed the activity.|<ul><li>Saturday and Sunday = weekend</li><li>Monday through Friday 0900 to 1800 = work time</li><li>Monday through Friday after 1800 until 0900 = weekday free time</li></ul>|
|Browser - Window Height (px)|The browser's window height (in pixels) the visitor used to access the activity.|1, 2, 3, etc.|
|Browser - Window Width (px)|The browser's window width (in pixels) the visitor used to access the activity.|1, 2, 3, etc.|
|Device - Screen Height|The device's screen height the visitor used to access the activity.|1, 2, 3, etc.|
|Device - Screen Width|The device's screen width the visitor used to access the activity.|1, 2, 3, etc.|
|Mobile > Pixel Density (ppi)|The mobile device's pixel density the visitor used to access the activity.|1, 2, 3, etc.|
|Operating System|The operating system the visitor's device used to access the activity.|<ul><li>Mac OS</li><li>Windows 10</li><li>Linux</li><li>Search Bot</li><li>Unknown OS</li></ul>|
|Operating System - Version|The operating system's version the visitor used to access the activity.|<ul><li>Windows 10</li><li>Mac OS 10</li></ul>|
|Traffic Sources - Referring Landing Page URL|The first page the visitor saw when accessing your site.|`https://www.adobe.com/experience-cloud.html`|

## Geo data {#geo}

|Attribute name|Attribute description|Sample values|
| --- | --- | --- |
|Geo - City|The city from which the visitor accessed the activity.|San Francisco|
|Geo - Country|The country from which the visitor accessed the activity.|Germany|
|Geo - DMA|The Designated Marketing Area (DMA) from which the visitor accessed the activity.|Charlottesville|
|Geo - Latitude|The latitude from which the visitor accessed the activity.|47.2699966430664<br>Rounded to 3 decimal places (approximately 100 meters accuracy)|
|Geo - Longitude|The longitude from which the visitor accessed the activity.|-122.269<br>Rounded to 3 decimal places (approximately 100 meters accuracy)|
|Geo - State/Region|The state or region from which the visitor accessed the activity.|<ul><li>Utah</li><li>New South Wales</li></ul>|
|Geo - Zip Code|The Zip Code from which the visitor accessed the activity.|84004|
|Mobile - Carrier|The mobile carrier the visitor used when accessing the activity.|<ul><li>Vodaphone</li><li>T-Mobile</li>|
|Network - Connection Speed|The network connection speed when the visitor accessed the activity.|<ul><li>Broadband</li><li>Cable</li>DSL<li>Mobile</li><li>Wireless</li><li>Satellite</li></ul>|
|Network - Domain Name|The name of the network domain from which the visitor accessed the activity.|`nnt.net`|
|Network - ISP|The network from which the visitor accessed the activity.|nnt communications corporation|

## Mobile data {#mobile}

|Attribute name|Attribute description|Sample values|
| --- | --- | --- |
|Mobile - Device - Brand|The mobile device's brand the visitor used to access the activity.|Apple|
|Mobile - Device - Model Name|The mobile device's model name the visitor used to access the activity.|iPhone XS|
|Mobile - OS - OSX|Specifies whether the user used an OSX device to access the activity.|0 = False, 1 = True|
|Mobile - Screen Height (px)|The mobile device's screen height (in pixels) the visitor used to access the activity.|1, 2, 3, etc.|
|Mobile - Screen Width (px)|The mobile device's screen width (in pixels) the visitor used to access the activity.|1, 2, 3, etc.|
