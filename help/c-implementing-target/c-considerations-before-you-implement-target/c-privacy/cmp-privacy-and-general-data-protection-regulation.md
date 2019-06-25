---
description: Information about the European Union's General Data Protection Regulation (GDPR) and a list of Frequently Asked Questions about how this regulation impacts your organization and Adobe Target.
keywords: gdpr;eu;european union;privacy;faq;frequently asked questions
seo-description: Information about the European Union's General Data Protection Regulation (GDPR) and a list of Frequently Asked Questions about how this regulation impacts your organization and Adobe Target.
seo-title: Privacy and General Data Protection Regulation (GDPR)
solution: Target
title: Privacy and General Data Protection Regulation (GDPR)
topic: Standard
uuid: 5e67adcf-464c-495f-9ba5-15152d9a6a41
---

# Privacy and General Data Protection Regulation (GDPR){#privacy-and-general-data-protection-regulation-gdpr}

Information about the European Union's General Data Protection Regulation (GDPR) and a list of Frequently Asked Questions about how this regulation impacts your organization and Adobe Target.

## Overview of the Privacy and General Data Protection Regulation (GDPR) {#topic_DE567ECB6C944695AEE5073889F1AEA9}

Information about how Adobe works with you to become GDPR-ready with the European Union's General Data Protection Regulation (GDPR).

## GDPR Overview {#section_8C99434A431B4494998B01B869E7EA5D}

On May 25, 2018, the European Union's GDPR goes into effect. For more information about what this means for you, see [GDPR and Your Business](https://www.adobe.com/privacy/general-data-protection-regulation.html).

When Adobe is providing software and services to an enterprise, Adobe is acting as a Data Processor for any personal data it processes and stores as part of providing these services. As a Data Processor, Adobe processes personal data in accordance with your company's permission and instructions (for example, as set out in your agreement with Adobe).

