---
title: Dynamic ad copy based on user or device
category: Advertising
author: Christopher Hoover
date: '2021-03-02'
tags: ['Google Ads']
description: | 
  Powerful tools that alter ad copy if certain conditions are met.
---

These are powerful tools that alter ad copy if certain conditions are met, but they are underused because people worry that they are way too complicated to understand. But they aren't difficult at all. They are actually super easy. And using them gives you an edge as your ads compete for attention. 

## What you'll learn in this post

This post will describe how to hack your ads so that they automatically change ad copy depending on searcher, without having to create multiple ads.

- Display special ad copy if a user is on a mobile device, and different copy if not
- Display special ad copy if a user is a member of a particular audience, and different copy if not

## How all this works

The IF function is text in a special format. Let's take a look at a mobile condition, and then break it down to show how easy it is. Here's the function in all its glory:

```
 {=IF(device=mobile, Free Shipping On Mobile Orders): Buy Now} 
 ```
 If you're not technical, that can look intimidating. Nerd kitty is here to put you at ease.     Let's break it down. First, the curly braces. This alerts AdWords not to treat this like straight text. ```{} ``` 
 
 If it's not text, what is it? We need to tell AdWords that this is an IF function: ```{=IF}``` Next we tell AdWords what the condition is:  ```{=IF(device=mobile)} ```
  
 Then we tell it what to do if the condition is true: ```{=IF(device=mobile, Free Shipping On Mobile Orders)}```
 
 And finally we tell it what to do if the condition isn't met: ```{=IF(device=mobile, Free Shipping On Mobile Orders): Buy Now}``` 
 
 Pretty easy, right? Now you're ready to hack your ads!

## How do I put the snippet inside an ad?

You place the snippet inside your ad just as you would any other text. For example, if you wrote your ad description like this:

``` Get The Best Shoes At The Best Price. {=IF(device=mobile, Free Shipping On Mobile Orders): Buy Now}```

 Your ad will appear on a mobile device, like this ![](https://adfury.io/wp-content/uploads/SNAG-0013-1-300x95.png) And on all other devices, like this ![](https://adfury.io/wp-content/uploads/SNAG-0014-1-300x79.png)

## Where can I place the snippet?

Anywhere you want except the final URL. This includes headline, description, even the display URL paths. Remember that rules still apply for character limit.

## Vary ad copy for a specific audience

An _audience_ is a list of users that you set up inside AdWords that share a characteristic. You can [learn more about audience lists from Google](https://support.google.com/adwords/editor/answer/1052569?hl=en). 

If you're new to audiences, Search Engine Land has a great article about some [things to keep in mind when setting up audiences](http://searchengineland.com/10-common-mistakes-setting-audiences-adwords-229858). For example, one audience might be made up of people that visited your website. Another audience might be made up of people that took a specific action, like made a purchase or downloaded a whitepaper.

The IF format is the same as with a mobile device, except this time the conditional is a list name. Let's say you maintain a list of people that have abandoned a cart on your site. You create a conditional with the curly snippet: ```{=IF}``` Add the user list ```{=IF(audience IN(Cart Abandoners)}``` Add text if the condition is true ```{=IF(audience IN(Cart Abandoners), 30%)}``` And add text if the condition is not true ```{=IF(audience IN(Cart Abandoners), 30%):20%}```

[This example from Google](https://support.google.com/adwords/answer/7207341), shows how the ad will display depending on whether the searcher has abandoned a cart.

 You can create a conditional that checks if the user is within one or more lists. For example ```{=IF(audience IN(Cart Abandoners, Product Viewers), 30%):20%}``` If the user is in either one of the groups, the condition will be true.

## When and why to use IF functions with audience lists

IF functions can be a way to engage customers appropriately depending on where they sit in the sales funnel. This can mean different things depending on whether you are running a lead generation campaign or a sales campaign.

### Lead generation

For lead generation campaigns the most common way to use audience lists in IF functions is to customize messages for people along the sales funnel. Many advertisers want to engage people that have never visited their web site differently vs. people that have made many visits and downloaded white papers.

### Sales and eCommerce

Most people don't make a purchase on the first visit to a site. 81% of hotel reservations are abandoned, with similar statistics for online carts. The good news is that adding an item or service to a cart reflects high _commercial intent._ It's an indication that this person is more likely than average to complete a sale. Using IF functions can provide that extra nudge with a larger discount or a benefit such as free shipping.

## A final note

Using IF functions with audience lists is powerful, but remember that an is only half a campaign. You can incrementally improve your AdWords performance through ad copy, but the impact will be limited without coordinated landing pages.
