---
description: Information about changes to how Adobe and Target use TLS (Transport Layer Security) to maintain the highest security standards and promote the safety of customer data.
keywords: tls;tls 1.0;transport layer security;encryption
seo-description: Information about changes to how Adobe and Target use TLS (Transport Layer Security) to maintain the highest security standards and promote the safety of customer data.
seo-title: TLS (Transport Layer Security) encryption changes
solution: Target
title: TLS (Transport Layer Security) encryption changes
topic: Standard
uuid: d222b966-ee73-4254-87b7-68099583e0dd
---

# TLS (Transport Layer Security) encryption changes{#tls-transport-layer-security-encryption-changes}

Information about changes to how Adobe and Target use TLS (Transport Layer Security) to maintain the highest security standards and promote the safety of customer data.

Transport Layer Security (TLS) is the most-widely deployed security protocol used today for web browsers and other applications that require data to be securely exchanged over a network. [!DNL Adobe] has security compliance standards that require the end-of-life of older protocols and is mandating the use of TLS 1.2 in order to have the most up-to-date and secure version in use. 

>[!NOTE]
>
>On February 20, 2019, the Adobe Target infrastructure was upgraded in the EMEA, Japan, and APAC regions to no longer collect data from end users with older devices or web browsers that do not support TLS 1.1 or later. This same upgrade is planned for the North America region for **April 1, 2019**. Migrating to TLS 1.2 provides improved security. It is important that you go through the specifics and plan out the changes with your IT team for a smooth transition.

We do not expect this to have a significant impact on customer data or reporting.

## Visual Experience Composer (VEC) with Enhanced Experience Composer (EEC) Enabled {#section_B374B62DEC3344C194AC7BECC2EE0AA0}

Until now, Adobe Target's [Enhanced Experience Composer](../../c-experiences/experiences.md#section_34265986611B4AB8A0E4D6ACC25EF91D) (EEC) used TLS 1.0 by default. Starting with the Target 18.4.1 release (April 25, 2018), Target is moving to TLS 1.2 by default.

Adobe will be moving customers in a phased manner to TLS 1.2. For those, whose domains are already 1.2 compliant, we will move them to TLS 1.2 without any changes needed from you. Most customer domains already support TLS 1.2; however, if your domain does not support TLS 1.2, we will keep those domains on TLS 1.0 like today (until February 2019).

