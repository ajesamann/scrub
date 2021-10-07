> Scrub is a CSS framework that removes the headache of styling large applications.

## Quickstart

The quickest way to get started with Scrub is by using the CDN to include the following files:

```html
<!-- Scrub CSS -->
<link
  href="https://cdn.jsdelivr.net/npm/scrubcss@1.0.6/css-dist/main.min.css"
  rel="stylesheet"
/>

<!--
  Or,
  Use the following (no variables, supports IE11):
  <link href="https://cdn.jsdelivr.net/npm/scrubcss@1.0.6/css-dist/main.min.css" rel="stylesheet" />
-->
```

### Documentation

Scrub is built with a mobile-first approach. That means all your base styles should be applied for smaller screens, then should be updated accordingly as the screens get larger.

#### Width & Height

Width and height are styled using their identifiers first, and then their size.

Identifiers: w = width, h = height

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

Example:

```html
<!-- width pixels -->
<div class="w-250px"></div>
<!-- width percents -->
<div class="w-35"></div>
<!-- height pixels -->
<div class="h-250px"></div>
<!-- height percents -->
<div class="h-half"></div>
```
