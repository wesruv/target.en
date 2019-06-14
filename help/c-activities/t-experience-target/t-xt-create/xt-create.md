---
description: Use the Visual Experience Composer to create an Experience Targeting activity on a Target-enabled page and to modify portions of the page within Target.
seo-description: Use the Visual Experience Composer to create an Experience Targeting activity on a Target-enabled page and to modify portions of the page within Adobe Target.
seo-title: Create an Experience Targeting activity
solution: Target
subtopic: Multivariate Test
title: Create an Experience Targeting activity
topic: Standard
uuid: 6299982b-b1ba-4dd0-9c69-36a76680a3e1
---

# Create an Experience Targeting activity{#create-an-experience-targeting-activity}

Use the [!UICONTROL Visual Experience Composer] (VEC) to create an [!UICONTROL Experience Targeting] (XT) activity on a Target-enabled page and to modify portions of the page within [!DNL Adobe Target].

1. From the [!UICONTROL Activities] list, click **[!UICONTROL Create Activity]** > **[!UICONTROL Experience Targeting]**.

   ![Create Activity > Experience Targeting](/help/c-activities/t-experience-target/t-xt-create/assets/xt_select-1.png)

   >[!NOTE]
   >
   >The available activity types depend on your Target account. Some activity types might not appear in your list. For example, Automated Personalization is a [Target Premium feature](/help/c-intro/intro.md#premium).

   For information about the activity types, see [Activities](../../../c-activities/activities.md#concept_D317A95A1AB54674BA7AB65C7985BA03) and [Target Activity types](/help/c-activities/target-activities-guide.md).

1. Select **[!UICONTROL Visual (Default)]**, if necessary.

   ![Create Experience Targeting Activity dialog box](/help/c-activities/t-experience-target/t-xt-create/assets/form_url-new.png)
   
   If you prefer to use the Form-Based Experience Composer, select that option. See [Form-Based Experience Composer](https://marketing.adobe.com/resources/help/en_US/target/target/t_form_experience_composer.html).

   >[!NOTE]
   >
   >In addition to the VEC and Form-Based Experience Composer, Target offers the Single Page Application VEC and the VEC for Mobile Apps. For more information about the various composers, see [Experiences and Offers](/help/c-experiences/experiences.md).

    For troubleshooting information about the VEC, should you have problems, see [Troubleshooting the Visual Experience Composer](../../../c-experiences/c-visual-experience-composer/r-troubleshoot-composer/troubleshoot-composer.md#reference_77743144F10143A3A89D56E116D296E4).

1. Specify your [activity URL](../../../c-activities/t-experience-target/t-xt-create/xt-activity-url.md#concept_D28549AAA0A14E3BB5F05F32BE8ABC90), then click **[!UICONTROL Next]**.

   If your account is configured with a default URL, that URL appears by default. You can change from the default to another URL.

   The Visual Experience Composer opens, showing the page specified in the URL.

   ![Experience Targeting activity within the VEC](/help/c-activities/t-experience-target/t-xt-create/assets/xt-in-vec.png)

1. Type a name for the activity in the space provided.

   ![Name field](/help/c-activities/t-experience-target/t-xt-create/assets/xt_name-new.png)

   The following characters are not allowed in an activity name:

   | Character | Description |
   |--- |--- |
   |`/`|Forward slash|
   |`?`|Question mark|
   |`#`|Number sign|
   |`:`|Colon|
   |`=`|Equals to|
   |`+`|Plus|
   |`-`|Minus|
   |`@`|At sign|

1. Create any new experiences by changing the elements on the page.

   For step-by-step instructions, see [Add experience](/help/c-activities/t-experience-target/t-xt-create/xt-add-experience.md).

   By default, the Visual Experience Composer does not allow changes to elements containing JavaScript, such as rotating banners. You can select to disable JavaScript if you want to be able to alter those elements using the Visual Experience Composer.

   As you hover the elements on your page, the elements are highlighted. Any highlighted element can be altered using the VEC. For a list of actions that can be performed on an element to change the experience, see [Visual Experience Composer Options](/help/c-experiences/c-visual-experience-composer/viztarget-options.md).

   If you created an mbox on the page using Target Classic (formerly Test&Target), that mbox appears as an element that shows the mbox name, and can be modified like any other element.

1. Specify the [goals and settings](../../../c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) for the activity.
