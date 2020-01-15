---
keywords: mixed content;secure;insecure;chrome;troubleshooting;vec;visual experience composer;unsecure
description: Some browsers block the display of a page if secure content is mixed with insecure content.
title: Enabling mixed content in your browser
topic: Advanced,Standard,Classic
uuid: 6944ce97-ff73-4b61-b006-35862ff83ef1
---

# Enabling mixed content in your browser{#enabling-mixed-content-in-your-browser}

Some browsers block the display of a page if secure content is mixed with insecure content.

If the Visual Experience Composer (VEC) tries to open a page containing mixed (secure and insecure) content, a message displays showing how to disable blocking in your browser so you can open an HTTP site or a site that has mixed calls (HTTPS and HTTP).

![](assets/mixed_content_warning.gif)

Previously, when mixed content was not allowed, you could still perform some actions in Step 1 of the three-step guided workflow when creating activities. Target now blocks actions in Step 1. When this message displays, you must enable mixed content before continuing.

Your browser's security settings might block mixed content or insecure (HTTP) content being loaded into a secure (HTTPS) page or frame (such as the VEC). If you don't want to disable your browser's security settings, you need to have an HTTPS website.

If you website is running on an insecure (HTTP) domain, you are required to allow the VEC to load active mixed content.

>[!NOTE]
>
>Allowing mixed content affects the VEC only and not your live website.

For more information, see [Mixed Content](https://developer.mozilla.org/en-US/docs/Web/Security/Mixed_content) on the *Mozilla Developer Network* (MDN) website.

## Enabling mixed content in Google Chrome {#task_FF297A08F66E47A588C14FD67C037B3A}

If you're visiting a site via a secure connection, Google Chrome will verify that the content on the web page has been transmitted safely. 

See [This page has insecure content](https://support.google.com/chrome/answer/1342714?hl=en) in Google Chrome Help.

### Training video: Enable the VEC in Chrome version 79.0.3945.117 or later (Jan. 2020)

If you are using the VEC with the latest version of Chrome (version 79.0.3945.117 or later), you need to update your site settings. Visitors to your site will not need to complete these steps.

>[!VIDEO](https://www.youtube.com/watch?v=6zGCi5Y8eVo)

The above video outlines the required steps:

1. Click the lock or caution icon, then click Site settings. 

   ![Site Settings](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/site-settings.png)

1. Scroll to Insecure content, then use the drop-down list to change Block (default) to Allow.

   ![Insecure content](/help/c-experiences/c-visual-experience-composer/r-troubleshoot-composer/assets/insecure-content.png)

1. Reload the VEC page.

## Enabling mixed content in Mozilla Firefox {#task_5448763B8DC941FD80F84041AEF0A14D}

By default, Firebox blocks pages that mix secure and insecure content. It is recommended that you permanently change this setting to use [!DNL Target].

1. In Firefox, enter `about:config` in the address bar.
1. Acknowledge the warning message displayed by Firefox.
1. In the search bar, type `block_active`.
1. Double-click ` **[!UICONTROL security.mixed_content.block_active_content]**` .

   The value changes from "True" to "False." When the value shows "False," you are finished.  It is recommended that you restart your computer after changing this setting. 

## Enabling mixed content in Microsoft Internet Explorer {#task_59E7D13C04DF486C92CD78D0C63DDDE8}

By default, Internet Explorer blocks pages that mix secure and insecure content. It is recommended that you permanently change this setting to use Target. 

1. In Internet Explorer, click the settings icon > **[!UICONTROL Internet Options]**.
1. Open the [!UICONTROL Security] tab.
1. Select **[!UICONTROL Internet]**, then click **[!UICONTROL Custom Level]**.
1. Select **[!UICONTROL Miscellaneous]**.
1. Under [!UICONTROL Miscellaneous], enable **[!UICONTROL Display Mixed Content]**.
1. Click **[!UICONTROL OK]** > **[!UICONTROL Yes]** > **[!UICONTROL Apply]**.

We recommended that you restart your computer after changing this setting.

