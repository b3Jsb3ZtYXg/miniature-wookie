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
.hidentext();
```
---
**Clear-fix for parents that contain float elements**

No inner variables

Example of usage: 
```less
.clearfix();
```
