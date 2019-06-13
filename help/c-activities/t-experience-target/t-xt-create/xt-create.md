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

1. [Create any new experiences](../../../c-activities/t-experience-target/t-xt-create/xt-add-experience.md#task_454646F2895242D3B92DC395A0CE1A00) by changing the elements on the page.

   
   
   By default, the Visual Experience Composer does not allow changes to elements containing JavaScript, such as rotating banners. You can select to disable JavaScript if you want to be able to alter those elements using the Visual Experience Composer.

   >[!NOTE]
   >
   >If you change the URL after making changes to a page for one or more experiences, the experience is reset using the new page and the changes you made are lost.

   As you hover the elements on your page, the elements are highlighted. Any highlighted element can be altered using the Experience Composer.

   If you created an mbox on the page using Target Classic (formerly Test&Target), that mbox appears as an element that shows the mbox name, and can be modified like any other element.

   >[!NOTE]
   >
   >If you deliver an image from a source other than your main page (such as an image hosted on akamai.net and delivered on dell.com), then that image does not display in the thumbnail of the page shown in the flow diagram.

1. Click **[!UICONTROL Next]**.

   The flow diagram opens.

   ![](assets/xt_diagram.png)

   The flow diagram leads you through the steps of choosing the audience for the activity and setting up experiences. 
1. Mouse over the audience, click the **[!UICONTROL Edit]** icon (three vertical ellipses) that displays, click **[!UICONTROL Change Audience]**, then select the audience for the first experience in your activity.

   ![](assets/xt_change_audience.png)

   The audience library appears. The audience library contains audiences that have previously been defined, including some common audiences that are pre-built as a part of Target. You can either select an audience from the library, or [create a new audience](../../../c-target/c-audiences/audiences.md#concept_65BE870D290E412D8BBF557EEA67C271). To show the same experience to all entrants, choose All Visitors.

   >[!NOTE]
   >
   >In addition to selecting an existing audience, you can combine multiple audiences to create ad hoc combined audiences rather than creating a new audience. For more information, see [Combining Multiple Audiences](../../../c-target/combining-multiple-audiences.md#concept_A7386F1EA4394BD2AB72399C225981E5).

   When creating an audience, you can select a location (mbox) and specify parameters for that location. Under Custom Parameters, select the mbox, then specify the desired parameters.

   >[!NOTE]
   >
   >Audiences are automatically imported in the background when you open the audience list and the imported audiences are more than 10 minutes old.

   You can click the [!UICONTROL Edit] icon (three vertical ellipses) that displays, then click [!UICONTROL Remove Audience] to remove an existing audience. 
1. Click **[!UICONTROL Add Experience Targeting]**.

   >[!NOTE]
   >
   >If you are targeting an experience to an audience, you must select the audience before you can add an experience. A message appears to remind you to choose your audience.

1. (Optional) Click **[!UICONTROL Add]** and set up additional targeted experiences.

   ![](assets/xt_add_xt.png)

   Click **[!UICONTROL Continue]** when you are finished with this step. 
1. Specify the [goals and settings](../../../c-activities/t-experience-target/t-xt-create/xt-goals-and-settings.md#reference_B25389FD6F3A4989801E740364B089CC) for the activity.

   ![](assets/xt_settings.png)

1. Click **[!UICONTROL Save & Close]**.
