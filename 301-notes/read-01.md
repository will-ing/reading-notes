# SMACSS and Responsive Web Design

## Responsive vs Adaptive vs Mobile

Type | Definition
---- | ----
Responsive | to react quickly and positively to any change
Adaptive | to be easily modified for a new purpose or situation, such as change
Mobile | to build a separate website commonly on a new domain solely for mobile users

# Responsive Web Design

> Responsive web design is broken down into three main components, including **flexible layouts**, **media queries**, and **flexible media**.

> Flexible grids are built using relative length units, most commonly **percentages** or **em** units. 

### Relative view port lengths

Type | Definition
---- | ----
vw | Viewports width
vh | Viewports height
vmin | Minimum of the viewport’s height and width
vmax | Maximum of the viewport’s height and width

**Media queries** - provide the ability to specify different styles for individual browser and device circumstances, the width of the viewport or device orientation for example. 

> There are three different logical operators available for use within media queries, including **and**, **not**, and **only**.

```css
@media all and (min-width: 800px) and (max-width: 1024px) {...}
@media not screen and (color) {...}
@media only screen and (orientation: portrait) {...}

```

#### Height & Width Media Features

```css
@media all and (min-width: 320px) and (max-width: 780px) {...}
```

#### Orientation Media Feature

```css
@media all and (orientation: landscape) {...}
```

#### Aspect Ratio Media Features

```css
@media all and (min-device-aspect-ratio: 16/9) {...}
```

#### Resolution Media Feature

```css
@media print and (min-resolution: 300dpi) {...}
```

### Mobile First

> The operating belief behind mobile first design is that a user on a mobile device, commonly using a smaller viewport, shouldn’t have to load the styles for a desktop computer only to have them over written with mobile styles later. Doing so is a waste of bandwidth.

#### Mobile first example

```css
/* Default styles first then media queries */
@media screen and (min-width: 400px)  {...}
@media screen and (min-width: 600px)  {...}
@media screen and (min-width: 1000px) {...}
@media screen and (min-width: 1400px) {...}
```

> avoiding CSS3 shadows, gradients, transforms, and animations within mobile styles isn’t a bad idea either. When used excessively, they cause heavy loading and can even reduce a device’s battery life.

#### Viewport meta tag

```html
<meta name="viewport" content="width=device-width">
```

#### Types of viewport scale

1. minimum-scale
1. maximum-scale
1. initial-scale
1. user-scalable properties

```html
<meta name="viewport" content="initial-scale=2">

 <!-- minimum-scale the value should be a positive integer lower than or equal to the initial-scale. -->
<meta name="viewport" content="minimum-scale=0">

<!-- setting the user-scalable value to yes will turn on zooming. -->
<meta name="viewport" content="user-scalable=yes">

<!-- Viewport Resolution -->
<meta name="viewport" content="target-densitydpi=device-dpi">

<!-- Combining Viewport Values -->
<meta name="viewport" content="width=device-width, initial-scale=1">
```

## Flexible Media

> One quick way to make media scalable is by using the max-width property with a value of 100%.

```css
img, video, canvas {
  max-width: 100%;
}
```

> To get embedded media to be fully responsive, the embedded element needs to be absolutely positioned within a parent element.

## Floats

### Problems with Floats

**Pushdown** - is a symptom of an element inside a floated item being wider than the float itself (typically an image). *To fix this* use overflow: hidden to cut off excess.

# SMACSS 

>is a way to examine your design process and as a way to fit those rigid frameworks into a flexible thought process.

### Categorizing CSS Rules

CSS categories -

Type | Definition
---- | ----
Base rules | wherever this element is on the page, it should look like this. Includes attribute selectors, pseudo-class selectors, child selectors or sibling selectors.
Layout rules | divide the page into sections. Layouts hold one or more modules together.
Modules | are the reusable, modular parts of our design. They are the callouts, the sidebar sections, the product lists and so on.
State rules | are ways to describe how our modules or layouts will look when in a particular state. Is it hidden or expanded? Is it active or inactive? They are about describing how a module or layout looks on screens that are smaller or bigger. They are also about describing how a module might look in different views like the home page or the inside page.
Theme rules | are similar to state rules in that they describe how modules or layouts might look. Most sites don’t require a layer of theming but it is good to be aware of it.



 src="https://code.jquery.com/jquery-3.1.1.js"

 sudo service postgresql start

[Main Page](https://will-ing.github.io/reading-notes301/)