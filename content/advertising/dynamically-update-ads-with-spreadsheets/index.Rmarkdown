---
title: Dynamically update ads with spreadsheets
category: Marketing Analytics
author: Christopher Hoover
date: 2021-03-02
tags: ['Google Ads']
description: | 
  Dynamically insert data from a spreadsheet into your ad copy.
---

## What you'll learn in this post

This post will describe how to dynamically insert data from a spreadsheet into your ad copy. By updating the spreadsheet, you are updating the ads automatically.

- How to tell AdWords when to use spreadsheet data, and which data to use
- How to format the spreadsheet correctly
- How to write the ads that will be dynamically changed
- How to upload the whole thing into AdWords

## Super brief description of how customizers work

You first create a spreadsheet with the text you want to use in the ad (we'll go over what this spreadsheet looks like next). You create your ads. You upload the spreadsheet into Google Ads. When Google displays the ad, it will replace all the {snippets} with the text it finds in your spreadsheet.

Google has a [illustration of what this looks like](https://support.google.com/google-ads/answer/6072565#examples&zippy=%2Cyou-want-to-target-by-keyword) There's no restriction on how you use customizers as long as the ad does not violate Google's policies related to character limit or content. This gives you flexibility in delivering advertising that exactly matches what people are searching for.

## Define what you want to show

The first step is to create a data file in a spreadsheet. The text in this file is what Google will use to replace the {snippet}. The easiest way to get up to speed is [download the sample file](https://storage.googleapis.com/support-kms-prod/CC6B1FCD3EFA81DC3D5F68F20CF07E3DA6DB) that Google has made available.

## Decide at what level to customize

See the three columns on the right of the spread sheet? They are examples of _targeting attributes_, which is how you tell Google what row to use when customizing the ad. There's a bunch of targeting attributes you can use.

#### Target by campaign

Here's an example of your spreadsheet if you wanted to target campaigns. If the ad triggered is part of the East Coast campaign, then the data in row 2 will be used to create the ad. Remove the other targeting columns so Google doesn't get confused.   ![](https://blog.adfury.io/wp-content/uploads/customizer8.png)

#### Target by ad group

Here's an example of your spreadsheet if you wanted to target ad groups. Because the same ad group name can appear multiple campaigns, it's always a good idea to keep both the Target campaign and Target ad group columns. Remove the other targeting columns so Google doesn't get confused. Now Google shows an ad from the "ProWhip 300" ad group, it'll use the data from row 2.   ![](https://blog.adfury.io/wp-content/uploads/customizer6.png)   (Note: You don't have to place the terms "ad group" or "campaign" into your spreadsheet like the example shows. If the ad group is named "ProWhip 300," just use that. In the example below, the ad group is called "ProWhip 300 ad group," which seems a bit odd, but whatever.

#### Target by location

Here's an example of your spreadsheet if you wanted to target by location. If the user is located in or interested in the indicated area, Google will use the associated row. For example, if someone is in or searching about San Francisco, the ad will use data from column 2.   ![](https://blog.adfury.io/wp-content/uploads/customizer9.png)

#### Restricting location

You can restrict the targeting to people physically located in the indicated location. To do this, create a column called "Target location restriction" and write the words "Physical location" in it. In the example below, only people physically in Oakland will trigger row 3.   ![](https://blog.adfury.io/wp-content/uploads/customizer7.png)   The physical location restriction is optional. Leave the cell empty (as it is next to San Francisco) if you don't want to use the restriction and include people searching both **in** and **about** the location.

#### Target by keyword

Here's an example of your spreadsheet if you wanted to target by keyword. Notice that you need to indicate match type. ![](https://blog.adfury.io/wp-content/uploads/Customizer10.png) You can customize the same keyword across different campaigns by including the Target campaign column as well. In the example below, the folks seeing the West coast campaign are getting quite a deal compared to the folks in the East.   ![](https://blog.adfury.io/wp-content/uploads/Customizer11.png)

#### Alternate keyword format

Google supports a different format for keywords if you prefer, separating keyword and match type. This format doesn't do anything different vs. the other keyword format. Some folks have a preference because one or the other better matches their existing keyword spreadsheets.

## ![](https://blog.adfury.io/wp-content/uploads/Customizer12.png)

## Define your dynamic text

Once you've decided on a targeting method, you need to define how you are going to customize your ads. You'll notice in the spreadsheet example that all attributes are defined by two qualities: a **name** and a **type**. For example, the attribute in column A is named **Model** and is type **text**. You format the attribute exactly as shown; Attributename (Attributetype)

### Customized attributes

There are four attribute types: text, number, price, and date. These are all used in the example spreadsheet. ![](https://blog.adfury.io/wp-content/uploads/Customizer2.png)

- **Text**: Any letters, numbers, or symbols. Think product name, like "Beautiful Roses"
- **Number**: Any whole numbers. Used especially with inventory (remember to update the spreadsheet!)
- **Price**: Any number (including decimals) and valid currency characters
- **Date**: A date in the format yyyy/MM/dd hh:mm:ss

Note: the example spreadsheet provided by Google uses a different date format from that specified in the ad customizer official documentation. We suggest you use the yyyy/MM/dd format indicated above to be sure it'll work as expected.

### Limiter attributes

We call them "limiters." Google calls them "standard." Whatever you call them, they place limits on how the customizer is used.

- **Device preference**: If you want to limit a row of data to people searching with phones, create a column called "Device preference" with values of either **mobile** or **all**.  You can only limit to mobile; you can't limit to tablets or desktops.
- **Scheduling**: You can limit your customizer to run only during certain windows of time during the week. Create a column called "Scheduling" The format is Day, start time - end time, like this: Monday, 09:00 AM - 05:00 PM. You have to indicate each day you want to run, separated by a semicolon, like this: Monday, 09:00 AM - 05:00 PM; Tuesday, 09:00 AM - 05:00 PM. Multiple time windows can be similarly separated, like this: Monday, 09:00 AM - 10:00 AM; Monday, 02:00 PM - 05:00 PM
- **Start date**: When you'd like your customized ad to begin showing in format  yyyy/MM/dd hh:mm:ss
- **End date**: When you'd like your customized ad to stop showing in format yyyy/MM/dd hh:mm:ss

### And one for good luck

There's a final attribute you can use in your spreadsheet if you like. It's Custom ID, and you can use it to place a unique identifying value for a row of data. AdWords will create one automatically if you don't, but some people prefer the custom ID to make analysis a bit easier. You can use any combination of letters and numbers.

## How to write your ad with customizers

To use a customizer, insert it anywhere in the ad. When the ad runs, Google will swap out the data that it finds in the spreadsheet for the customizer. The format is {=DataSetName.AttributeName} where DataSetName is the name that you give the spreadsheet when you upload it into Google. For example, let's say that you were creating an ad for a flower shop. The ad will appear like this:

## ![](https://blog.adfury.io/wp-content/uploads/SNAG-0050.png)

You would start with a spreadsheet that looked something like this ![](https://blog.adfury.io/wp-content/uploads/SNAG-0048.png)   And your ad copy will look like this (when you upload your spreadsheet to Google, it'll ask for a name. For this example, let's say your named your file "SpringSale") **Headline 1:** Get {=SpringSale.Count} beautiful {=SpringSale.Flower} **Headline 2**: Just {=SpringSale.Start_price} for a limited time

## Upload your file into Google

To make any of this work, you have to place the spreadsheet with your customizer data into Google Sign in to your [AdWords](https://adwords.google.com/) account. Click **Shared library** on the left navigation bar ![](https://blog.adfury.io/wp-content/uploads/Customizer13.png) And choose **business data** ![](https://blog.adfury.io/wp-content/uploads/Customizer14.png) Click **+DATA** and choose the sort of data you’d like to add.   ![](https://blog.adfury.io/wp-content/uploads/Customizer15.png) Name your new data source. It’s best to use a short name without any spaces, and make sure not to re-use the name of an old data set or feed that you've removed. AdWords can only recognize new names. ![](https://blog.adfury.io/wp-content/uploads/SNAG-0055.png) Click **Browse for file** and choose the file you’d like to upload. Keep in mind that the size limit for .csv and .tsv files is 500MB and 50MB for other file types. Click **Upload**.
