---
description: Select an experience to be used as control while creating an Automated Personalization (AP) or Auto-Target activity.
keywords: experience;control;automated personalization;auto-target
seo-description: Select an experience to be used as control while creating an Automated Personalization (AP) or Auto-Target activity in Adobe Target.
seo-title: Use a specific experience as control in Adobe Target
solution: Target,Analytics
title: Use a specific experience as control
uuid: c67901d2-19cd-47d3-b8c4-abdcb046f404
---

# ![PREMIUM](/help/assets/premium.png) Use a specific experience as control

You can select an experience to be used as control while creating an [Automated Personalization](/help/c-activities/t-automated-personalization/automated-personalization.md) (AP) or [Auto-Target](/help/c-activities/auto-target-to-optimize.md) (AT) activity.

This feature lets you route the entire control traffic to a specific experience, based on the traffic allocation percentage configured in the activity. You can then evaluate the performance reports of the personalized traffic against control traffic to that one experience. 

The control option to randomly serve experiences is also available. 

By using a specific experience as the control, your reports can help answer the question, "Is running an AP/AT activity better than doing what I would have done instead?" A benefit of AP/AT activities is that you can create more options that might not make sense to deliver to all users, but can be powerful for the right user. But that means that comparing our algorithm to random isn't fair; you would never run all of the options to all visitors on your site.

## Specify a specific experience as control

1. While creating an [AP activity](/help/c-activities/t-automated-personalization/create-ap-activity.md) or [AT activity](/help/c-activities/t-test-ab/t-test-create-ab/ab-audience.md), configure the experiences as desired.
1. On the [!UICONTROL Targeting] page (step 2 of the three-part guided workflow), select the desired experience as the control.
1. Specify the desired traffic allocation for the control experience and the other experiences.
1. Continue with the [!UICONTROL Goals & Settings] page.

## Known limitations

The following are known limitations when using a specific experience as control:

* Changing the control experience in an already live activity isn't advised. The latest control experience selected is named in reporting (even if older reports are based on another experience).
* Deleting the control experience isn't advised.
* In AP activities, including targeting on the control experience isn't advised that could further constrain who can see that experience.
* In AP activities, lift and confidence information is *NOT* available in the offer-level report if a specific experience is selected. Lift and confidence information is available if "random" is selected as the control.

  Lift and confidence information *is* available at the overall "targeted" vs. "control" traffic level for the activity. This difference is because comparing a specific experience's conversion rate to an offer's conversion rate isn't logical due to the difference in units.

## Troubleshooting

If problems should arise, consider the following troubleshooting tips:

* Because all control traffic goes to a single experience or set of offers when you select the experience as control (compared to random, where the control traffic amount is split over the number of experiences/offers in your activity), you generally do not need as much traffic to flow to the control. 10% is a good place to start.
* If you do one of the following to a live activity, the control is automatically reset to randomly served experiences (instead of the previously selected specific experience):

  * Delete an experience
  * Remove a location or offer (AP only)
  * Exclude an experience, manually, via removing duplicate offers or via an exclusion group (AP only)
