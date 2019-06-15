---
description: Target automatically collects and uses a variety of data to build its personalization algorithms in Automated Personalization (AP) and Auto-Target (AT) activities. When a visitor enters the AP or AT activity, a snapshot of information is passed to a set of "training records" (the visitor data that the personalization algorithms will learn on).
seo-description: Adobe Target automatically collects and uses a variety of data to build its personalization algorithms in Automated Personalization (AP) and Auto-Target (AT) activities. When a visitor enters the AP or AT activity, a snapshot of information is passed to a set of "training records" (the visitor data that the personalization algorithms will learn on).
seo-title: Data collection for Adobe Target's personalization algorithms
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
| --- | --- | --- | --- |
|URL Parameters|Target inspects the URL to extract the URL parameters.|`Custom - URL Parameter - [URL Parameter]`|Custom data|
|Referring URL Parameters|In general, the referring URL is the URL that referred to a particular page that initiated the mbox call.<br>Note that this variable can be impacted by the users' activity on your site as well as the technical implementation of your site.|`Custom - [Referring URL Parameter] - [Parameter value]`|Custom data|
|Environmental and Session data|Information about how and when the user is accessing the activity.<br>See "Environmental and session data" below.|`Visitor Profile - [attribute name]`<br>`Browser - [browser attribute]`<br>`Operating System - [OS attribute]`|Visitor Profile - Start of Most Recent Visit<br>Visitor Profile -Total Visits<br>Visitor Profile - Average Time per Visit<br>Browser - Timezone<br>Browser - Day of Week<br>Browser - Language Setting<br>Browser - Type<br>Operating System - Version|
|Geographical|Information on where the visitor is located.<br>See "Geographical data" below.|`Geo - [geo attribute]`|City<br>Country<br>Region/State<br>Zip Code<br>Latitude<br>Longitude<br>ISP or Mobile Carrier|
|Device and Mobile Data|Device and mobile-specific information.<br>See "Device and mobile data" below.|`Device - [device attribute]`<br>`Mobile - [mobile attribute]`|Mobile Device OS<br>Mobile Screen Size|

The following sections contain detailed information about the various data types, including attribute names, descriptions, and sample values.

>[!NOTE]
>
>Some of the values in the following tables have been rounded to the nearest integer or hour.

## Environmental and session data {#env-session}

|Attribute name|Attribute description|Sample values|
| --- | --- | --- |
|Browser - Day of Week|The day of the week when the visitor accessed the activity.|0 to 6.<br>(0 = Sunday)|
|Browser - Hour of Day|The hour of the day when the visitor accessed the activity.|0 to 23<br>(0 = midnight)|
|Browser - Hour of Week|The hour of the week when the visitor accessed the activity.|0 to 168<br>(Sunday midnight = 0)|
|Browser - Language Setting|The language specified in the visitor's browser used to access the activity.|English<br>German|
|Browser - Screen Height (px)|The device's browser screen height (in pixels) the visitor used to access the activity.|1, 2, 3, etc.|
|Browser - Time of Day|The browser's time of day when the visitor accessed the activity.|0, 6, 12, 18<br>(0 = night, 6 = morning, 12 = afternoon, 18 = evening)|
|Browser - Timezone|The visitor's time zone while accessing the activity.|Pacific Time<br>Eastern Time<br>GMT|
|Browser - Type|The type of browser the visitor used while accessing the activity.|Chrome<br>Firefox<br>Internet Explorer<br>Safari<br>Other|
|Browser - Weekday/Weekend|The work status when the visitor accessed the activity (weekend, work hours, or weekday free-time).|Saturday and Sunday = weekend<br>Monday through Friday 0900 to 1800 = work time<br>Monday through Friday after 1800 until 0900 = weekday free time|
|Browser - Window Height (px)|The browser's window height (in pixels) the visitor used to access the activity.|1, 2, 3, etc.|
|Browser - Window Width (px)|The browser's window width (in pixels) the visitor used to access the activity.|1, 2, 3, etc.|
|Device - Screen Height|The device's screen height the visitor used to access the activity.|1, 2, 3, etc.|
|Device - Screen Width|The device's screen width the visitor used to access the activity.|1, 2, 3, etc.|
|Mobile > Pixel Density (ppi)|The mobile device's pixel density the visitor used to access the activity.|1, 2, 3, etc.|
|Operating System|The operating system on the visitor's device used to access the activity.|Mac OS<br>Windows<br>Linux<br>Search Bot<br>Unknown OS|
|Operating System - Version|The operating system's version the visitor used to access the activity.|Windows 10<br>Mac OS 10|
|Traffic Sources - Referring Landing Page URL|The first page the visitor saw when accessing your site.|`https://www.adobe.com/ecloud.html`|

## Geographical data {#geo}

|Attribute name|Attribute description|Sample values|
| --- | --- | --- |
|Geo - City|The city from which the visitor accessed the activity.|San Francisco|
|Geo - Country|The country from which the visitor accessed the activity.|Germany|
|Geo - DMA|The Designated Marketing Area (DMA) from which the visitor accessed the activity.|Charlottesville|
|Geo - Latitude|The latitude from which the visitor accessed the activity.|47.269<br>Rounded to 3 decimal places (approximately 100 meters accuracy)|
|Geo - Longitude|The longitude from which the visitor accessed the activity.|-122.269<br>Rounded to 3 decimal places (approximately 100 meters accuracy)|
|Geo - State/Region|The state or region from which the visitor accessed the activity.|Utah<br>New South Wales|
|Geo - Zip Code|The Zip Code from which the visitor accessed the activity.|84004|
|Mobile - Carrier|The mobile carrier the visitor used when accessing the activity.|Vodafone<br>T-Mobile|
|Network - Connection Speed|The network connection speed of the device when the visitor accessed the activity.|Broadband<br>Cable<br>DSL<br>Mobile<br>Wireless<br>Satellite|
|Network - Domain Name|The name of the network domain from which the visitor accessed the activity.|`nnt.net`|
|Network - ISP|The network from which the visitor accessed the activity.|nnt communications corporation|

## Device and Mobile data {#geo}

|Attribute name|Attribute description|Sample values|
| --- | --- | --- |
|Mobile - Device - Brand|The brand of the mobile device the visitor used to access the activity.|Apple|
|Mobile - Device - Model Name|The model name of the mobile device the visitor used to access the activity.|iPhone XS|
|Mobile - OS - OSX|Specifies whether the user used an OSX device to access the activity.|0 is False, 1 is True|
|Mobile - Screen Height (px)|The mobile device's screen height (in pixels) the visitor used to access the activity.|1, 2, 3, etc.|
|Mobile - Screen Width (px)|The mobile device's screen width (in pixels) the visitor used to access the activity.|1, 2, 3, etc.|