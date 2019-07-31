---
description: Release notes that provide information about features, enhancements, and fixes for the latest or upcoming [!DNL Adobe Target] releases.
keywords: release notes
seo-description: Release notes that provide information about features, enhancements, and fixes for the latest or upcoming [!DNL Adobe Target] releases.
seo-title: Adobe Target release notes (prerelease)
solution: Target
title: Target release notes (prerelease)
topic: Standard
uuid: 35ecabbe-b8b4-479b-9266-4823c831d79a
---

# Target release notes (prerelease){#target-release-notes-prerelease}

These release notes provide information about features, enhancements, and fixes for the latest or upcoming [!DNL Adobe Target] releases.

**Last Updated: July 31, 2019**

>[!NOTE]
>
>These release notes contain prerelease information. Release dates, features, and other information are subject to change without notice. To view information about the current release, see [Target Release Notes](release-notes.md). The information on these pages might be the same or it might differ, depending on the timing of releases.
>
>The issue numbers in parentheses are for internal [!DNL Adobe] use.

## Announcements

Enterprise Permissions allows [!DNL Target] customers to use a single organization, but divide it into workspaces for their different teams or workflows. This facilitates effective scaling of their optimization program across teams. Although the feature was available in the [!DNL Target] UI, the Admin APIs lacked the corresponding support until earlier this year. In the [!DNL Target] February 2019 release, Adobe updated the Admin APIs so that you can use the integration account to access all workspaces created in your organization. So, while earlier, Admin APIs were restricted to just the default workspace, the February update granted access to all workspaces with [!UICONTROL Approver] access.

With the upcoming [!DNL Target] September 2019 release, Target Enterprise Permissions will provide customers with the following access controls:

* You can choose the workspaces to which the integration can be applied
* You can apply a role to the Adobe I/O integration: [!UICONTROL Approver], [!UICONTROL Editor], or [!UICONTROL Observer].

This update will support the following use cases:

* Grant the Adobe I/O integration access to all workspaces with the [!UICONTROL Observer] role for reporting purposes with no rights to create or edit resources.
* Grant the Adobe I/O integration the access to select workspaces with the appropriate role to allow a central team to make API-driven changes in only a few workspaces.
* Each team owning its workspace decides to have its own integration whenever the team is ready to explore APIs and choose the role accordingly.
* Mix and match any of above scenarios.

**Action Needed**: Those customers who are currently leveraging APIs for CRUD operations on resources (activities, audiences, offers, and reporting) across all workspaces need to grant their existing Adobe I/O integration access to all workspaces with the desired role as per their use case. You can do so by selecting each [!DNL Target] [!UICONTROL Product Profile] in the [!DNL Adobe Admin Console] and adding the integration(s) in the [!UICONTROL Integration] tab. Prior to the September release, all integrations operated using [!UICONTROL Approver] access, irrespective of choice made in the [!UICONTROL Product Role] drop-down list. You can now choose the desired role.

This action *must* be performed before September 4, 2019 to not face any disruption on your end. If this action is not performed, after the [!DNL Target September release, the access controls will activate and you will observe access to just the default workspace if that's how you are currently set up. There is no adverse reaction to setting up integrations in advance as per the above guidelines. The sooner you make this change, the better. Little time is required to set this up, depending on the number of workspaces in your organization. This process takes only a few clicks to add an existing integration into workspaces with the desired role.

## Target Standard/Premium 19.8.1 (August 20, 2019) {#tgt-19-8-1}

This maintenance release includes the following enhancement:

* Several security fixes, including a security update to the Rich Text Editor (RTE) in the Visual Experience Composer (VEC). (TGT-35383)

## Prerelease information {#section_7B9D4AAFC6A74388B9D7DEF0658D8B63}

To receive advance notifications about upcoming product enhancements to Target and other Adobe Experience Cloud solutions, sign up for the Adobe Priority Product Update:

[https://www.adobe.com/subscription/priority-product-update.html](https://www.adobe.com/subscription/priority-product-update.html) 
