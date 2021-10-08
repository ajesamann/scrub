> Scrub is a CSS framework that removes the headache of styling large applications.

## Quickstart

The quickest way to get started with Scrub is by using the CDN to include the following files:

```html
<!-- Scrub CSS -->
<link
  href="https://cdn.jsdelivr.net/npm/scrubcss@1.1.0/css-dist/main.min.css"
  rel="stylesheet"
/>

<!--
  Or,
  Use the following (no variables, supports IE11):
  <link href="https://cdn.jsdelivr.net/npm/scrubcss@1.1.0/css-dist/main.min.css" rel="stylesheet" />
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

Special sizes for both:

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

For example mr = margin-right, pl = padding-left, pt = padding-top, mb = margin-bottom, and ma or pa = all sides. You can also use "auto" at the end for auto sizing.

Special sizes:

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

### Text

The identifier for text is literally text.

Sizes:

```
"tiny": 10px
"xs": 12px
"sm": 14px
"md": 16px
"lg": 18px
"xl": 20px
"2xl": 22px
"3xl": 24px
"4xl": 26px
"5xl": 28px
"6xl": 30px
```

Example:

```html
<!-- font will be 22px -->
<div class="text-2xl"></div>
<!-- font will be 10px -->
<div class="text-tiny"></div>
```

To alter text color, just use the identifier then the name of the color as the suffix.

Example:

```html
<!-- black text color -->
<div class="text-black"></div>
```

To add text styles, just use the name of the style you're looking for.

```
italic
bold
underline
decoration-off
```

### Flex

Scrub offers premade flex containers. The naming convention for these is like so - nameOfLayout-directionOfFlex. (column or row)

Layout class names:

```
center-<direction>
top-<direction>
bottom-<direction>
left-<direction>
right-<direction>
between-<direction>
around-<direction>
evenly-<direction>
```

Let's look at some examples.

```html
<!-- This container will move all children to the center of the column -->
<div class="center-column">
  <!-- children -->
  <div></div>
  <div></div>
  <div></div>
</div>

<!-- This container will move all children to the left of the column -->
<div class="left-column">
  <!-- children -->
  <div></div>
  <div></div>
  <div></div>
</div>

<!-- This container will spread all children evenly throughout the row -->
<div class="evenly-row">
  <!-- children -->
  <div></div>
  <div></div>
  <div></div>
</div>

<!-- This container will spread all children as much as possible throughout the row -->
<div class="between-row">
  <!-- children -->
  <div></div>
  <div></div>
  <div></div>
</div>
```

You can also create your own flex containers. Easily control your container if you don't want to use the premade ones.

Values for alignment:

```
"center": center
"start": flex-start
"end": flex-end
"between": space-between
"around": space-around (justify-content only)
"evenly": space-evenly
"stretch": stretch (align-items only)
```

```html
<!-- just use f-<name of direction> then j for justify-content, a for align-items and a value for alignment -->
<div class="f-column j-start a-center">
  <!-- children -->
  <div></div>
  <div></div>
  <div></div>
</div>
```

Flex wrap options can be toggled with "wrap-on/off".

### Flex Children

Align self values:

```
"center": center
"start": start
"end": end
"f-start": flex-start
"f-end": flex-end
"base": baseline
"stretch": stretch
```

Align self example:

```html
<div class="center-row">
  <div></div>
  <!-- align self to flex end -->
  <div class="self-a-f-end"></div>
  <div></div>
</div>
```

Grow and shrink work the same way. Simply use the word grow or shrink, then an integer 0-5.
For example grow-3 or shrink-0.

Flex basis values:

```
"auto": auto
"25": 25%
"33": 33%
"50": 50%
"100": 100%
```

Just simply use "basis-25" or whatever value you wish to use.

### Background colors

Backgrounds are simple.

"bg-(name of color)"

### Border

Adding a border consists of providing the size of the border and the color.

Border size values:

```
"tiny": 1px
"sm": 2px
"md": 3px
"lg": 4px
```

Example:

```html
<!-- border around whole element, black color -->
<div class="border-tiny-black"></div>
```

Naming convention for border radius:

Values: top, bottom, left, right

```
- All corners
round-(size)

- Specific corner
round-(y value)-(x value)-(size)
```

Border radius values:

```
"sm": 10px
"md": 25px
"lg": 50px
```

```html
<!-- border radius all corners, 50px -->
<div class="round-lg"></div>
<!-- border radius top right only, 10px -->
<div class="round-top-right-sm"></div>
```

### Shadows

Shadow classes:

```
shadow-sm
shadow-md
shadow-lg
```

### Shapes

Scrub offers currently squares and circles. The pixel sizes are the same on all sides, and work in increments of 25 up to 500.

For declaring a shape, just use the name of the shape, then the size.

Examples:

```html
<!-- circles -->
<div class="circle-125px"></div>
<!-- squares -->
<div class="square-450px"></div>
```

### Positioning

If you need to use absolute positioning, scrub has you covered. Just use "abs" for absolute, or "rel" for relative.

We also have a premade centering class for absolute elements. Use "center-abs" to center absolute elements.

To control a absolute element, grab it with it's axis identifier, (top, bottom, left, right) then use a value 0-250 (pixels).

Example:

```html
<div class="abs top-0 right-35"></div>
```

### Dividers

Dividers are declared using their horizontal or vertical identifiers, then the size of the divider.

Divider size values for horizontal and vertical:

```
"5px": 5px
"10px": 10px
"15px": 15px
"20px": 20px
"25px": 25px
"30px": 30px
"35px": 35px
"40px": 40px
"45px": 45px
"50px": 50px
"quarter": 25%
"half": 50%
"three-quarters": 75%
"full": 100%
"screen": (100vw for horizontal) (100vh for vertical)
```

Dividers us sm, md, and lg to determine the thickness of the actual divider. The last value given is either the width or the height depending on the divider type. You can use "none" at the end to give it your own width.

Let's look at some examples:

```html
<!-- vertical divider - small thickness - 100% width -->
<div class="v-divider-sm-full"></div>
<!-- horizontal divider - large thickness - 25 pixel width -->
<div class="h-divider-lg-25px"></div>
```

### Components

Currently there are only two premade components in Scrub.

Buttons and chips. All you have to do is call the component name and then how round you want the corners.

Values:

```
"rectangle"
"round-sm"
"round-md"
"round-full"
```

Examples:

```html
<!-- completely rounded button -->
<div class="btn-round-full"></div>
<!-- no border radius button -->
<div class="btn-rectangle"></div>
<!-- small border radius chip -->
<div class="chip-round-sm"></div>
```

### Inputs

Inputs are styled by our default input styling.

We haven't incorporated any control of inputs yet, but the defaults look alot better than htmls default inputs.

### Media Queries (responsive styling)

Scrub takes a very simple and widely used approach when it comes to responsive styling. You must style for mobile first. To activate a media query on a style just apply md?(name of class) or lg?(name of class).

Let's dive deeper.

Breakpoint values:

```
"md": 960px
"lg": 1280px
```

Say we want our div below to have 50% width on mobile, 100% width on small tablets, and 75% width on desktops. Every screen size above your identifier will take the current queries styles, unless a new query takes over.

```html
<div class="w-50 md?w-100 lg?w-75"></div>
```

These classes do not have to be in order, but notice how we applied the identifiers. Most all classes support this convention in Scrub.

### Misc Classes

```
"max": take full width and height of parent
"max-screen": take full width and height of screen
"smooth-on": smoothly transition element styles
"smooth-off": turn off smooth transitions
"clickable": show cursor on hover
"border-box": apply box-sizing border-box
```

Happy styling!
