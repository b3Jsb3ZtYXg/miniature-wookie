# Deprecated in favor of autoprefixer usage

**Test rgba background**, simple and useful mixin to check element's size, paddings and etc. By default it sets to 30% transparent red

Inner variables and defaults: 
```less
.testbg(@red: 255, @green: 0, @blue: 0, @alpha: .3);
```
Example of usage: 
```less
.testbg(0,0,0,.5);
```
---
**Test outline**, this mixin apply 1px solid red outline to the element.

Inner variables and defaults: 
```less
.testout(@width: 1px, @line-type: solid, @color: red);
```
Example of usage: 
```less
.testout(1px,dashed,#000);
```
---
**Hide text while using sprites**

No inner variables

Example of usage: 
```less
.hidentext;
```
---
**Clear-fix for parents that contain float elements**

No inner variables

Example of usage: 
```less
.clearfix;
```
---
**This mixin sets opacity**, 50% by default

Inner variables and defaults: 
```less
.opac(@opacity: 0.5);
```
Example of usage:
```less
.opac(0.8);
```
---
**Box sizing**, border-box by default

Inner variables and defaults: 
```less
.sizing(@sizing: border-box);
```
Example of usage:
```less
.sizing(border-box);
```
---
**Size of element**, 0 by default

Inner variables and defaults: 
```less
.size(@width:0, @height:0);
```
Example of usage:
```less
.size(100px, 200px);
```
---
**Disable user selection**

Inner variables and defaults: 
```less
.u-select(@argument: none);
```
Example of usage:
```less
.u-select(text);
```
---
**This mixin sets `background-size: cover`**

No inner variables

Example of usage: 
```less
.bg-cover;
```
---
**This mixin sets `background-size: contain`**

No inner variables

Example of usage: 
```less
.bg-contain;
```
---
**Background size mixin** that allows you to set element's background size. By default it expect 2 numbers: horizontal background size and vertical background size, also it supports multiple background sizes. But remember that you need to escape commas between pairs of numbers or values like this `~","`

Inner variables and defaults: 
```less
.bg-size(...);
```
Example of usage:
```less
.bg-size(10px 10px ~"," cover); 
```
In this case first pair refers to the one background, second value - to other background
---
**Set `border-radius`**, 5px by default to all corners. Mixin `border-raius` allows you to add custom radius to each corner. 

Inner variables and defaults: 
```less
.rounded(@radius: 5px);

or

.b-radius(@top-left: 5px, @top-right: 5px, @bottom-right: 5px, @bottom-left: 5px);
```
Example of usage:
```less
.rounded(10px);

or

.border-radius(7px, 10px, 15px, 20px);
```
---
**Linear gradient as background**, first argument is angle or position, second - start color, then stop color. At last - fallback color.

By default it's `background: linear-gradient(top, #fff, #000)` with start color as fallback

Inner variables and defaults: 
```less
.l-gradient(@angle-position: top, @start-color: #fff, @stop-color: #000, @fallback-color: @start-color);
```
Example of usage:
```less
.l-gradient(170deg, #ffa500, #d20909, #ffa500);
```
---
**Set `box-shadow`**. Arguments: horizontal offset, vertical offset, blur radius, spread, color.

Inner variables and defaults: 
```less
.shadow(@hoff: 1px, @voff: 1px, @blur: 2px, @spread: 0, @color: #000);
```
Example of usage:
```less
.shadow(-6px, 4px, 8px, -3px, rgba(0, 0, 0, 0.5));
```
---
**Set `box-shadow: inset`**. Arguments: horizontal offset, vertical offset, blur radius, spread, color.

Inner variables and defaults: 
```less
.inset-shadow(@hoff: 1px, @voff: 1px, @blur: 2px, @spread: 0, @color: #000);
```
Example of usage: 
```less
.inset-shadow(-3px, 3px, 6px, 0, rgba(0, 0, 0, 0.5));
```
---
**Animation mixin**. There are a bunch of arguments: animation-name, animation-duration, animation-tfunction, animation-delay, animation-iteration, animation-direction, animation-play-state.

