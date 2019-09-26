---
description: Contemporary technology product teams are adopting continuous delivery principles for product launches. Target helps developers and product teams roll out new product capabilities quickly and efficiently.
keywords: rollout;roll out;continuous delivery;product launch;phased rollout
seo-description: Contemporary technology product teams are adopting continuous delivery principles for product launches. Adobe Target helps developers and product teams roll out new product capabilities quickly and efficiently in a phased rollout.
seo-title: Contemporary technology product teams are adopting continuous delivery principles for product launches. Adobe Target helps developers and product teams roll out new product capabilities quickly and efficiently.
solution: Target
title: Feature flagging
topic: Standard
---

# Feature flagging

Contemporary technology product teams are adopting continuous delivery principles for product launches. Adobe Target helps developers and product teams roll out new product capabilities quickly and efficiently in a phased rollout.

The following links provide information for key concepts you need to understand to enable continuous delivery:

* [A/B Test activities](/help/c-activities/t-test-ab/test-ab.md)
* [JSON offers](/help/c-experiences/c-manage-content/create-json-offer.md)
* [Audience refinements](/help/c-target/c-audiences/creating-a-profile-attribute-comparison-audience.md)

## Continuous delivery

1. By default, turn the feature "off" on release.

   Use a server-side or in-app variable to control this.

1. Create a Target JSON Offer that sets this variable to "on."

1. Create an A/B Test activity in the [Visual Experience Composer](/help/c-experiences/c-visual-experience-composer/visual-experience-composer.md) (VEC) with two experiences and use the JSON offer created in the previous step in one experience.

   Or

   Create an A/B Test activity in the [Form-Based Experience Composer](/help/c-experiences/form-experience-composer.md) with a single experience and use the JSON offer created in the previous step.

   >[!NOTE]
   >
   >The Form-based Experience Composer allows you to create an A/B Test activity with a single experience. You cannot create the activity with a single experience using the VEC.

1. Specify your desired traffic allocation for the activity.

   If you want to start by rolling this feature out to 5% of your visitors, specify 5 in the Targeting step of the three-part guided workflow and send 100% of the qualifying visitors to the experience with the JSON offer (Experience A). 

   The following illustration shows the VEC with two experiences.

   ![Traffic allocation for feature flagging in the VEC](/help/c-implementing-target/c-api-and-sdk-overview/assets/feature-flagging.png)

   The following illustration shows the Form-based Experience Composer with a single experience.

   ![Traffic allocation for feature flagging in the Form-based Experience Composer](/help/c-implementing-target/c-api-and-sdk-overview/assets/feature-flagging-form.png)

1. You can increase the traffic allocation to this activity by gradually increasing the 5% either through the Target UI or using the API until you reach 100% traffic allocation.

   >[!NOTE]
   >
   >An A/B Test activity is sticky for a visitor through the session. If you decrease the traffic allocation, visitors who started seeing this feature continue to view it until their sessions are reset.

## A/B Test features

If you are using A/B/..N Test features, use the approach discussed above with the following improvements:

* Each feature variant should be represented using an appropriate JSON offer that makes a Target experience.
* You can manage traffic allocation for this test in the manner described above.

## Parametrized rollouts

The method described above helps you manage a controlled rollout. 

You can roll out a feature for your beta participants only and then later roll out the feature to all other customers. This can be easily achieved by leveraging [Target Location (mbox) parameters](/help/c-target/c-audiences/c-target-rules/custom-parameters.md) or [profile parameters](/help/c-target/c-audiences/c-target-rules/visitor-profile.md). These parameters can be used in conjunction with phased traffic allocation.

## Server-side vs. client-side

Feature rollouts and testing can be delivered via [Target APIs](/help/c-implementing-target/c-api-and-sdk-overview/api-and-sdk-overview.md) (and server-side SDKs) as well as the client side SDKs (JS, Mobile SDK). Depending on how your website, mobile app, or kiosk is architected, you can leverage Target's different integration options.
