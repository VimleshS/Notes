# Media Queries

* [Mobile-first and old IE](http://jakearchibald.github.io/sass-ie/)
* [sass-mq](https://github.com/sass-mq/sass-mq)
* [@include-media](http://include-media.com/)
* [Managing responsive breakpoints](http://www.sitepoint.com/managing-responsive-breakpoints-sass/)
* [Advanced media queries](https://github.com/at-import/breakpoint/wiki/Advanced-Media-Queries#resolution-media-queries)

No more browser sniffing or separate m.example.com mobile version of your sites.

* Media Type - `screen`, `print`, `tv`
* Media Features - dimensions, resolution, colors, orientation

```
// Far too precise, exactly 600px
@media only screen and (width: 600px) {}
	
// 480px or narrower
@media only screen and (max-width: 480px) {}

// At least 640px wide (Mobile-First concept)
@media only screen and (min-width: 640px) {}
```
	
**Note**: There is no reason to use `device-width` as desktop browser don't typically use the full width of the monitor physical width like smartphone does.

## Content-Driven Breakpoints vs Device-Driven Breakpoints

## Resolution

1. IE hasn't implemented DPPX, so use DPI (1.5 * 96 = 144dpi)
2. Safari does not support `resolution`, use `-webkit-device-pixel-ratio`

```
@media (resolution: 1.5dppx), (resolution: 144dpi), (-webkit-device-pixel-ratio: 2) {}
```

* [Retina media queries](https://css-tricks.com/snippets/css/retina-display-media-query/)
* [iPhone 6 Screens Demystified](http://www.paintcodeapp.com/news/iphone-6-screens-demystified)
* [The iOS Design Guidelines](http://iosdesign.ivomynttinen.com/)
* [Starter's Guide to iOS Design](http://taybenlor.com/2013/05/21/designing-for-ios.html)

## Sass

Most of us started working with `@media` was adding blocks of them at the bottom of your main stylesheet. That works, but it leads to mental disconnect between the original styling and the responsive styles.

* [Responsive typography with chained media queries](https://bugsnag.com/blog/responsive-typography-with-chained-media-queries)

```scss
$default-browser-context: 16px !default;

@function em($target, $context: $default-browser-context) {
  @return $target / $context * 1em;}

$bp-medium: em(690px);

@mixin bp($breakpoint) {
  @if $breakpoint == medium {
    @media all and (min-width: $bp-medium) { @content; }  }}

.sidebar {
  background: #eee;
  
  @include bp(medium) {
    float: left;
    width: percentage(400px / 1280px);  }}
```
	
```scss
@mixin hidpi($media: all) {
  @media
    only #{$media} and (min--moz-device-pixel-ratio: 1.5),
    only #{$media} and (-o-min-device-pixel-ratio: 3/2),
    only #{$media} and (-webkit-min-device-pixel-ratio: 1.5),
    only #{$media} and (min-device-pixel-ratio: 1.5),
    only #{$media} and (min-resolution: 144dpi),
    only #{$media} and (min-resolution: 1.5dppx) {
      @content;    }}
```