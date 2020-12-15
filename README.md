# Ornate CSS

**May your designs be Ornate, and your code be simple.**

## Utility powered, mobile responsive, grid based CSS framework.

Highly inspired by other frameworks like Tailwind css, and Bulma Ornate CSS and built using
[Gaudiamus](https://gaudiamus-css.github.io/) allows developers and designers to accomplish complicated web designs
while you're writing your HTML. Whether you want to design using Ornate CSS' out-of-the-box solutions, or expand the
utilities to fit your projects, Ornate empowers your decision while remaining light and non-invasive.

[Installation](#installation)

[Basic Usage](#basicUsage)

### <a name="installation"></a> Installation

The recommended way of using Ornate is downloading it via the npm:

` npm i ornate_css `

### <a name="basicUsage"></a> Basic Usage

Include "ornate_css/scss/index.scss" into your own .sass or .scss file.

```scss
//import Ornate css

@import "./node_modules/ornate_css/scss/index.scss
```

Built directly into OrnateCSS is [normalize.css](https://necolas.github.io/normalize.css/), a css file that essentially
resets a browsers default styling and forces uniformity for reliable consistency when styling your site.

Normalize is definitely the recommended css reset of its kind. Regardless, use whatever you like as long as you have a
reset of some sort.

Ornate has a plethora of utility classes. The majority of which follow this simple formula for ease of memorization:

```scss
//name of property - side -unit number


// Example
// border - bottom - 1px - solid
.b-b-1-solid
  // margin - top - 1em
.m-t-1
  // margin - top & bottom - 1em
.m-y-1
```

As you see you can see, when setting properties you can choose to set a side or not.

```scss
// Affect the entire border
// border - 1px - solid
.b-1-solid
  // margin - 3em
.m-3
  // Y axis e.g.: top and bottom
.m-y-2
  // X axis e.g.: left and right
.m-x-2

```

One can even review the above and notice a pattern when wit comes to declaring properties. Knowing that
"m" stands for margin, you can then assume tha "p" stands for padding.

### The Grid System

Being powered by [Gaudiamus](https://gaudiamus-css.github.io/), Ornate also uses CSS Grid. The grid system is now easier
to implement.

By default, we use the common 12-grid.

```html

<div class="grid-4-4-4">
  <div>child1</div>
  <div>child2</div>
  <div>child3</div>
</div>
```

Any Combination is possible:

```html

<div class="grid-7-5">
  <div>
    <div class="grid-6-6">
      <div>one-1</div>
      <div>one-2</div>
    </div>
  </div>
  <div>two</div>
</div>
```

### Placement

You can place elements on the x and y-axis of the grid-area with ease:

```html

<div class="grid-3-3-3-3">
  <span class="place-x-center">1</span>
  <span class="place-x-end">2</span>
  <span class="place-y-start">3</span>
  <span class="place-y-stretch">4</span>
</div>

```

### Responsiveness

What about breakpoints? We use a markup similar to tailwind css to tackle this. However, now the grid really starts to
make the difference. Finally, you will have an overview of your breakpoints. Start with mobile and go up:
(here is makes sense to play around with your window-size if you can)

"xs": 320px,
"sm": 425px,
"md": 768px,
"lg": 1024px,
"xl": 1440px,
"xxl": 2560px,
"xxxl":3440px

```html

<div class="grid-12 md:grid-6-6 lg:grid-3-3-3-3">
  <div>1</div>
  <div>2</div>
  <div>3</div>
  <div>4</div>
</div>
```

Responsiveness in Ornate allows you to adhoc allow different pre-built classes to be active at different breakpoints.

## Pre-Built Utility Classes

There are two types of Utilities:

1. Dashed utilities

   The most common and typically in the following format: **.m-t-2**
2. Colon Utilities

   Represent a condition that is met before being used. An example of this would be responsive utilities: "xs:", "sm:"
   , "md:", "lg:", "xl:", "xxl:", "xxxl:"

   Meanwhile, the others represent a specific state. Such as focus, hover, and active.

In addition, there are default values that help support all the utilities.

```scss
$baseSpacing20
px

$spacingUnitrem

$spacingStep.25

$numSpacingUnits5

$shorthand-map: (
  "t":"top",
  "b":"bottom",
  "r":"right",
  "l":"left",
  "x":(1:"left", 2:"right"),
  "y":(1:"top", 2:"bottom"));

$property-map: ("m":"margin", "p":"padding");
```

### Colors:

Colors can be added to a background, borders or text.

```scss
/* Colors */
$primaryColor: #3F51B5;
$accentColor: #ff5252;
$successColor: #4caf50;
$warningColor: #FF9800;
$dangerColor: #c92d2d;
$gray: rgba(0, 0, 0, .2);
$white: #e8e5e5;
$black: #101010;

/* Light version */
$lightPrimaryColor: #C5CAE9;
$lightAccentColor: #FFCDD2;
$lightSuccessColor: #C8E6C9;
$lightWarningColor: #FFE0B2;
$lightDangerColor: #f44336;

/* Dark version */
$darkPrimaryColor: #303F9F;
$darkAccentColor: #D32F2F;
$darkSuccessColor: #388E3C;
$darkWarningColor: #F57C00;
$darkDangerColor: #b71c1c;

```

## Dashed Utilities

### Layout

**Container**

Container sets an element for setting the width to 100% and centering.

```scss
.container {
  max-width: calc(100% - 20px);
  margin: $baseSpacing auto;
}
```

****

**Position**

```scss
.position-relative
.position-absolute
.position-fixed
```

****

**Visibility**

```scss
// Display: none
.hide
  // Display: block
.display
```

****
**z-index**

```scss
/* Z-Index */
$z-index-map: (
  "0":0,
  "10":10,
  "20":20,
  "30":30,
  "40":40,
  "50":50,
  "auto":"auto"
);

.z-0
.z-10
.z-20
.z-30
.z-40
.z-50
.z-auto
```

****

### Typography

**Font Family**

```scss
// font-family: ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, "Noto Sans", sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";
.font-sans
  // font-family: ui-serif, Georgia, Cambria, "Times New Roman", Times, serif;
.font-serif
  // font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
.font-mono
```

**Font Size**

```scss
.font-sm
.font-default
.font-md
.font-lg
.font-xl
.font-xxl
```

**Text Transformation, Decorations, Overflow, Align**

```scss

// Transformations
.uppercase
.lowercase
.capitalize
.normal-case
  //Decorations
.underlined
.overline
.lineThrough
.none
  //Overflow
.overflow
.text-overflow
.overflow-clip
.text-decoration-none
  //Align
.text-right
.text-center
.text-left
.text-justify
```

****
**Padding**

```scss
.p-1
.p-2
.p-3
.p-4
.p-5
.p-x-1
.p-t-2
.p-r-3
.p-b-4
.p-l-5
.p-y-1
.p-t-2
.p-r-3
.p-b-4
.p-l-5

```

**Margin**

```scss
.m-1
.m-2
.m-3
.m-4
.m-5
.m-x-1
.m-t-2
.m-r-3
.m-b-4
.m-l-5
.m-t-1
.m-r-2
.m-b-3
.m-l-4

```

****

### Sizing

Sizing comes in two flavors:

1. Percentage

```scss
.w-25p
```

2. REM unit

```scss
.h //height
.w //width
  //example
.h-10

$height-width-scale: (
  0: 0px,
  1: 0.25rem,
  2: 0.5rem,
  3: 0.75rem,
  4: 1rem,
  5: 1.25rem,
  6: 1.5rem,
  7: 1.75rem,
  8: 2rem,
  9: 2.25rem,
  10: 2.5rem,
  11: 2.75rem,
  12: 3rem,
  14: 3.5rem,
  16: 4rem,
  20: 5rem,
  24: 6rem,
  28: 7rem,
  32: 8rem,
  36: 9rem,
  40: 10rem,
  44: 11rem,
  48: 12rem,
  52: 13rem,
  56: 14rem,
  60: 15rem,
  64: 16rem,
  72: 18rem,
  80: 20rem,
  96: 24rem,
  auto: auto
);
```

****

### Borders

```scss
// rounds the corners of a border
.b-rounded
  // border - px line width - border style
.b-1-solid // Outputs border with a solid 1px width
  // You can even determine what border sides
.b-b-1-solid // Outputs border with a solid 1px width that is on the bottom
  // In order to color a border you can simply use the following syntax
  // with any color:
.b-black
```

**Border Decorations**

```scss
.b-1-wave
.b-1-solid
.b-1-double
.b-1-dotted
.b-1-dashed
```

****

### Effects

**Shadowing**

```scss
.raise-1-[[color]

]
.raise-2-black
.raise-3-primary
```

**Opacity**

```scss
.opacity-25 // 0.25
.opacity-50 // 0.50
.opacity-75 // 0.75
.opacity-100

// 1
```

**Cursor**

```scss
.cursor-auto
.cursor-default
.cursor-pointer
.cursor-wait
.cursor-text
.cursor-move
.cursor-not-allowed
```

**User-select**

```scss
.select-none
.select-text
.select-all
.select-auto
```

****

### SVG

Much like Tailwind you can style svg's that primarily use path as it's main attribute. I suggest
using [zondicons](http://www.zondicons.com/)

```scss
  .fill-svg {
  fill: currentColor;
}

.stroke-svg {
  stroke: currentColor;
}

// TO color  after using either fill-svg or stroke-svg use text coloring
.fill-svg .text-primary
```

****

## Compositions

As alluded to before, compositions are pre-made classes made to style commonly used elements.

**Box**
As it sounds, .box is a simple class that wraps the element in a borderless container. The said container has a drop
shadow.

```scss
// box - level - color
.box-low-primary
.box-med-primary
.box-low-primary
```

****

**Button**
Primarily there are three types of buttons:

1. Regular
2. Line
3. Fab

```scss
.btn {
  @extend .b-rounded, .font-md, .b-gray, .b-1-solid, .uppercase, .m-2, .cursor-pointer, .font-sans,
  .font-strong;
  // .btn-[color] is a flat button tha is colored.
  // btn - color
  .btn-primary
}

// btn - line - color
.btn-line-primary
```

**Fab button**

```scss
.btn-fab
  //btn - fab - color
.btn-fab-primary
```

**Round Button**

```scss
.btn-round
  //btn - round - line (which is by default solid ) - color
.btn-round-line-primary
  //btn - round - color
.btn-round-primary
```

****

## Input forms

**Label**

Label styling is very simple.

```scss
  .label {
  @extend .font-strong, .font-sans;
}
```

**Input**

```scss
.input {
  @extend .b-rounded, .b-b-1-solid, .b-gray, .bg-gray, .opacity-75, .b-l-none, .b-r-none, .b-t-none,
  .focus\:b-b-2-solid, .focus\:b-black, .bg-white, .font-sans, .m-y-2, .p-t-2,
  .focus\:raise-1-gray, .p-x-1;
}
// input - color
.input-primary

.input-rounded {
  border-radius: 16px;
  @extend .b-b-1-solid, .b-gray, .bg-gray, .opacity-75, .b-l-none, .b-r-none, .b-t-none,
  .focus\:b-b-2-solid, .focus\:b-black, .bg-white, .font-sans, .m-y-2, .p-t-2,
  .focus\:raise-1-gray, .p-x-2;
}

// input - rounded - color
.input-rounded-primary
```

**Input & Textarea Disabled/ read-only**
```scss
    input:disabled,
    textarea:read-only {
      @extend .cursor-not-allowed, .opacity-100, .bg-gray;
    }

    input:read-only,
    textarea:read-only {
      @extend .cursor-text, .opacity-100, .bg-gray;
    }
```

**Textarea**
```scss
    .textarea {
      @extend .focus\:raise-1-gray, .b-1-solid, .b-gray, .b-rounded;
    }

    //textarea - color
    .textarea-primary
```

**Drop-down/ Select**
```scss
    .select {
      @extend .bg-white, .font-sans, .b-rounded;

      option:nth-child(2n+1) {
        @extend .bg-white, .opacity-50;
      }
    }

  // select - color
  .select-primary

  .select-alt {
    @extend .b-white, .b-1-solid, .opacity-75, .font-sans, .b-rounded;
  }

  // select - alt - primary
  .select-alt-primary
```
