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

<img src="https://d33wubrfki0l68.cloudfront.net/fedcd70d34fc3a5dea2369e727b6a8e7081de43b/3496e/images/initial-coordinate-systems.jpg" width="500">

* Using SVG inline or within <object> provides developers with the widest range of customisation.
 
```
<object type="image/svg+xml" data="kiwi.svg" class="logo">
  Kiwi Logo <!-- fallback image in CSS -->
</object>
```

