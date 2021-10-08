> Scrub is a CSS framework that removes the headache of styling large applications.

## Quickstart

The quickest way to get started with Scrub is by using the CDN to include the following files:

```html
<!-- Scrub CSS -->
<link
  href="https://cdn.jsdelivr.net/npm/scrubcss@1.0.7/css-dist/main.min.css"
  rel="stylesheet"
/>

<!--
  Or,
  Use the following (no variables, supports IE11):
  <link href="https://cdn.jsdelivr.net/npm/scrubcss@1.0.7/css-dist/main.min.css" rel="stylesheet" />
-->
```

## Documentation

Scrub is built with a mobile-first approach. That means all your base styles should be applied for smaller screens, then should be updated accordingly as the screens get larger.

### Width & Height

Width and height are styled using their identifiers first, and then their size.

Identifiers: w = width, h = height, min-w = min-width, max-w = max-height, min-h = min-height, max-h = max-height. You can also you x or y for left-right & top-bottom identifiers. (ie. mx-20px (top-bottom))

Sizing:

- Pixels start at 25 and go in increments of 25 up to 500. (both width and height)
- Percents start at 5 and go in increments of 5 up to 100. (width) Height only uses the special sizes below.

Special Sizes for both:

```
"0": 0
"quarter": 25%
"half": 50%
"three-quarters": 75%
"full": 100%
"screen": 100vh (or vw for width)
```

These sizes also apply for max-width/height and min-width/height.

Example:

```html
<!-- width pixels -->
<div class="w-250px"></div>
<!-- width percents -->
<div class="w-35"></div>
<!-- max-width pixels -->
<div class="max-w-125px"></div>
<!-- min-width pixels -->
<div class="min-w-half"></div>
<!-- height pixels -->
<div class="h-250px"></div>
<!-- height percents -->
<div class="h-half"></div>
<!-- max-height pixels -->
<div class="max-h-75px"></div>
<!-- min-height pixels -->
<div class="min-h-quarter"></div>
```

### Margin & Padding

Margin and padding use the same naming convention as width and height, except they have directional identifiers as well.

Sizing:

- Sizing starts at 5px and goes up to 200px in increments of 5.

For example mr = margin-right, pl = padding-left, pt = padding-top, mb = margin-bottom, and ma or pa = all sides. You can also use the "auto" at the end for auto sizing.

Special Sizes:

```
"0": 0
"auto": auto (margin only)
"tiny": 2px
```

Example:

```html
<!-- margin right -->
<div class="mr-20px"></div>
<!-- padding top & bottom 10px -->
<div class="py-10px"></div>
<!-- margin top auto -->
<div class="mt-auto"></div>
<!-- padding bottom 0 -->
<div class="pb-0"></div>
```

With margin there is also specific names for the auto margins.

```html
<!-- margin top auto -->
<div class="push-top"></div>
<!-- margin bottom auto -->
<div class="push-bottom"></div>
<!-- margin right auto -->
<div class="push-right"></div>
<!-- margin left auto -->
<div class="push-left"></div>
```