You should not face any issue during this migration phase. If the VEC has stopped loading a site that was earlier working, [open a Client Care ticket](../../cmp-resources-and-contact-information.md#reference_ACA3391A00EF467B87930A450050077C) citing this migration as a possible cause.

If, however, you are one of those customers who are on TSL 1.0 without supporting TLS 1.2, then you should plan for movement of your domains/infrastructure to TLS 1.2. We will continue to support the TLS 1.0 protocol until February 2019. Starting in February 2019, Target will not support the TLS 1.0 protocol to be used for the VEC via the Enhanced Experience Composer capability.

Although we strongly recommend everyone to be on TLS 1.2 going forward, if you are a new customer but do *NOT* support TLS 1.2, please reach out to Customer Care informing them that you need to be on TLS 1.0 for the Enhanced Experience Composer. However, please plan to move to TLS 1.2 as you will also not be supported beyond February 2019.

## Activity Delivery {#section_46CA5943E4354B259014C2BF340AECD6}

Starting February 2019, Target servers will no longer support TLS 1.0. With this change, Target servers will no longer accept requests from end users with older devices or web browsers that do not support TLS 1.1 or later. As a result, older devices and browsers that support only TLS 1.0 (or support TLS 1.0 by default) will not receive activity content from Adobe Target. The site's default content will render.

Some of the older devices and browsers that will be affected include:

* Android 4.3 and earlier versions 
* Internet Explorer 8-10 on Windows 7 and earlier versions 
* Internet Explorer 10 on Windows Phone 8.0 
* Safari 6.0.4/OS X10.8.4 and earlier versions

As you plan for this change, consider the following (note that the February 2019 deadline affects all of these items):

* You must ensure that your default site is ready in a manner that is consumable for compliant devices and browsers. 
* Be aware that the number of visitors in your Target reports can potentially see an insignificant drop in the number of visitors. 
* You might need to change audiences created specifically to target older devices or browsers that do not support TLS 1.0—delivery to those devices an browsers will no longer work.

For more details about supported browsers and their versions, see [Supported Browsers](../../c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100).

## Adobe Target APIs {#section_88797FA5434049EC89F908853CC76903}

Starting February 2019, Target APIs will no longer support TLS 1.0 encryption. Customers who access the API should verify that they will not be impacted.

* API clients using Java 7 with default settings will need modifications to support TLS 1.2. For more information, see " [Changing default TLS protocol version for client end points: TLS 1.0 to TLS 1.2](https://www.java.com/en/configure_crypto.html)" on the Java website. 
* API clients using Java 8 should not be impacted because the default setting is TLS 1.2. 
* API clients using other frameworks will need to contact their vendors for details on TLS 1.2 support.

## Access to Experience Cloud Solutions Interfaces {#section_748870ADE77B4CBEB18518DC784E64E5}

Because the Target Standard/Premium interface already requires a [modern web browser](../../c-implementing-target/c-considerations-before-you-implement-target/supported-browsers.md#reference_01B4BF99E7D545A7998773202A2F6100), we do not anticipate issues. If you are unable to connect to Target, you should upgrade your browser to the latest version.

## How to Check Which TLS Version Your Browser Uses {#section_44716DA2CEFF492BABD95AE32B1A3FC6}

To check the TLS version on your website using Firefox (other browsers have similar steps):

1. Open the affected website in Firefox. 
1. Click the **[!UICONTROL Show Site Information]** icon on the browser's address bar.

   ![](assets/firefox_more_info.png)

1. Click **[!UICONTROL Show Connection Details]** > **[!UICONTROL More Information]**.

   ![](assets/firefox_more_info_2.png)

1. Examine the TLS version information under Technical Details:

   ![](assets/firefox_more_info_3.png)

## Expected Behavior with Browsers Supporting TLS 1.0 Only {#section_B5DA97A34EF248EB927610A5DA71EF2F}

This section describes what to expect with browsers that support TLS 1.0 only when using an at.js or mbox.js implementation. For comparison purposes, this section also describes what to expect with browsers that support TLS 1.1 and 1.2.

### Central Endpoints

| Target JavaScript Implementation | Details |
|--- |--- |
|at.js|With TLS 1.0 enabled:<ul><li>Using browser dev tools, on the Network tab, you'll see "200 OK." This means the request has succeeded.</li><li>User sees a "Can't connect securely to this page" message. The message explains that this might be caused because the site uses outdated or unsafe TLS security settings.</li><li>No console errors are displayed.</li></ul>With TLS 1.1 or 1.2 enabled:<ul><li>at.js file is downloaded.</li></ul>|
|mbox.js|With TLS 1.0 enabled:<ul><li>Using browser dev tools, on the Network tab, you'll see "200 OK." This means the request has succeeded.</li><li>User sees a "Can't connect securely to this page" message. The message explains that this might be caused because the site uses outdated or unsafe TLS security settings.</li><li>No console errors are displayed.</li></ul>With TLS 1.1 or 1.2 enabled:<ul><li>mbox.js file is downloaded.</li></ul>|

### Edge Endpoints

| Target JavaScript Implementation | Details |
|--- |--- |
|at.js|With TLS 1.0 enabled:<ul><li>Using browser dev tools, on the Network tab, you'll see "200 OK." This means the request has succeeded.</li><li>User sees a "Can't connect securely to this page" message. The message explains that this might be caused because the site uses outdated or unsafe TLS security settings.</li><li>No console errors are displayed.</li><li>Default content is served.</li></ul>With TLS 1.1 or 1.2 enabled:<ul><li>Offer content is served.</li></ul>|
|mbox.js|With TLS 1.0 enabled:<ul><li>Using browser dev tools, on the Network tab, you'll see "200 OK." This means the request has succeeded.</li><li>User sees a "Can't connect securely to this page" message. The message explains that this might be caused because the site uses outdated or unsafe TLS security settings.</li><li>No console errors are displayed.</li><li>Default content is served.</li></ul>With TLS 1.1 or 1.2 enabled:<ul><li>Offer content is served</li></ul>|

### Activity Targeted with Browser-Version Audience (Internet Explorer, Versions 6, 7, or 8)

>[!NOTE]
>
>Audiences stop working.

| Target JavaScript Implementation | Details |
|--- |--- |
|at.js|at.js is not supported on Internet Explorer versions earlier than version 10.|
|mbox.js|With TLS 1.0 enabled:<ul><li>Default content is served.</li><li>No Target requests are fired.</li><li>No console error is displayed.</li><li>Using browser dev tools, on the Network tab, you'll see "200 OK." This means the request has succeeded.</li></ul>With TLS 1.1 or 1.2 enabled:<ul><li>Offer content is served.</li></ul>|