As the Data Controller, you determine the personal data that Adobe processes and stores on your behalf. If you use Adobe Experience Cloud solutions, Adobe might host personal data for you, depending on the solutions you use and the information you choose to send to your Adobe Experience Cloud account. For a detailed list of examples, see [Adobe Experience Cloud Privacy](https://www.adobe.com/privacy/marketing-cloud.html#collect).

Adobe Experience Cloud will be providing GDPR-ready APIs for Data Controllers that allow them to complete the following tasks, prior to the GDPR regulation's effective date:

* Access Data Subject information stored within Target 
* Delete Data Subject information stored within Target

## The Adobe General Data Protection Regulation API Website {#section_51B8FA3CBE234E9592BDA7083B5CE4CD}

For more information, see:

* [Adobe General Data Protection Regulation API website](https://www.adobe.io/apis/cloudplatform/gdpr.html) 
* [GDPR Documentation](https://www.adobe.io/apis/cloudplatform/gdpr/docs.html)

## Adobe Target and Adobe Launch Opt-In {#section_6F7B53F5E40C4425934627B653E831B0}

Target provides opt-in functionality support via Adobe Launch to help support your consent management strategy. Opt-in functionality lets customers control how and when the Target tag is fired. There is also an option via Adobe Launch to pre-approve the Target tag. To enable the ability to use Opt-In in Target at.js, you should use `targetGlobalSettings` and add the `optinEnabled=true` setting. In Launch you'll need to select "enable" from the GDPR Opt-In drop-down list in the Target Launch Extension installation view. See the [Launch documentation](/help/c-implementing-target/c-implementing-target-for-client-side-web/how-to-deployatjs/cmp-implementing-target-using-adobe-launch.md) for more details.

The following code snippet shows you how to enable the `optinEnabled=true` setting:

```
window.targetGlobalSettings = {
  optinEnabled: true
};
```

>[!NOTE]
>
>Opt-in functionality is supported in at.js version 1.7.0 and at.js 2.1.0. Opt-in is not supported in at.js version 2.0.0 and 2.0.1.
>
>Using Adobe Launch to manage opt-in is the recommended approach. Further granular control exists in Adobe Launch to hide selected elements of your page prior to Target firing that are helpful to leverage as part of your consent strategy.

There are three scenarios to consider when using Opt-In:

1. **The Target tag is pre-approved via Adobe Launch (or the data subject previously approved Target):** The Target tag is not held for consent and functions as expected. 
1. **The Target tag is NOT pre-approved and `bodyHidingEnabled` is FALSE:** The Target tag fires only after consent is collected from the customer. Before consent is collected, default content only is available. After consent is received, Target is called and personalized content is available to the data subject (visitor). Because only default content is available before consent, it is important to leverage an appropriate strategy, such as a splash page that covers any portion of the page or content that might be personalized. This ensures that the experience remains consistent for the data subject (visitor). 
1. **The Target tag is NOT pre-approved and `bodyHidingEnabled` is TRUE:** The Target tag fires only after consent is collected from the customer. Before consent is collected, default content only is available. However, because `bodyHidingEnabled` is set to true, `bodyHiddenStyle` dictates what content on the page is hidden until the Target tag is fired (or the data subject declines opt-in, in which case default content is displayed). By default, `bodyHiddenStyle` is set to `body { opacity:0;`}, which hides the HTML body tag. Our recommended page configuration is below so that the entire body of the page, other than the consent manager dialog, is hidden by putting the content of the page in one container and the consent manager dialogue in a separate container. This setup configures Target so that it hides the page content container only. See [Adobe Launch documentation for more information on how to configure these settings](https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.html).

   The recommended page setup for scenario 3 is:

   ```
   <html> 
   <head> 
   //visitor, at.js 
   </head> 
    
   <body> 
   <div id = "consentManagerDialog"> 
    
   //consent manager html dialog goes here 
   </div> 
    
   <div id="pageContent"> 
   // page content goes here 
   </div> 
    
   </body> 
   </html> 
   
   ```

   Assuming the `bodyHiddenStyle` of:

   ```
   #pageContent { opacity:0;}
   ```

## General Data Protection Regulation FAQ {#concept_41F88DE95D2943178BEC382736B5C038}

Frequently Asked Questions about the General Data Protection Regulation (GDPR) specific to Adobe Target.

### What is Adobe's policy for General Data Protection Regulation (GDPR)? {#section_A6849628D6524C80A6E16946DC5D25A9}

Adobe either already meets or is implementing our obligations as a Data Processor. We have a strong foundation of certified security and privacy controls by design and will continue to make product enhancements in advance of the May 2018 deadline. Enterprise customers will have the responsibility to implement these enhancements, as well as update any necessary policies and procedures.

### Will my company, the Data Controller, need to submit a GDPR request to each Adobe Experience Cloud solution that it uses? {#section_1DCFA9387D0C4506B14DCE04C49AC22A}

No, Adobe is providing a central way to help Data Controllers meet their GDPR requirements. Data Controllers will not need to go directly to each solution.

All GDPR requests across Experience Cloud solutions, including Target, will be made through a central Adobe API, currently called the GDPR API. The API will then complete the request across the Data Controller's Experience Cloud solution suite.

### What information will Adobe enable our customers to delete in response to a data subject/user request? {#section_4B51D00924EC4166B2442218B69214F0}

The information related to an individual visitor within Target is contained within the Target Visitor Profile. Adobe Target will enable our customers to delete all data associated with an ID in their Visitor Profile. For examples of the profile data Adobe Target stores, see [Visitor Profile](../../../c-target/c-audiences/c-target-rules/visitor-profile.md#concept_E972690B9A4C4372A34229FA37EDA38E).

Aggregated or anonymized data (for example, reporting data) that does not identify a particular individual, or data that is unrelated to a specific individual (for example, content data), is outside the scope of a user-deletion request.

Target Visitor Profiles that have been inactive for 90 days are deleted by default, without any action required.

### What IDs are supported to help customers complete a GDPR access and deletion request for Target? {#section_F7D0EE4E6A28490FB20056A0D26118BC}

Target supports the following ID types to locate a customer profile:

| User ID | Name Space ID Type | Namespace ID | Definition |
|--- |--- |--- |--- |
|Experience Cloud ID (ECID)|Standard|4|Adobe Experience Cloud ID, formerly known as Visitor ID or Marketing Cloud ID. You can use the JavaScript API to locate this ID (see details below).|
|TnT ID / Cookie ID(TNTID)|Standard|9|Target identifier set as a cookie in the visitor’s browser. You can use the JavaScript API to locate this ID (see details below).|
|3rd-Party ID / CRM ID (THIRDPARTYID)|Target-Specific|N/A|If you provide Target with your CRM or other unique identifier information for your customers.|

>[!NOTE]
>
>Although Adobe Target supports both first-party and third-party cross-domain cookies, first-party Adobe Target cookies only are recommended for GDPR.

### How does Adobe Target handle consent management? {#section_C86BF5EE4FAA47039659850E7594A6BA}

GDPR doesn't change when you need to get consent, but how you get it. Each customer's consent strategy depends on its data collection and use practices as well as its privacy policy. Consent management isn’t supported by and shouldn’t be achieved via Target for GDPR.

Adobe does not currently offer a Consent Management Solution, but there are various tools developing in the market to address some of the new requirements. For more information on privacy tools in general, including consent managers, see the [2017 Privacy Tech Vendor Report](https://iapp.org/media/pdf/resource_center/Tech-Vendor-Directory-1.4.1-electronic.pdf) on the International Association of Privacy Professionals (iaap) website.

Adobe Target does provide opt-in functionality support via Adobe Launch to provide support your consent management strategy. Opt-in functionality lets customers control how and when the Adobe Target tag is fired. There is also an option via Adobe Launch to pre-approve the Adobe Target tag. Using Adobe Launch to manage opt-in is the recommended approach. Further granular control exists in Adobe Launch to hide select elements of your page prior to the Adobe Target firing that might be helpful to leverage as part of your consent strategy.

For more information on GDPR and Adobe Launch, see [The Adobe Privacy JavaScript Library and GDPR](https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.html). Also, see the “Adobe Target and Adobe Launch Opt-In” section above.

### Does AdobePrivacy.js submit information to the GDPR API? {#section_1EB8A2BAAD31474C97C1D455F41DA739}

[!DNL AdobePrivacy.js] does *not* submit this information to the API. The customer must do that. This library provides only the IDs that are stored in the browser for that specific visitor.

### What does removeIdentities remove? {#section_D3A1591EA1B84C499CE1563DEAF32448}

[!DNL removeIdentities] *only* removes those identities from the browser, and that only depends on whether the Adobe solution has implemented it.

For example, Target deletes the cookies storing its IDs, but Adobe Audience Manager (AAM) does not delete the demdex ID that is stored in a 3rd-party cookie.

### What information needs to be included in a Target GDPR request? {#section_D29A4744AE6344E68AD7710B185FD6D0}

In addition to the requirements from Central Privacy Service, a valid GDPR message for Target contains:

```
{ 
    "jobId":"12345AD43E", 
    ... 
    "products":["Target",...], 
    "companyContexts":[ 
        { 
            "namespace":"imsOrgID", 
            "value":"123456789@AdobeOrg" 
        }, 
        ... 
    ], 
    "userContexts":[ 
        { 
            "namespace":"ECID", 
            "namespaceId":4, 
            "type":"standard", 
            "value":"53792210477379708453829363835595041181" 
        } 
        And/OR: 
        { 
            "namespace":"TNTID", 
            "namespaceId":9, 
            "type":"standard", 
            "value":"1234567890" 
        } 
        And/OR: 
        { 
            "namespace":"THIRDPARTYID", 
            "type":"target", 
            "value":"thirdPartyIdName" 
        }, 
        ... 
    ] 
}
```

### What types of responses can I expect from Target via the GDPR API? {#section_F67263D2A72B4641A47CE36729CCAE8F}

| Request Status | Target Response Message | Scenario |
|--- |--- |--- |
|Processing|Processing|Target received the GDPR request and is processing.|
|Complete|Not applicable - company context not applicable|The IMS ID in the GDPR request is not mapped to any Target client.<br>Note that some companies have multiple IMS IDs. You must submit the IMS ID where Target is provisioned.|
|Complete|Not applicable - user context not found|The ID provided in the GDPR request for the specific visitor or data subject is not present in the Target profile store.<br>Note that this result also returns if you attempt to submit a namespace ID type that is not supported by Target (see above for supported IDs).|
|Error|Error Message (details depend on the type of error)|Error while fetching or deleting the requested data subject profile.<br>Error while uploading to Azure for access request.|

### What response does Target send to the GDPR API for an access request? {#section_D96D8FBEAF9C4BDAA638215FAFE00763}

Responses to access data requests contain a summary of the Target profile for the visitor in question. Note that this return is sent to the Experience Cloud GDPR API, which in turn sends Data Controllers a response.

A sample Target access API response could look like this:

```
{ 
    "jobId":"12345AD43E", 
    ... 
    "products":["Target",...], 
    "companyContexts":[ 
        { 
            "namespace":"imsOrgID", 
            "value":"123456789@AdobeOrg" 
        }, 
        ... 
    ], 
    "userContexts":[ 
        { 
            ~"namespace":"ECID", 
            "namespaceId":4, 
            "type":"standard", 
            "value":"53792210477379708453829363835595041181" 
        } 
        And/OR: 
        { 
            ~"namespace":"tntId", 
            "namespaceId":9, 
            "type":"standard", 
            "value":"1234567890" 
        } 
        And/OR: 
        { 
            "namespace":"thirdPartyId", 
            "type":"target", 
            "value":"thirdPartyIdName" 
        }, 
        ... 
    ] 
} 

```

| Field | Description |
|--- |--- |
|jobId|Indicates the GDPR job ID from the Central GDPR API.|
|imsOrgID|Provides a unique identifier for your company.|
|namespace|Also referred to as data source. See "What IDs are supported to help customers complete a GDPR access and deletion request for Target?" in this topic.|
|type|The type of ID for which you requested the GDPR data access. Target accepts several ID types, some of which are standard and some of which are Target-specific. See "What IDs are supported to help customers complete a GDPR access and deletion request for Target?" in this topic.|
|value|The ID of the namespace/data source. See "What IDs are supported to help customers complete a GDPR access and deletion request for Target?" for accepted values.|
|integration code|Integration codes are friendly names for your data sources and help you track your data sources easier than using data source IDs.|

When multiple values are provided to identify profiles, each valid identifier has one profile file. The profile file(s) are sent to the central GDPR Azure Blob through the GDPR Central API, in the format of Target Profile JSON response.

A sample Target Profile JSON could look like the following example:

```
{"profileAttributes": 
 
"Sample_Parameter":{"value":"Gold Loyalty Status","modifiedAt":"2018-04-11T21:44:14.000-04:00"}, 
 
"user.ReturnTimeOfDay":{"value":"44.0","modifiedAt":"2018-04-11T21:44:14.000-04:00"}, 
 
"firstSessionStart":{"value":"1523497450602","modifiedAt":"2018-04-11T21:44:10.000-04:00"}, 
 
"user.sessionCountScript":{"value":"1","modifiedAt":"2018-04-11T21:44:14.000-04:00"} 
   } 
} 

```

The following table contains description of the illustrative profile JSON fields:

| Field | Description |
|--- |--- |
|Sample_Parameter|Many pieces of information in the Target profile are uploaded or directly provided by the Data Controller. In this example, a parameter was uploaded into the Target profile using the Profile Update API. For more information, see [Methods to get Data into Target](/help/c-implementing-target/c-considerations-before-you-implement-target/c-methods-to-get-data-into-target/methods-to-get-data-into-target.md).|
|user.ReturnTimeOfDay|This standard field includes the time of day of a user’s most recent return visit.|
|firstSessionStart|This standard field includes the time of day the user’s first session began.|
|user.sessionCountScript|Many pieces of information in the Target profile are uploaded or directly provided by the Data Controller. In this example, a profile script is incrementing the number of sessions this visitor has made to the Data Controller’s site. For more information, see [Profile Script Attributes](/help/c-target/c-visitor-profile/profile-parameters.md).|

>[!NOTE]
>
>This is a shortened version of a Target profile JSON for the purpose of illustration. Many of the fields of the Target profile are not standard. What is returned depends on what information is in that specific visitor profile.

## Does Target support IP obfuscation? {#section_428907B0CD9842D9B245B38C66A53C6A}

Target supports IP obfuscation in Target if you choose to use it as part of your GDPR implementation strategy. For more information, see [Privacy](../../../c-implementing-target/c-considerations-before-you-implement-target/c-privacy/privacy.md#concept_639482A343DB4963A6144378E1D8D7F0). 
