**Test rgba background**, simple and useful mixin like in dev tools tools to see element's size, paddings and etc. By default it sets to 30% transparent red

Inner variables and defaults:
```css
testbg($red: 255, $green: 0, $blue: 0, $alpha: .3);
```
Example of usage: 
```css
testbg(0,0,0,.5);
```
---
**Test outline**, this mixin apply 1px solid red outline to the element.

Inner variables and defaults: 
```css
testout($width: 1px, $line-type: solid, $color: red);
```
Example of usage: 
```css
testout(1px,dashed,#000);
```
---
**Hide text while using sprites**

No inner variables

Example of usage: 
```css
hidentext();
```
---
**Clear-fix for parents that contain float elements**

No inner variables

Example of usage: 
```css
clearfix();
```