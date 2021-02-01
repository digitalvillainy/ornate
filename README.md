# Ornate CSS

**May your designs be Ornate, and your code be simple.**

## Utility powered, mobile responsive, grid based CSS framework.

Highly inspired by other frameworks like Tailwind css, and Bulma Ornate CSS and built using
[Gaudiamus](https://gaudiamus-css.github.io/) allows developers and designers to accomplish complicated web designs
while you're writing your HTML. Whether you want to design using Ornate CSS' out-of-the-box solutions, or expand the
utilities to fit your projects, Ornate empowers your decision while remaining light and non-invasive.


### <a name="installation"></a> Installation
Visit the official [Ornate CSS](https://ornatecss.com) site for the full documentation.

The recommended way of using Ornate is downloading it via the npm:

` npm i ornate_css `

### <a name="basicUsage"></a> Basic Usage

Include "ornate_css/scss/index.scss" into your own .sass or .scss file.

[![](https://data.jsdelivr.com/v1/package/npm/ornate_css/badge)](https://www.jsdelivr.com/package/npm/ornate_css)

```scss
//import Ornate css

@import "./node_modules/ornate_css/scss.12ba3e41.css

```
### use a CDN
https://cdn.jsdelivr.net/npm/ornate_css@0.2.2/scss.12ba3e41.min.css

Built directly into OrnateCSS is [normalize.css](https://necolas.github.io/normalize.css/), a css file that essentially
resets a browsers default styling and forces uniformity for reliable consistency when styling your site.

Normalize is definitely the recommended css reset of its kind. Regardless, use whatever you like as long as you have a
reset of some sort.

There are some custom resets built into Ornate CSS:
```scss
  a,
  a:visited,
  a:link,
  a:active {
    border-bottom: 0 solid;
    @extend .text-decoration-none, .text-black;
  }

  ul,
  ol {
    @extend .list-style-none;
  }

  h1,
  h2,
  h3,
  h4,
  h5 {
    margin: 0;
  }
}
```

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

### <a name="the-grid-system"></a> The Grid System

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

# Thank you!

Thank you for using Ornate CSS, if you have problems or would like to contribute
please reach out through email rrivera@redbannermedia.com
