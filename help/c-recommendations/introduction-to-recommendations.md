---
description: Introduction to Target Recommendations activities that automatically display products or content that might interest your customers based on previous user activity or other algorithms. Recommendations help direct customers to relevant items they might otherwise not know about.
keywords: Recommendations;
seo-description: Introduction to Adobe Target Recommendations activities that automatically display products or content that might interest your customers based on previous user activity or other algorithms. Recommendations help direct customers to relevant items they might otherwise not know about.
seo-title: Introduction to Recommendations activities in Adobe Target
solution: Target
title: Introduction to Recommendations
title-outputclass: premium
topic: Premium
badge: premium
---

# ![PREMIUM](/help/assets/premium.png) Introduction to Recommendations

The text in this article comes from the *Introduction to Recommendations* webinar, which you can view in its entirety below. In addition to the following text, the webinar includes a question-and-answer session.

## Introduction

We all know about the kinds of recommendations we see in retail. Increasingly, customers expect these kind of recommendations and use them as a starting point to explore other available options. If you think about your own shopping behavior, these kind of recommendations work. Nearly everyone among us has bought a product we saw first in a recommendation somewhere.

The following illustration shows a recommendation that displays accessories that are commonly purchased with a new phone, including charging stations, cases, and headphones.

![Recommendation showing accessories others have purchased with a new phone.](/help/c-recommendations/assets/intro-1.png)

But what we don’t always think about is how digital-first brands are raising the bar of customer expectations. Increasingly, the way we consume media and content is driven by personalized recommendations. Think about the first thing you see when you open Netflix, Spotify, or YouTube. In a world where more alternatives are available than ever, it’s critical that you can identify the most relevant content for your customer at the point of interaction.

![Recommendation showing digital-first brands](/help/c-recommendations/assets/intro-2.png)

Marketers use [!DNL Adobe Target] to drive personalized experiences across a wide variety of industries, customer types, and channels.

[!DNL Adobe Target] delivers personalized content everywhere.

![Illustration showing how Target delivers recommendations in various places](/help/c-recommendations/assets/intro-3.png)

