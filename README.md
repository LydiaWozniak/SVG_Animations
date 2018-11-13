# SVG

* Scalable Vector Graphics

caniuse.com

<img src="https://github.com/LydiaWozniak/SVG_Animations/blob/master/Screen%20Shot%202018-11-09%20at%2015.16.44.png" width="500">

### SVG can be implemented inline.

 ``` 
<svg class="blob" height="1000" width="1000">
  <circle class="dot" cx="50" cy="50" r="50" stoke="none" fill="black" />
</svg>

 ```

* This is a solid black circle with the origin (50, 50), a radius of 50.

* Coordinate system with an x and y axis and the origin is at the top-left corner.

* The size of the whole image in this example is 1000 x 1000.

<img src="https://d33wubrfki0l68.cloudfront.net/fedcd70d34fc3a5dea2369e727b6a8e7081de43b/3496e/images/initial-coordinate-systems.jpg" width="500">

* Using SVG inline or within `<object>` provides developers with the widest range of customisation.
 
```
<object type="image/svg+xml" data="kiwi.svg" class="logo">
  Kiwi Logo <!-- fallback image in CSS -->
</object>

```
# Animations & Transistions

## Transitions

[Example](https://codepen.io/LydiaMoo/pen/mQErOQ)

* Transistions can be used to smoothly change a CSS property for pseudo-class or change of class.

* For SVG paths with the same number of points can be transitioned by using the d property. 
```
 .btn:hover path{
  d: path("M 5,10 L 7.5,15 M 15,5 L 7.5,15");
  stroke: #27AE60;
}
```


## Animations

[Example](https://codepen.io/LydiaMoo/pen/pQbEEj?editors=1100)

* To animate separate parts of the SVG image either enclosing `<g>` tags can be added or clasees `class="part_one"`.
* In CSS keyframes can be used to describe animations. 

```
  @keyframes myAnimation{
    0{
      transform:translate(50px, 50px);
    }
    100%{
      transform:translate(1000px, 100px);
    }
  }
```

```
 .dot1{
 animation: myAnimation 10s ease-out 2s 0 none;
}
```
Animation property shorthand
`animation: keyframes_name duration timing_function delay iteration_count fill_mode;`

### Performance
[source](https://www.html5rocks.com/en/tutorials/speed/high-performance-animations/)

Modern browsers can animate four things really cheaply: position, scale, rotation and opacity. The most performant things to animate are styles that affect paint.

```
color	
border-style
visibility	
background
text-decoration	
background-image
background-position	
background-repeat
outline-color	
outline
outline-style	
border-radius
outline-width	
box-shadow
background-size
```
The least performant things to animate are those which affect layout.
```
width	
height
padding	
margin
display	
border-width
border	
top
position	
font-size
float	
text-align
overflow-y	
font-weight
overflow	
left
font-family	
line-height
vertical-align	
right
clear	
white-space
bottom	
min-height
```

### Animating in React

In react Animations can be more complicated as they often involve manipulating the component lifecycle and often need to delay DOM updates. 
ReactCssTransitionGroup ` react-transition-group `

## More Things to Look at:
* Clip Paths
* Filters
* View-box
*
*
*

