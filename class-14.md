# CSS Transforms, Transitions, and Animations


type | description
---- | ----
`transform` | The value specifies the transform type followed by a specific amount inside parentheses.

```css
div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}
```

*the `transform` property includes multiple vendor prefixes to gain the best support across all browsers.*

type | description
---- | ----
`rotate` | provides the ability to rotate an element from 0 to 360 degrees.
`scale` | property allows you to change the appeared size of an element. 
`translate` | works a bit like that of relative positioning, pushing and pulling an element in different directions
`skew` | s used to distort elements on the horizontal axis, vertical axis, or both.

```css
.box-1 {
  transform: rotate(20deg);
}

.box-1 {
  transform: scale(.75);
}

.box-1 {
  transform: translateX(-10px);
}
```

type | description
---- | ----
`perspective`  | The perspective for each element can be thought of as a vanishing point, similar to that which can be seen in three-dimensional drawings.
`scale2` | three-dimensional transform elements may be scaled on the z axis.
`backface-visibility` | hree-dimensional transforms, elements will occasionally be transformed in a way that causes them to face away from the screen. `none` property takes even more significance when using animations.

```html
<div class="group">
  <figure class="box">Box 1</figure>
  <figure class="box">Box 2</figure>
  <figure class="box">Box 3</figure>
</div>
```


```css
.group {
  perspective: 200px;
}
.box {
  transform: rotateX(45deg);
}

.box-1 {
  transform: perspective(200px) rotateX(45deg);
}
/* shorthand */
.box {
  transform: rotateX(15deg) translateZ(20px);
  transform-origin: 0 0;
}
```

## transition properties

```css 
/* If multiple properties need to be transitioned they may be comma separated */
.box {
  background: #2db34a;
  border-radius: 6px
  transition-property: background, border-radius;
  transition-duration: .2s, 1s;
  transition-timing-function: linear, ease-in;
  transition-delay: 0s, 1s;
}

/* shorthand */
/* transition-duration, transition-timing-function, and lastly transition-delay. */
 transition: background .2s linear, border-radius 1s ease-in 1s;
```

### Card flip (kinda cool)

```html
<div class="card-container">
  <div class="card">
    <div class="side">...</div>
    <div class="side back">...</div>
  </div>
</div>
```

```css
.card-container {
  height: 150px;
  perspective: 600;
  position: relative;
  width: 150px;
}
.card {
  height: 100%;
  position: absolute;
  transform-style: preserve-3d;
  transition: all 1s ease-in-out;
  width: 100%;
}
.card:hover {
  transform: rotateY(180deg);
}
.card .side {
  backface-visibility: hidden;
  height: 100%;
  position: absolute;
  width: 100%;
}
.card .back {
  transform: rotateY(180deg);
}
```

## Animations

>To set multiple points at which an element should undergo a transition, use the `@keyframes` rule. 

```css
@keyframes slide {
  0% {
    left: 0;
    top: 0;
  }
  50% {
    left: 244px;
    top: 100px;
  }
  100% {
    left: 488px;
    top: 0;
  }
}

/* Assign to an element */
.stage:hover .ball {
  animation-name: slide;
  animation-duration: 2s;
  animation-timing-function: ease-in-out;
  animation-delay: .5s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
}

.stage:active .ball {
  animation-play-state: paused;
}

/* shorthand */
.stage:hover .ball {
  animation: slide 2s ease-in-out .5s infinite alternate;
}
.stage:active .ball {
  animation-play-state: paused;
}

```
*The `animation-play-state` property allows an animation to be `played` or `paused` using the running and paused keyword values respectively.*

## [8 SIMPLE CSS3 TRANSITIONS THAT WILL WOW YOUR USERS](https://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users/)

1. fade in
2. change color
3. grow
4. shrink
5. rotate
6. square to circle
7. 3d shadows
8. swing
9. insert border


[Main Page](https://will-ing.github.io/reading-notes)