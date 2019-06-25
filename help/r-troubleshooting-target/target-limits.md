---
description: Information about the character limits and other limits (offer size, audiences, profiles, values, parameters, etc.) that affect activities and other elements in Adobe Target.
keywords: character limit;mbox parameters;batch delivery api;profile parameters;limits;built in profiles;maximum;limit;constraint;character;best practice;orderid;orderTotal;mbox3rdPartyID;category;categoryID
seo-description: Information about the character limits and other limits (offer size, audiences, profiles, values, parameters, etc.) that affect activities and other elements in Adobe Target.
seo-title: Limits
solution: Target
title: Limits
topic: Standard
uuid: 603fb800-a26c-43ec-b2d9-ef7a8ed8721e
---

# Limits{#limits}

Information about the character limits and other limits (offer size, audiences, profiles, values, parameters, etc.) that affect activities and other elements in Adobe Target.

 The limits listed below are recommended limits. When these limits are approached or exceeded, performance can slow. Slow interface load times can also be caused by a very complex activity, such as many audiences, targets, and experiences all in one activity. 
 
 Highly complex activities should be reviewed with Adobe Consulting and tested in a limited environment before being released to production.

## Activity names

**Limit**: 250 characters.

## Audience names

**Limit**: 256 characters.

Values longer than 256 characters are truncated.

## categoryId parameter

**Limit**: 250 characters.

## Customer attribute names

**Limit**: 128 characters.

## Customer attribute alias ID

**Limit** 50 characters.

## Entity custom attributes

**Limit**: The maximum length depends on the language.

* 15,000 characters (single-value, one- and two-byte languages)
* 500 values, 100 characters per value (multi-value)

The maximum length of single-value entity custom attributes is 15,000 characters (for one- and two-byte UTF-8 encoded languages such as English and other Latin-script alphabets) or 10,000 characters (for three-byte UTF-8 encoded languages such as Chinese, Japanese and Korean).

Multi-value entity custom attributes can contain no more than 500 values. Each individual value is limited to 100 characters. The total number of characters across all values must conform to the limitations for the maximum length of single-value entity custom attributes (see above.)

## entityID parameters

**Limit**: 1,000 characters.

## excludedIds {#excludedid}

**Limit**: 5 KB for POST requests. 2,083 characters minus the length of the URL for GET requests.

For GET requests, although the limit on the back end is 5 KB, due to the fact that Microsoft Internet Explorer limits the URL to 2,083 characters, the realistic limit is 2,083 characters minus the current length of the URL.

## Experience names

**Limit**: 20 characters.

## In-mbox profile attribute value

**Limit**: 256 characters.

Values longer than this get truncated.

## In-mbox profiles in an mbox request

**Limit**: 50 profiles.

All profiles after 50 are ignored.

## In-mbox profile names

**Limit**: 128 characters.

## mbox names

**Limit**: 250 characters.

## mbox parameters

**Limit**: The following limits apply to mbox parameters:

* mbox parameters: 500 parameters per mbox.
* Profile parameters: 500 parameters.
* profile parameters per mbox:
* Other Parameters (URL, referring URL, etc.): 50 per mbox for each other parameter type.

For parameters that get logged in the Target database, the limits above are for standard mbox requests. These limits apply unless the request is shortened due to web browser limitations.

If you are using the [Batch Delivery API](https://developers.adobetarget.com/api/#server-side-batch-delivery) in the Mobile Services SDK, the limit of 50 mbox parameters, 50 profile parameters, and 50 for other parameter types are limitations of the API itself. It is not possible to send a request containing more that these numbers using the Batch Delivery API. If a request contains more than these limits, the API will return the following error message:
"The number of mboxParameters cannot exceed 100."

## mbox request URLs

**Limit**: 2,083 characters.

This limit is due to Microsoft Internet Explorer URL length restrictions.

## mbox3rdPartyId parameter

**Limit**: 60 characters.

## Offer names

**Limit**: 250 characters.

## Offer size

**Limit**: The following size limits apply to offers:

* 256 KB for HTML offers. 
* 64 KB for visual offers from the UI. 
* 512 KB from the API.

If you are using a global mbox, the limit is for the whole set of content returned for the page. Limiting offer size improves page load times. If the limit is exceeded, the following message appears:

"The content for the experience is too large to deliver. Please modify the experience to affect less page code."

## orderId parameter

**Limit**: 120 characters.

Recommended limit.

## orderTotal parameter

**Limit**: 120 characters.

Recommended limit.

## productPurchasedId parameter

**Limit**: 47 characters per comma-separated value.

Anything longer is truncated by the system.

## Reusable Audiences/Account

**Limit**: 75 audiences.

Recommended limit. JavaScript timeouts occur in the interface if you have too many.

## Script profile input box in the Target UI

**Limit**: 2,000 characters.

Recommended limit. Depends on the size of the encoded string, which could be much longer than the raw string. If the string is too large, it fails before it gets to Adobe Target.

## Script profile names

**Limit**: 50 characters.

## Script profile values

**Limit**: 2,048 characters.

For performance reasons, we recommend a return value that is no longer than 256 characters.

For a String return value, if the size of the return value exceeds 2,048 characters, the script is disabled by the system.

For an array return value, if the size of the concatenated values of the array exceeds 2,048 characters, the script is disabled by the system.

## Target conditions

**Limit**: 1,000 values.

Recommended limit. This refers to the number of line-separated values in the targeting text area. For example, entering 1,000 zip codes into a zip code target.