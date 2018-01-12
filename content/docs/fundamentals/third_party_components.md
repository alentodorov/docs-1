---
$title: Include third-party content
$order: 3
$category: Develop
toc: true
components:
  - iframe
  - facebook
---
[TOC]


Learn how to include third-party components in your pages.

## Embed a Tweet

Embed a  Tweet from Twitter in your page by
using the [`amp-twitter`](/docs/reference/components/amp-twitter.html) element.

To embed a tweet in your page,
first include the following script in the `<head>`:

[sourcecode:html]
<script async custom-element="amp-twitter"
  src="https://cdn.ampproject.org/v0/amp-twitter-0.1.js"></script>
[/sourcecode]

Currently, tweets are automatically proportionally scaled
to fit the provided size,
but this may yield less than the ideal appearance.
Manually tweak the provided width and height or use the media attribute
to select the aspect ratio based on screen width.

<!-- embedded twitter example -->
<div>
<amp-iframe height="174"
            layout="fixed-height"
            sandbox="allow-scripts allow-forms allow-same-origin"
            resizable
            src="https://ampproject-b5f4c.firebaseapp.com/examples/thirdparty.twitter.embed.html">
  <div overflow tabindex="0" role="button" aria-label="Show more">Show full code</div>
  <div placeholder></div> 
</amp-iframe>
</div>

{% call callout('Tip', type='success') %}
See more `amp-twitter` examples at [AMP By Example](https://ampbyexample.com/components/amp-twitter/).
{% endcall %}


## Embed an Instagram

Embed an Instagram in your page by
using the [`amp-instagram`](/docs/reference/components/amp-instagram.html) element.

To embed an Instagram,
first include the following script in the `<head>`:

[sourcecode:html]
<script async custom-element="amp-instagram"
  src="https://cdn.ampproject.org/v0/amp-instagram-0.1.js"></script>
[/sourcecode]

Include the Instagram data-shortcode found in the Instagram photo URL.
For example, in `https://instagram.com/p/fBwFP`,
`fBwFP` is the data-shortcode.
Also, Instagram uses a fixed aspect ratio for responsive layouts,
so the value for width and height should be universal.

<!-- embedded Instagram example -->
<div>
<amp-iframe height="174"
            layout="fixed-height"
            sandbox="allow-scripts allow-forms allow-same-origin"
            resizable
            src="https://ampproject-b5f4c.firebaseapp.com/examples/thirdparty.instagram.embed.html">
  <div overflow tabindex="0" role="button" aria-label="Show more">Show full code</div>
  <div placeholder></div> 
</amp-iframe>
</div>

{% call callout('Tip', type='success') %}
See more `amp-instagram` examples at [AMP By Example](https://ampbyexample.com/components/amp-instagram/).
{% endcall %}

## Display a Facebook post or video

Display a Facebook post or video in your page by
using the [`amp-facebook`](/docs/reference/components/amp-facebook.html) element.

You must include the following script in the `<head>`:

[sourcecode:html]
<script async custom-element="amp-facebook"
  src="https://cdn.ampproject.org/v0/amp-facebook-0.1.js"></script>
[/sourcecode]

##### Example: Embedding a post

Source: 
```html
<amp-facebook width="486" height="657"
    layout="responsive"
    data-href="https://www.facebook.com/zuck/posts/10102593740125791">
</amp-facebook>
```
Preview: 
<amp-facebook width="486" height="657"
    layout="responsive"
    data-href="https://www.facebook.com/zuck/posts/10102593740125791">
</amp-facebook>

##### Example: Embedding a video

Source: 
```html
<amp-facebook width="476" height="316"
    layout="responsive"
    data-embed-as="video"
    data-href="https://www.facebook.com/nasaearth/videos/10155187938052139">
</amp-facebook>
```
Preview: 
<amp-facebook width="476" height="316"
    layout="responsive"
    data-embed-as="video"
    data-href="https://www.facebook.com/nasaearth/videos/10155187938052139">
</amp-facebook>

{% call callout('Tip', type='success') %}
See more `amp-facebook` examples at [AMP By Example](https://ampbyexample.com/components/amp-facebook/).
{% endcall %}

## Embed a YouTube video

Embed a YouTube video in your page by 
using the [`amp-youtube`](/docs/reference/components/amp-youtube.html) element.

You must include the following script in the `<head>`:

[sourcecode:html]
<script async custom-element="amp-youtube"
  src="https://cdn.ampproject.org/v0/amp-youtube-0.1.js"></script>
[/sourcecode]

The YouTube `data-videoid` can be found in every YouTube video page URL.
For example, in `https://www.youtube.com/watch?v=Z1q71gFeRqM`,
`Z1q71gFeRqM` is the video id.

Use `layout="responsive"` to yield correct layouts for 16:9 aspect ratio videos:

<!-- embedded youtube example -->
<div>
<amp-iframe height="174"
            layout="fixed-height"
            sandbox="allow-scripts allow-forms allow-same-origin"
            resizable
            src="https://ampproject-b5f4c.firebaseapp.com/examples/responsive.youtube.embed.html">
  <div overflow tabindex="0" role="button" aria-label="Show more">Show full code</div>
  <div placeholder></div> 
</amp-iframe>
</div>

{% call callout('Tip', type='success') %}
See more `amp-youtube` examples at [AMP By Example](https://ampbyexample.com/components/amp-youtube/).
{% endcall %}


## Display an ad

Display an ad in your page by 
using the [`amp-ad`](/docs/reference/components/amp-ad.html) element.
Only ads served via HTTPS are supported.

No ad network-provided JavaScript is allowed to run inside the AMP document.
Instead, the AMP runtime loads an iframe from a
different origin (via iframe sandbox)
and executes the ad network’s JS inside that iframe sandbox.

You must specify the ad width and height, and the ad network type.
The `type` identifies the ad network's template.
Different ad types require different `data-*` attributes.

<!-- embedded ad example -->
<div>
<amp-iframe height="212"
            layout="fixed-height"
            sandbox="allow-scripts allow-forms allow-same-origin"
            resizable
            src="https://ampproject-b5f4c.firebaseapp.com/examples/thirdparty.ad-basic.embed.html">
  <div overflow tabindex="0" role="button" aria-label="Show more">Show full code</div>
  <div placeholder></div> 
</amp-iframe>
</div>

If supported by the ad network,
include a `placeholder`
to be shown if no ad is available:

<!-- embedded ad example -->
<div>
<amp-iframe height="232"
            layout="fixed-height"
            sandbox="allow-scripts allow-forms allow-same-origin"
            resizable
            src="https://ampproject-b5f4c.firebaseapp.com/examples/thirdparty.ad-placeholder.embed.html">
  <div overflow tabindex="0" role="button" aria-label="Show more">Show full code</div>
  <div placeholder></div> 
</amp-iframe>
</div>

AMP supports a wide range of ad networks. See the [amp-ad reference documentation](/docs/reference/components/amp-ad.html#supported-ad-networks)  for a full list.

{% call callout('Read on', type='read') %}
Learn more about ads in the [Serving Ads on AMP](/docs/guides/ads_on_amp.html) guide.
{% endcall %}
