SASS mixins readme. Other preprocessor's readme placed in related files.

**Test rgba background**, simple and useful mixin like in dev tools tools to see element's size, paddings and etc. By default it sets to 30% transparent red

Inner variables and defaults:
```sass
=testbg($red: 255, $green: 0, $blue: 0, $alpha: .3)
```
Example of usage: 
```sass
+testbg(0,0,0,.5)
```
---
**Test outline**, this mixin apply 1px solid red outline to the element.

Inner variables and defaults: 
```sass
=testout($width: 1px, $line-type: solid, $color: red)
```
Example of usage: 
```sass
+testout(1px,dashed,#000)
```
---
**Hide text while using sprites**

No inner variables

Example of usage: 
```sass
+hidentext()
```
---
**Selection**, this mixin allows to customize text color and background color of selected text.

Inner variables and defaults: 
```sass
=selection($text-color: #333, $bg-color: #efefef)
```
Example of usage: 
```sass
+selection(#f00, #000)
```
---
**Clear-fix for parents that contain float elements**

No inner variables

Example of usage: 
```sass
+clearfix()
```
---
**Stripped gradient as background** This mixin was created by css-tricks.com with some fixes from Paul d'Aoust. First argument is variable that contain color list, second - direction, then fallback color.

Inner variables and defaults: 
```sass
=stripes-gradient($colors, $direction: "to right", $fallback-color: #fff)
```
Example of usage:
```sass
$colors: #fa9300, #66c9ee, #c9c9c9, #82b964
+stripes-gradient($colors, to right)
```