Inner variables and defaults: 
```less
.animate(@animation-name:first, @animation-duration:1s, @animation-tfunction:linear, @animation-delay:0s, @animation-iteration:infinite, @animation-direction:normal, @animation-play-state:running)
```
Example of usage: 
```less
.animate(some-name,2s,linear,0s,1); //Here we just use 4 first args and last 2 are defaults
```
---
**Multiple transform**. Feel free to use any valid arguments, it useful for combinations

Inner variables and defaults: 
```less
.transf(...);
```
Example of usage: 
```less
.transf(rotate(360deg) scale(1.5));
```
---
**Transform origin mixin**. Allows you to change the point of origin of a transform.

Inner variables and defaults: 
```less
.t-origin(@X-axis:50%, @Y-axis:50%, @Z-axis:0);
```
Example of usage: 
```less
.t-origin(0, 50%);
```
---
More detailed transformation mixins:
**Set `transform: rotate`**. Rotates element from current position.

Inner variables and defaults: 
```less
    .t-rotate(@rotate-angle: 0deg);
```
Example of usage:
```less
    .t-rotate(45deg);
```
---
**This mixin proportionally scale element**. `transform: scale` By default it sets to 1

Inner variables and defaults: 
```less
    .t-scale(@scale: 1);
```
Example of usage: 
```less
    .t-scale(1.3);
```
---
**Scale element by X and Y**. `transform: scale` with two arguments. Similar to previous. By default it sets to 1

Inner variables and defaults: 
```less
        .t-scaleXY(@scaleX: 1, @scaleY: 1);
```
Example of usage:
```less
    	.t-scaleXY(1.4, 2);
```
---
**Scale element by X `transform: scalex`**. By default it sets to 1

Inner variables and defaults: 
```less
		.t-scaleX(@scaleX: 1);
```
Example of usage:
```less
		.t-scaleX(0.5);
```
---
**Scale element by Y `transform: scaley`**. By default it sets to 1

Inner variables and defaults: 
```less
		.t-scaleY(@scaleY: 1);
```
Example of usage:
```less
		.t-scaleY(2.5);
```
---
**This mixin allows you to skew an element on the x and y axis**, By default it sets to 0

Inner variables and defaults: 
```less
	.t-skew(@skewx-angle: 0, @skewy-angle: 0);     
```
Example of usage:
```less
	.t-skew(0deg, -25deg);     
```
---
**Skew element on the x axis**.

Inner variables and defaults: 
```less   
		.t-skewX(@skewX-angle: 0);
```
Example of usage:
```less   
		.t-skewX(30deg);
```
---
**Skew element on the y axis**.

Inner variables and defaults: 
```less
		.t-skewY(@skewY-angle: 0);
```
Example of usage: 
```less
		.t-skewY(-45deg);
```
---
**This mixin moves or relocates an element on the x and y axis** using `transform: translate`

Inner variables and defaults: 
```less
	.t-translate(@move-x:0, @move-y:0);
```
Example of usage:
```less
	.t-translate(-40px, 100px);
```
---
**Allows elements to change values over a specified duration**. 

Default options: all properties, 0.5s uration, ease time function and no delay

Inner variables and defaults: 
```less
.transit(@property: all, @duration: .5s, @tfunction: ease, @delay: 0s);
```
Example of usage:
```less
.transit(all, 0.5s, ease-in, 0);
```
---
**Column count mixin**. 
Create css multiple columns. One by default

Inner variables and defaults: 
```less
.col-count(@count: 1);
```
Example of usage:
```less
.col-count(@count: 5);
```
---
**Column gap**. 
Gap between css multiple columns

Inner variables and defaults: 
```less
.col-gap(@gap: 0);
```
Example of usage:
```less
.col-gap(@gap: 10px);
```