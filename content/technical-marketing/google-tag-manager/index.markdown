---
title: Getting started with Google Tag Manager
author: Christopher Hoover
date: 2021-03-12
categories: [Marketing Analytics]
tags: ['Tag Manager']
description: |
  How to use Google Tag Manager to place snippets of code on a website.
---

Google Tag Manager makes it easy to place snippets of code, called **tags**, on a website or app without having to directly access the code of the website. Instead of asking an engineer to place multiple different tags on a site, the idea is to instead add a special tag container to your site. Every time someone visits your page, the container will check the Tag Manager website for any tags you put there. If it finds any, it'll load them on your site.

![GTM getting tags](GTMa.png)

Tags are often, not not exclusively, used to inform external tools such as Google Analytics about user behavior on the site. To understand how this works, we need to briefly talk about cookies, pixels, and events.

## Cookies
A "cookie" is a small text file that your browser gets from a website. When you first browse to a website, the server responds by sending both the site and any cookies it would like your browser to save.

![Set cookie](GTM1.png)

Your browser will save the cookie and associated it with the site. Any time you visit that site again, your browser will send along whatever data is in the cookie associated with that website.

![Send cookie](GTM2.png)

Cookies are especially useful for staying logged into websites. Let's say you log into Twitter. Your browses goes to the Twitter site and you log in. The Twitter server will generate a long string of text, called a session ID, which your browser will save as a cookie. From then on, every time you interact with Twitter your browser will send along the cookie with its session ID and Twitter will know who you are without needing you a log in. Without the cookie, you would have to log in every time you clicked anything on the site.

Cookies also help with tracking, even on sites that don't require a log in. By storing a random session ID in a cookie, you can track where a user goes in your site because the same ID will appear with every incoming request. You won't know who the person is, but you'll know where they went and you can start to map trends -- "People who read this blog post also tend to read this other post."

## Tracking pixels
Analytics tools such as Google Analytics use session IDs to build reports about how people interact with your site. For this to work you must somehow get your user's browser to interact with the Google Analytics server (and/or other third party servers) so that it can set a session ID. Some time ago, engineers invented a clever way to do this using image requests.

By referencing an image stored on a third party site, the browser had to make a request to that site to retrieve the image. That request enables a session ID to be set via a cookie. The image itself is tiny and transparent (a **pixel**), invisible to the user.

![Get pixel](GTM3.png)

These days tags use javascript snippets instead of actual pixels, but the name has stuck.

## Triggering event
Tags are always associated with a **triggering event**. What you are saying is "When **triggering event** happens, tell **tag** about it." For example, you can tell Tag Manager that "when a user **clicks on this button**, run the **Google Analytics** tag." Now, whenever that button is clicked, the event is registered in Google Analytics.

An event can be something the browser does, or something a user does. Common triggers include:

* When the page loads
* When the page has finished loading
* When someone downloads a report
* When someone scrolls more than 50% through a page
* When someone watches more than 50% of a video
* When someone submits a form
* Etc.

A comprehensive list of events that can be associated with a tag is available on the [MDN web docs site](https://developer.mozilla.org/en-US/docs/Web/Events).

## Setting up a Tag Manager account
To get started with Tag Manager, go to the Tag Manager website at [tagmanager.google.com](https://tagmanager.google.com/) and click "Create Account"

![Create GTM Account](CreateGTMAccount.png)

Fill out the simple form.

![](SetUpGTM.png)

You'll need to read and agree to the terms and conditions. Once you do that you'll be presented with the Tag Manager code.

![](InstallCode.png)

This is the only code you'll need to install on your site to support tags. Once it's installed, any tags you place in the Tag Manager website will be used on your site.
