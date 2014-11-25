**Test rgba background**, simple and useful mixin like in dev tools tools to see element's size, paddings and etc. By default it sets to 30% transparent red

Inner variables and defaults: 
```css
@mixin testbg($red: 255, $green: 0, $blue: 0, $alpha: .3);
```
Example of usage: 
```css
@include testbg(0,0,0,.5);
```
---
**Test outline**, this mixin apply 1px solid red outline to the element.

Inner variables and defaults: 
```css
@mixin testout($width: 1px, $line-type: solid, $color: red);
```
Example of usage: 
```css
@include testout(1px,dashed,#000);
```
---
**Hide text while using sprites**

No inner variables

Example of usage: 
```css
@include hidentext;
```
---
**Selection**, this mixin allows to customize text color and background color of selected text.

Inner variables and defaults: 
```css
@mixin selection($text-color: #333, $bg-color: #efefef);
```
Example of usage: 
```css
@include selection(#f00, #000);
```
---
**Clear-fix for parents that contain float elements**

No inner variables

Example of usage: 
```css
@include clearfix;
```
---
**This mixin sets opacity**, 50% by default

Inner variables and defaults: 
```css
@mixin opacity($opacity: 0.5);
```
Example of usage:
```css
@include opacity(0.8);
```
---
**Box sizing**, border-box by default

Inner variables and defaults: 
```css
@mixin box-sizing($sizing: border-box);
```
Example of usage:
```css
@include box-sizing(border-box);
```

---
**Size of element**, 0 by default

Inner variables and defaults: 
```css
@mixin size($width:0, $height:0);
```
Example of usage:
```css
@include size(100px, 200px);
```
---
**Disable user selection**

Inner variables and defaults: 
```css
@mixin user-select($argument: none);
```
Example of usage:
```css
@include user-select(text);
```
---
**This mixin sets `background-size: cover`**

No inner variables

Example of usage: 
```css
@include bg-cover;
```
---
**This mixin sets `background-size: contain`**

No inner variables

