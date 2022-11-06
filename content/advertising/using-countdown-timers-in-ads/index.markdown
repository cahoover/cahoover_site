---
title: Using countdown timers in ads
categories: [Advertising]
author: Christopher Hoover
date: 2021-03-02
tags: ['Google Ads']
description: | 
  How write an ad that includes a countdown toward a special event, such as the end of a registration period..
---
When it comes to powerful-but-overlooked capabilities built into Google Ads, ad customization is right there at the top of the list. It's a really cool feature that lets you automatically adapt your ad copy to match the context of the searcher. There are many different kind of ad customization options, but in this post will focus on only one - the countdown.

## What you'll learn in this post

This post will describe how write an ad that includes a countdown toward a special event, such as the end of a registration period.

- What the countdown looks like and how they can be helpful
- How to insert them into your ads

## Introduction

Imagine you have an event that you want to run a countdown toward.  You can build an ad that automatically reflects the remaining time available, first in days and then in hours and minutes as the deadline approaches. Check out the last line in this ad. ![ad countdown](/img/google-ads/fakead_countdown.png) See the "2 days" bit? Cool, huh? It counts down automatically toward a date you specify, relative to the time zone of the searcher.

A countdown like this is useful in all kinds of situations. Perhaps you're running a sale that's ending soon. Or you're a real estate agent with a home that takes bids at the end of the week. Maybe there's a registration deadline, or a meet-and-greet happening. To make this happen, you insert the following code into your ad

```
{=COUNTDOWN("YEAR/MO/DY 09:00:00”)}
```
I used bold font for emphasis. To make it stand out. You don't have to use a bold font in your ad. Not that you would. But somebody will, unless I add this sentence.

Oh, the time. I better mention the time. The example snippet above has 09:00:00 as a stop time. That's 9am. You'll want to use your actual stop time, in 24 hour (sometimes called military) format. Don't write 09:00:00pm. Write 21:00:00. For example, if the countdown ends on September 21 at five in the afternoon, you'd write the last line in your ad like this: 

```
Hurry! Deadline for fall registration is in {=COUNTDOWN("2017/09/21 17:00:00”)}
```
 Which renders in the ad like the image above. Isn't that easy? A couple more details.

## Add countdown variables

You can add variables to cause the countdown to appear only for a specific language, and you can specify when you would like the countdown to appear.

In the following example, the countdown will appear only for Spanish language searches beginning three days before the date specified (i.e. if the event is 4 days away, the ad won't serve): ```{=COUNTDOWN("YEAR/MO/DY 09:00:00", 'es',  3)}```

The default language is US-EN. You can keep this default and specify a beginning time by leaving the language space blank, like this: ```{=COUNTDOWN("YEAR/MO/DY 09:00:00", ,  3)}``` The computer uses the commas to determine which variable is which, so be sure and use this format exactly as shown.

One more thing. By default, the countdown reflects the time zone of the searcher. For example, the timer might expire for someone searching on the East coast but still be active for searchers on the West coast. If you'd like the time to be the same for everyone, you can base the countdown on the the time zone of the account by using GLOBAL_COUNTDOWN, like this: ```{=GLOBAL_COUNTDOWN("YEAR/MO/DY 09:00:00", ,  3)}``` Which would show the same amount of time remaining to anyone searching in US English, beginning three days before the specified date, regardless of their time zone.

## Some important notes

Okay here are additional details you need to be aware of. About which you need to be aware. Whatever.

- **You gotta have a regular ad.** If you are using a customization in an ad, Google requires that you have another ad in the same ad group that doesn't have a customization.
- **Character limit still applies.**  If you decide to include a countdown in your text ad description, be sure and account for the characters inserted by the counter. If you go outside your character limit when the counter is inserted, the ad will be disapproved.
- **If the countdown isn't active, neither is your ad.** When your countdown timer expires, your ad stops running. If you've set your time to start three days before a date, the ad won't run four days before. I mention this because some people think same ad will continue to run, just without the customization. It won't.
