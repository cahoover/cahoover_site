---
title: Avoiding SPAM without CAPCHA
author: Christopher Hoover
date: 2021-03-01
tags: ['CRO']
description: A quick guide to avoding landing page spam without a capcha tool.
---
You've put together a beautiful landing page, and it's generating conversions for you like a well-oiled machine. All is humming along wonderfully except for one small fly in the ointment: spam. Bots are filling out your form, clogging up your CRM with spam, and making themselves a nuisance. What to do? The most common way to evade spambots is the CAPTCHA test. You know the ones; they try to get you to prove you're not a robot by typing in the letters and numbers seen in a distorted image.

More recent versions of CAPTCHA are a bit more sophisticated; they try to be less disruptive by tracking your mouse movements for telltale human swerves and bounces. !

But no matter how you present a test for humanness, one thing remains clear: they are a killer for conversions. A post by Moz's Casey Henry described [CAPTCHA's effect on conversion rates](https://moz.com/blog/captchasaffectonconversionrates) and found that turning off CAPTCHA increased conversions by 3.2%. Considering that you can often directly map conversions to revenue, you should take seriously any reduction in performance.

## The honeypot method: imperfect, but worth a try

The goto method for avoiding spam bots is to use a so-called "honeypot" field in the form. Such a field is hidden from humans, but completed by bots. Simply discard submissions with text in the hidden field, and you've reduced conversion spam.

## The traditional way to hide a field

The first thing to try is including a "type=hidden" in the input field. It's easy because it doesn't even require messing around with the CSS. For example:

```html
<input name="_" type="hidden" value="" autocomplete="off" tabindex="1" />
```

Amazingly, some spam robots still add text to this field! A very similar method uses the CSS style `{display: none;}`. Our friends at Wordstream [wrote about it](http://www.wordstream.com/blog/ws/2017/01/04/ppclandingpagetips), and there are [many similar articles](https://solutionfactor.net/blog/2014/02/01/honeypottechniquefasteasyspamprevention/) around the net. Often, this works just great. Sometimes it doesn't.

## Some bots aren't fooled

The problem with the type=hidden and {display:none;} techniques is that many modern bots are smart enough to avoid them. So what to do? Well, to begin with, make sure you give the type="hidden"  technique a try.  If you're still getting spam, try `{display:none;}`

Then try the related CSS visibility command.

```html
.odd_email{visibility: hidden}
<input class="odd_email" name="email_field" type="text" autocomplete="off" tabindex="1" />
```

These are the most straightforward methods, and they work for a lot of people. But if you're still getting spam, there are a few other options. All of them a riffs on the same theme: hide the field from humans, display it to bots.

## Move the field out of the way

You can try using CSS positioning to move the field out of the user's viewport. For example in your CSS

```html
.odd_email{position: absolute; top: 3px; left: 680px;}
<input class="odd_email" name="email_field" type="text" autocomplete="off" tabindex="1" />
```

## Make the field invisible

You can use CSS to make the field transparent to human viewers using the opacity property.

```html
.odd_email{opacity: 0;}
```

Note that the opacity value may not be supported by very old browsers. If this is a concern, be sure and test your field.

## Bury the field behind the z

The CSS `zindex` property defines where an element is located in the 3rd dimension (the z axis) relative to other layers. Define the main form fields with a positive z-index value, and then use a negative z-index value for the form that you wish to remain hidden.

```html
.odd_email{position:relative; zindex: 100}
```

## Indent the hidden field

The CSS text indent property specifies the indentation of the element. By providing a value of 100%, you are indenting the field to the far right side of the form element. By adding the overflow:hidden property, you hide the indented field. By adding the whitespace:nowrap property, you ensure the indented field doesn't leave an awkward space in your form.

```html
.odd_email{ textindent: 100%; whitespace: nowrap; overflow: hidden; }
<div class="odd_email"><input name="odd_email" type="text" autocomplete="off" tabindex="1" /></div>
```

## Be careful of autocomplete features

As you experiment with different techniques for hiding honeypot fields, you should be mindful that many browsers have autocomplete features that automatically fill out forms on behalf of their users. To make sure your honeypot isn't accidentally completed by a wellmeaning autocomplete bot, add autocomplete="off" to the honeypot's input tag.

## Be careful of tab indexing

Also, many people navigate through forms by clicking the tab button. You don't want them to tab to your hidden field and accidentally enter data.  To ensure the field isn't accessible by tab clicks, add  tabindex="1" to the input tag.

## Be careful of obvious labels

Some spam bots are programmed to watch for labels such as "honey," "honeypot," "spam" and similar variations. It's easiest to use some somewhat realistic but obviously fake name. I've used "odd_email" in the examples above.

## Please share

If you thought this post was useful or helpful, please share by clicking one of the social media buttons below!