* **Publishing**: Web publishers use [!DNL Target Recommendations] to recommend articles to site visitors and drive increased engagement.
* **Video Tutorials**: [!DNL Adobe Creative Cloud] uses [!DNL Target] to recommend video tutorials to Photoshop users in-app.
* **Gaming**: Gaming companies use [!DNL Target] to recommend games and content to users on their consoles.
* **B2B Sales**: Business-to-business companies use [!DNL Target] to recommend videos, whitepapers, and blog posts to B2B prospects; deliver downloads; and help to existing customers (https://theblog.adobe.com/testing-shifts-high-gear-intel).
* **Travel**: A German travel booker uses [!DNL Target] to recommend hotels and more to travelers (https://2017.summit.adobe.com/na/sessions/summit-online/online-2017/#17608).
* **Retail**: A leading B2B retailer uses [!DNL Target] to recommend top categories and products to return visitors in the browser and in its mobile app (https://theblog.adobe.com/optimization-personalization-b2b-powerhouse-grainger/).

What makes for great recommendations?

![Illustration showing the three elements that make great recommendations](/help/c-recommendations/assets/intro-4.png)

Great recommendations should be relevant and personalized. This means you need these three things:

* **Marketer controls** to help drive relevance of the items that are recommended. As a marketer, you bring valuable context to the table and you know what attributes of your products or content are relevant for a recommendations model to consider. If you’re running a video site, you know that users might be interested in seeing movies from the same director, but probably don’t care about seeing movies that were produced by the same studio. [!DNL Target] empowers you with controls that allow you to enhance your algorithms with this domain knowledge.
* **Sophisticated models** to make sense of millions of items in your catalog and interaction events. [!DNL Target] has sophisticated machine learning capabilities built over a decade of experience and we handle billions of recommendations per year.
* **User context** to ensure that recommendations are timely and relevant to your users. You don’t want to recommend the video that someone just watched or the shirt that someone just added to their cart. Target’s rich user profile can be used in recommendations to ensure personalization.

## Implement Target Recommendations

Start with a strategy.

![Illustration showing recommendations strategy](/help/c-recommendations/assets/intro-5.png)

* **What items do you want to recommend?** First, think about what you want to recommend. This could be products, videos, or content.
* **Where do you want to show recommendations?** Next, think about where you want to make recommendations. Broadly what channels (web, mobile, in-store, and so forth). What parts of the customer journey? What pages on your site?
* **How will you determine if recommendations are successful?** Then, suppose that you have an experience without recommendations and an experience with recommendations, or you have two different types of recommendations. How would you determine which experience was a better experience for your customers? Some metrics might be more difficult than others to measure. For example, the impact of recommendations on Customer Lifetime Value is often difficult to directly get to. So it is often easier to get to a less abstract metric and one that is more concrete, for example, revenue per visit, average order value, or number of clicks. In some cases you might be looking to minimize a metric, for example, the number of support calls.

There are three broad steps involved in creating your recommendations catalog:

![Illustration showing the steps to create your recommendations catalog](/help/c-recommendations/assets/intro-6.png)

1. Teach [!DNL Target] about your context or products.
1. Capture user behavior.
1. Get recommendations with the right context.

### Teach [!DNL Target] about your context or products

When you start with [!DNL Recommendations], you pass information about every item you want to recommend. [!DNL Target] offers several integration options to create your catalog.

![Illustration showing how to teach Target about your context or products](/help/c-recommendations/assets/intro-7.png)

The simplest, and most frequently used method is to send a CSV file on a daily or weekly basis from your product information management system or your content management system. But you can also pass information on the data layer from your page using the [!DNL Adobe Target] Javascript library, leverage our APIs to pass information directly from your source system, or use our [!DNL Adobe Analytics] integration if you are already passing catalog data to [!DNL Analytics].

Sometimes, you might want to use multiple options together, for example, passing most data daily via a CSV file and passing inventory updates more frequently via API.

Your IT department will usually be involved in helping set this step up.

Whichever method you choose, you should include metadata about each item in three categories:

![Illustration showing metadata information for your catalog](/help/c-recommendations/assets/intro-8.png)

* Data that you want to display to the user receiving the recommendation. For example, the name of the movie and an image URL.
* Data that is useful for applying marketing and merchandising controls. For example, the rating of the movie so that you do not recommend NC-17 movies.
* Data that is useful for determining the similarity of items to other pieces of items. For example, the genre of the movie.

### Capture user behavior

Next, you should add tags or leverage you existing [!DNL Analytics] implementation to track the events (such as views and purchases) that drive [!DNL Target] algorithms.

![Illustration showing how to capture user behavior](/help/c-recommendations/assets/intro-9.png)

You need to ensure that [!DNL Target]is aware of the items that your users are viewing and the items that your users are purchasing. If purchasing isn’t relevant to your context, you might want to track a different type of conversion event, for example, downloading, completing, and so forth.

If you are already using [!DNL Target] to run A/B Tests activities on your site, you might have already completed this step. Or if you are already using [!DNL Adobe Analytics] to report on site visits and conversion behavior, you can use [!DNL Analytics] as your behavioral datasource. If not, it’s easiest to set this up using a tag manager such as Adobe Launch. It’s also possible to send offline or in-app interactions to [!DNL Target] via real-time API.

### Get recommendations with the right context

Pass information about the user and context at the point of interaction to [!DNL Target] to return relevant and personalized recommendations.

![Illustration showing how to get recommendations with the right context](/help/c-recommendations/assets/intro-10.png)

Besides user behavior in aggregate, you need to pass along to [!DNL Target] the specific context where recommendations are being shown. This includes information about the page and information about the user profile. [!DNL Target] can use this information to make personalized recommendations.

## Build your first Recommendations activity

What is a good recommendations activity?

![Illustration showing the parts that make a good recommendations activity](/help/c-recommendations/assets/intro-11.png)

A good recommendations activity includes the following components:

|Component|Details|
| --- | --- |
|Audience|Who should see these recommendations?|
|Criteria|What items should be recommended?|
|Design|How should recommended items be displayed?|

![Illustration showing what makes up a recommendations activity: Audiences, Criteria, and Designs](/help/c-recommendations/assets/intro-12.png)

Out of the box, [!DNL Target] includes 14 built-in audiences, 42 built-in criteria, and 10 built-in design templates. You can customize each of these or add your own. We’ve had previous [webinars about building audiences](https://landing.adobe.com/acs/2018/na/adobe-target/registration.html) in [!DNL Target]. This article focuses on the middle part of this: defining the criteria you use for your recommendation.

## Adobe Target Basics Webinar: Introduction to Recommendations {#intro-to-recs}

The *Introduction to Recommendations* webinar includes an in-depth exploration of how to leverage the value of [!DNL Adobe Target Recommendations]. Find out how this [!DNL Target] activity automatically displays products or content that might interest your customers by optimizing real-time suggestions based on previous visits. Further, dive into the [!DNL Target] UI for a step-by-step overview of how to build a [!DNL Recommendations] activity.

[Introduction to Recommendations](https://forums.adobe.com/external-link.jspa?url=https%3A%2F%2Fadobecustomersuccess.adobeconnect.com%2Fp8gt31drhs3e%2F%3FOWASP_CSRFTOKEN%3D4bd6cac5d0806167ee0a5449ba93d6300548d09c922bcb751c38973897a5703a)