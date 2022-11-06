---
title: Target users based on video consumption
category: Advertising
author: Christopher Hoover
date: 2021-03-02
tags: ['Google Ads']
description: | 
  Build an audience made up of people that have watched a certain amount of a video.
---

There are many ways to build an audience to target with specialized advertising. In this post we’ll discuss one of them, an audience made up of people that have watched a certain amount of a video (say 50% or more).

Targeting based on video consumption is useful because many businesses use videos to communicate their value proposition. Unlike white papers or other forms of written content, you can measure how much of a video has been watched. You can then use that data to create audiences with different levels of interest in your product.

## What you’ll learn

This post goes over

- An introduction to Audience Lists
- How Audience Lists work for custom targeting
- How to integrate YouTube data into Google Analytics
- How to create audience lists based on video engagement
- How to create targeted advertisements for audience lists
- How Analytics can deepen your understanding of customer behavior

## An introduction to Audience lists

An audience (also called a user list) is a group of users that performed some action on your site. The nature of the action is up to you. Examples include:

- **A visitor to your website**: this can include anyone who visited any page on your site, or a particular page, or some combination of pages.
- **A visitor that took a specific action**: this can include someone that viewed some portion of a video (discussed in this post), downloaded a white paper, or abandoned a cart.

It’s possible to create an audience out of two or more audiences:

- **A combination**: for example, people that downloaded a piece of content and also viewed a video.

Google will also automatically create an audience for you based on existing audiences or leads

- **Similar audiences**: made up of people that share interests and behaviors with users in other lists.
- **Lead audience:** also called “Customer match with email” is an audience made up of uploaded email addresses. This enables you to target advertising to leads already in your system.

## How audience lists work with AdWords

You can use audiences to target specific messages to specific groups of people, or you can select one or more audiences to be excluded from certain advertising. The way it works is this: a visitor to your site is tracked anonymously by storing small bits of data (called a cookie) in the user’s computer. When a user’s behavior meets the criteria to join an audience, Google adds the associated cookie ID to the audience. When the user then visits sites on the Google Display Network or uses Google Search, the cookie identifies the user as a member of an audience.

## Make sure remarketing is on in Google Analytics

Before any of this will work you need to turn on Remarketing in Google Analytics. To do this, navigate to Admin in the left-hand column, then select tracking info, then select Data Collection ![](https://blog.adfury.io/wp-content/uploads/RemarketingOn.png)

## Preparing to track embedded videos

To monitor events within individual videos, you need to add a little snippet into the embed code of your video, after the question mark: jsapi=1 Your embed code will look like this (I've outlined the little snippet in red): ![](https://blog.adfury.io/wp-content/uploads/TrackingVideo.png) Note that this will enable monitoring of videos _embedded on your website_. It does not monitor videos that are watched directly from your YouTube channel.

## Get the monitoring file from Google

By adding enablejsapi=1 to your embed code, you are flagging which video you would like to monitor. The next step is to set up the monitoring so that you capture interaction data. You do this by deploying a file through Google Tag manager.

Download the file from [http://goo.gl/c4rP83](http://goo.gl/c4rP83)

Now log onto Google Tag Manager and choose the container that you want to use to monitor these videos. In our case, have one container: ![](https://blog.adfury.io/wp-content/uploads/TagMgrContainer.png)

Once you select your container, select Admin at the top of the page, and then select import container ![](https://blog.adfury.io/wp-content/uploads/TagManager2.png) Select the file you downloaded from Google as the file to import.

You have the option to overwrite or merge the workspace with the content of the container. **We suggest you select merge and rename conflicting tags**. This is the safest option and will prevent you from losing data on already in your workspace.

At the bottom of the page you’ll see a summary of the tags, triggers, and variables you are adding. Review it and click Confirm. ![](https://blog.adfury.io/wp-content/uploads/TagManager3.png)

## **What you just added to you tag manager**

You’ve just added two tags, two triggers, and two variables to your Tag manager. Here’s a summary: **Tags**

- YouTube Listener: detects events that occur through videos that include jsapi=1 in its embed code and sends data to Analytics
- YouTube Events: a universal Google Analytics event triggered when it receives data from the YouTube Listener

**Triggers**

- YouTube Ready: triggered when it finds a YouTube video with jsapi=1 in the embed code.
- YouTube Event: triggered when the YouTube listener detects an event.

**Variables**

- Is YouTube Present: is true if it finds at least one video with jsapi=1 in the embed code
- Data Layer Action and Label: retrieves the values exposed by the YouTube Listener.

## Monitor how videos are performing in Google Analytics

You can now track embedded YouTube videos using Google Tag Manager and Google Analytics. You can dive into details about how videos are performing by

- Navigate to Behavior --> Top Events and click on Video
- Click on customize at the top of the report
- Under Dimension Drilldowns, remove the Event Category dimension and switch Event Action with Event Label
- Modify the filter to “Event Category equals Video” to show videos in this report

## Create an audience in Google Analytics

You can create audiences based on _any_ segment monitored by Google Analytics, including video viewing data. To set up an audience, the first thing you must do is define a _segment_, which is Google's term for a filtered view of your website audience.

In this case, we are building a segment of users who have watched at least 50% of a video. The nuts and bolts of building a segment is outside of the scope of this blog post. If you're not sure how to do it, you can begin with the [Google article on building new segments](https://support.google.com/analytics/answer/3124493?hl=en).

Once you have a segment created, you can build an audience based on the segment by clicking the arrow next to the segment title. For example, the image below shows a segment called "Video 50%" which includes all users. ![](https://blog.adfury.io/wp-content/uploads/BuildAudience.png)

When you save an audience, it becomes available in AdWords, and you can use it in the remarketing campaigns you manage there.

## Using an audience in Google AdWords

Now that we have an audience of users who have watched at least 50% of a specific video, we can create a campaign targeted toward that audience.

The easiest way to do this is to click the AdWords link in your audience list.

In Analytics, navigate to Admin --> Audience Definitions --> Audiences Then click the AdWords logo next to the audience you want to use. ![](https://blog.adfury.io/wp-content/uploads/Audience.png)   1 Linked References Adfury blog [[Advertise to leads based on video consumption]] Unlinked References
