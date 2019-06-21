---
description: Information about Target and the SameSite IETF standard used starting with Google Chrome version 76.
keywords: google;samesite
seo-description: Information about Adobe Target and the SameSite IETF standard introduced with Google Chrome version 76.
seo-title: Adobe Target and SameSite cookie policies
solution: Target
subtopic: Getting Started
title: Google Chrome SameSite cookie policies
topic: Standard
uuid: aaeda1e6-7b2c-4a00-b65d-bfc95ea796b5
---

# Google Chrome SameSite cookie policies

Google recently announced that starting with Chrome 76, which is slated for a July 30, 2019 release, developers must explicitly specify which cookies can work across websites and which cookies can track users. 

## SameSite overview

To provide safeguards around when cookies can be sent across sites so that users are protected, Google adds support for an IETF standard called "SameSite" in Google Chrome 76 (and later), which requires web developers to manage cookies with the SameSite attribute component in the `Set-Cookie` header.

There are three different values that can be passed into the SameSite attribute: Strict, Lax, or None.

|Value|Description|
| --- | --- |
|Strict|Cookies with this setting can be accessed only when visiting the domain on which it was initially set. In other words, Strict completely blocks the cookie from being used across sites. This option is best for applications that require high security, such as banks.|
|Lax|Cookies with this setting are sent only on same-site requests or top-level navigation with non-idempotent HTTP requests, such as `HTTP GET`. Therefore, this option should be used if the cookie can be used by third-parties, but with an added security benefit that protects users from being victimized by [CSRF](https://en.wikipedia.org/wiki/Cross-site_request_forgery) (Cross-Site Request Forgery) attacks.|
|None|Cookies with this setting work the same way as cookies work today.|

Keeping the above in mind, Chrome 76 (and later) introduces two settings: "SameSite by default cookies" and "Cookies without SameSite must be secure." Users have the ability to enable either setting or both settings.

|Setting|Description|
| --- | --- |
|SameSite by default cookies|When set, all cookies that don't specify the SameSite attribute are automatically forced with `SameSite = Lax`.|
|Cookies without SameSite must be secure|When set, cookies without the SameSite attribute or with `SameSite = None`, need to be Secure. Secure in this context means that all browser requests must follow the HTTPS protocol. Cookies that do not adhere to this requirement are rejected.|

![SameSite settings page](/help/c-implementing-target/c-considerations-before-you-implement-target/assets/samesite.png)

## Target follows Google's security best practices

With Target, we want to ensure that you are successful by always supporting the industry's latest best practices for security. We are happy to announce that Target supports the new security settings introduced in Google Chrome 76.

When your visitors have turned on the "SameSite by default cookies setting," Target continues to deliver personalization without any impact and without any intervention by you. Target uses first-party cookies and will continue to function properly as the flag `SameSite = Lax` is applied by Google Chrome.

When visitors enable the "Cookies without SameSite must be secure option," and you do not opt-in for Target’s cross-domain tracking feature, Target's first-party cookies continue to work. However, when you opt-in to using cross-domain tracking to leverage Target across multiple domains, Google Chrome 76 (and later) requires `SameSite = None` and `Secure` flags to be used for third-party cookies. This means that you must ensure your sites use the HTTPS protocol. Target's client-side libraries automatically use the HTTPS protocol and, in addition to that, attach the `SameSite = None` and `Secure` flags to Target’s third-party cookie to ensure all activities continue to deliver.

## What do you need to do?

Review the following table to understand what you need to do to have Target continue to work for Google Chrome 76+ users.

The table contains the following columns:

* **Target Client Side Library**: Whether you are using mbox.js, at.js 1.*x*, or at.js 2.*x* on your sites and how Google Chrome settings impact you
* **SameSite by default cookies = Enabled**: If your visitors have "SameSite by default cookies enabled" on Chrome 76+, how does it impact you and is there anything you need to do to have Target continue to work
* **Cookies without SameSite must be secure = Enabled**: If your visitors have "Cookies without SameSite must be secure" enabled on Chrome 76+, how does it impact you and is there anything you need to do to have Target continue to work
* **Adobe Target’s Cross Domain Tracking = Enabled**: If your visitors have "Same Site by default cookies" enabled and "Cookies without SameSite must be secure" enabled on Chrome 76+, and you are using Target for cross-domain tracking, how does it impact you and is there anything you need to do to have Target continue to work

|Target client-side library|SameSite by default cookies = Enabled|Cookies without SameSite must be secure = Enabled|Adobe Target’s Cross Domain Tracking = Enabled|
| --- | --- | --- | --- |
|mbox.js|No impact because mbox.js uses a first-party cookie|No impact because customers are not using cross-domain tracking|Customers must enable the HTTPS protocol for their site.<br>Target uses a third-party cookie to track users and Google requires third-party cookies to have `SameSite = None` and for sites to use the HTTPS protocol.|
|at.js 1.*x*|No impact because at.js 1.*x* uses a first-party cookie|No impact because customers are not using cross-domain tracking|Customers must enable the HTTPS protocol for their site.<br>Target uses a third-party cookie to track users and Google requires third-party cookies to have `SameSite = None` and for sites to use the HTTPS protocol|
|at.js 2.*x*|No impact because at.js 2.*x* uses a first-party cookie|No impact because customers are not using cross-domain tracking|Cross-domain tracking is not supported in at.js 2.*x* and, therefore, there is no impact to customers|

## What does Adobe need to do?

|Target client-side library|SameSite by default cookies = Enabled|Cookies without SameSite must be secure = Enabled|Adobe Target’s Cross Domain Tracking = Enabled|
| --- | --- | --- | --- |
|mbox.js|No impact because mbox.js uses a first-party cookie|No impact because customers are not using cross-domain tracking|Target adds `SameSite = None` and `Secure` flag to third-party cookie when the Target backend is called.|
|at.js 1.*x*|No impact because at.js 1.*x* uses a first-party cookie|No impact because customers are not using cross-domain tracking|Target adds `SameSite = None` and `Secure` flag to third-party cookie when the Target backend is called.|
|at.js 2.*x*|No impact because at.js 2.*x* uses a first-party cookie|No impact because customers are not using cross-domain tracking|Cross-domain tracking is not supported in at.js 2.*x*|

## Conclusion

As the industry makes strides to create a more secure web for consumers, Target is absolutely committed to delivering personalized experiences while meeting and exceeding the privacy expectations of visitors.