Example of usage: 
```css
@include bg-contain;
```
---
**Background size mixin** that allows you to set element`s background size. By default it expect 2 numbers: horizontal background size and vertical background size, also it supports multiple background sizes. But remember that you need to put commas between pairs of numbers

Inner variables and defaults: 
```css
@mixin bg-size($arguments...);
```
Example of usage:
```css
@include bg-size(10px 10px, cover); 
or
@include bg-size(#{10px 10px}, #{100%  100%});
```
In this case first pair refers to the one background, second - to other

---
**Set `border-radius`**, 5px by default to all corners. Mixin `border-raius` allows you to add custom radius to each corner. 

Inner variables and defaults: 
```css
@mixin rounded($radius: 5px);

or

@mixin border-radius($top-left: 5px, $top-right: 5px, $bottom-right: 5px, $bottom-left: 5px);
```
Example of usage:
```css
@include rounded(15px);

or

@include border-radius(7px, 10px, 15px, 20px);
```
---
**Linear gradient as background**, first argument is angle or position, second - start color, then stop color. At last - fallback color.

By default it's `background: linear-gradient(top, #fff, #000)` with start color as fallback

Inner variables and defaults: 
```css
@mixin linear-gradient($angle-position: top, $start-color: #fff, $stop-color: #000, $fallback-color: $start-color);
```
Example of usage:
```css
@include linear-gradient(170deg, #ffa500, #d20909, #ffa500);
```
---
**Stripped gradient as background** This mixin was created by css-tricks.com with some fixes from Paul d'Aoust. First argument is variable that contain color list, second - direction, then fallback color.

Inner variables and defaults: 
```css
@mixin stripes-gradient($colors, $direction: "to right", $fallback-color: #fff)
```
Example of usage:
```css
$colors: #fa9300, #66c9ee, #c9c9c9, #82b964;
@include stripes-gradient($colors, to right);
```
---
**Set `box-shadow`**. Arguments: horizontal offset, vertical offset, blur radius, spread, color.

Inner variables and defaults: 
```css
@mixin box-shadow($hoff: 1px, $voff: 1px, $blur: 2px, $spread: 0, $color: #000);
```
Example of usage:
```css
@include box-shadow(-6px, 4px, 8px, -3px, rgba(0, 0, 0, 0.5));
```
---
**Set `box-shadow: inset`**. Arguments: horizontal offset, vertical offset, blur radius, spread, color.

Inner variables and defaults: 
```css
@mixin inset-box-shadow($hoff: 1px, $voff: 1px, $blur: 2px, $spread: 0, $color: #000);
```
Example of usage: 
```css
@include inset-box-shadow(-3px, 3px, 6px, 0, rgba(0, 0, 0, 0.5));
```
---
**Multiple `box-shadow`**. Arguments: horizontal offset, vertical offset, blur radius, spread, color for each shadow

Inner variables and defaults: 
```css
@mixin multiple-box-shadow($shadow...);
```
Example of usage: 
```css
@include multiple-box-shadow(inset  0  3px 3px -2px #555, 
                             inset  0 -3px 3px -2px #555);
```
---
**Animation mixin**. There are a bunch of arguments: animation-name, animation-duration, animation-tfunction, animation-delay, animation-iteration, animation-direction, animation-play-state.

Inner variables and defaults: 
```css
@mixin animation($animation-name:first, $animation-duration:1s, $animation-tfunction:linear, $animation-delay:0s, $animation-iteration:infinite, $animation-direction:normal, $animation-play-state:running)
```
Example of usage: 
```css
@include animation(some-name,2s,linear,0s,1); //Here we just use 4 first args and last 2 are defaults
```
---
**Multiple transform**. Feel free to use any valid arguments, it useful for combinations

Inner variables and defaults: 
```css
@mixin transform($arguments...);
```
Example of usage: 
```css
@include transform(rotate(360deg) scale(1.5));
```
---
**Transform origin mixin**. Allows you to change the point of origin of a transform.

Inner variables and defaults: 
```css
@include t-origin($X-axis:50%, $Y-axis:50%, $Z-axis:0);
```
Example of usage: 
```css
@include t-origin(0, 50%);
```
---
More detailed transformation mixins:
**Set `transform: rotate`**. Rotates element from current position. Default units `deg`

Inner variables and defaults: 
```css
@mixin rotate($rotate-angle: 0);
```
Example of usage:
```css
@include rotate(45deg);
```
---
**This mixin proportionally scale element**. `transform: scale` By default it sets to 1

Inner variables and defaults: 
```css
@mixin scale($scale: 1);
```
Example of usage: 
```css
@include scale(1.3);
```
---
**Scale element by X and Y**. `transform: scale` with two arguments. Similar to previous. By default it sets to 1

Inner variables and defaults: 
```css
@mixin scaleXY($scaleX: 1, $scaleY: 1);
```
Example of usage:
```css
@include scaleXY(1.4, 2);
```
---
**Scale element by X `transform: scalex`**. By default it sets to 1

Inner variables and defaults: 
```css
@mixin scaleX($scaleX: 1);
```
Example of usage:
```css
@include scaleX(0.5);
```
---
**Scale element by Y `transform: scaley`**. By default it sets to 1

Inner variables and defaults: 
```css
@mixin scaleY($scaleY: 1);
```
Example of usage:
```css
@include scaleY(2.5);
```
---
**This mixin allows you to skew an element on the x and y axis**

Inner variables and defaults: 
```css
@mixin skew($skewx-angle: 0, $skewy-angle: 0);     
```
Example of usage:
```css
@include skew(0, -25deg);     
```
---
**Skew element on the x axis**.

Inner variables and defaults: 
```css   
@mixin .skewX($skewX-angle: 0);
```
Example of usage:
```css   
@include skewX(30deg);
```
---
**Skew element on the y axis**.

Inner variables and defaults: 
```css
@mixin skewY($skewY-angle: 0);
```
Example of usage: 
```css
@include skewY(-45deg);
```
---
**This mixin moves or relocates an element on the x and y axis** using `transform: translate`

Inner variables and defaults: 
```css
@mixin translate($move-x:0, $move-y:0);
```
Example of usage:
```css
@include translate(-40px, 100px);
```
---
**Allows elements to change values over a specified duration**. 

Default options: all properties, 0.5s uration, ease time function and no delay

Inner variables and defaults: 
```css
@mixin transition($property: all, $duration: .5s, $tfunction: ease, $delay: 0s);
```
Example of usage:
```css
@include transition(all, 0.5s, ease-in, 0s);
```
---
**Column count mixin**. 
Create css multiple columns. One by default

Inner variables and defaults: 
```css
@mixin col-count($count: 1);
```
Example of usage:
```css
@include col-count($count: 5);
```
---
**Column gap**. 
Gap between css multiple columns

Inner variables and defaults: 
```css
@mixin col-gap($gap: 0);
```
Example of usage:
```css
@include col-gap($gap: 10px);
```