---
description: Information about supported and not-supported at.js plug-ins.
keywords: at.js plugins;supported plugins;unsupported plugins
seo-description: Information about supported and not-supported at.js plug-ins.
seo-title: at.js Plug-ins
solution: Target
title: at.js Plug-ins
topic: Standard
uuid: ef36b2b2-bf6d-497e-b3f5-2b572a1b8a8d
---

# at.js Plug-ins{#at-js-plug-ins}

Information about supported and not-supported at.js plug-ins.

Many people have built customized plugins and response plug-ins for [!DNL mbox.js]. These custom plug-ins might not be supported by [!DNL at.js] without being updated.

If you are using a plug-in that is not listed here and you would like to know the status, please contact your account representative.

Here is the current status of some of the plug-ins that are used by many customers when used with [!DNL at.js]: 

| Plugin | Details |
|--- |--- |
|mboxTrack|Not supported.<br>This is replaced by the [adobe.target.trackEvent(options)](/help/c-implementing-target/c-implementing-target-for-client-side-web/adobe-target-trackevent.md) function. Update your plug-ins to apply the new function.<br>See the [integrations](/help/c-implementing-target/c-implementing-target-for-client-side-web/c-how-atjs-works/target-atjs-integrations.md) page.|
|Persistent Profile Backup Plugin|Not supported.<br>This plug-in was deprecated when the  Target profile lifetime was extended from two weeks to 90 days. Check the expiration date of your mbox cookie to see the profile lifetime setting on your account.<br>Contact ClientCare if you would like to extended the profile lifetime to 90 days.|
|ttMeta|Supported.<br>This plug-in should continue to work with at.js.|