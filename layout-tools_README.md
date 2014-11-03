Layout tools on lesscss and scss
=============
This is a pretty weird mixins library but it useful in css coding especially for pixel perfect.

##Tutorial and demo
A little bit more information about this lib and demo you can find [here](http://orlovmax.com/lab/tools/pixel-perfect-dev).

One`regular-graph-paper` mixin allows you to put regular graphing paper over top your developed page. It creates lines similar to regular graphing paper using linear gradients above your markup, so you can see sizes of elements and margins between them. 

`Layout` mixin allows you to overlay your layout image over top of the developed page. Also you can change the transparency so you can see through image layout and set layout width like your layout picture. As extra option in this mixin included previous mixin, so you can put trbasparent layout with regular graph paper over top youe page.

Basic mixins and defaults
---
**Graph paper mixin in lesscss**

*Default settings and variables*

`.regular-graph-paper(@grid-opacity:1, @cell-width: 10px, @cell-height: 10px, @line-color: #fff);` - variables set opacity of grid lines (1 by default), width and height (10x10px default) of grid cells and line color (white by default).

*Use example:*

`.regular-graph-paper(.4, 10px, 10px, #2c3e50);` - it means that grid have 40% transparency, 10x10px cells and line color #2c3e50 (midnight from flat-ui).

**Graph paper mixin in scss**

*Default settings and variables*

`@mixin regular-graph-paper($grid-opacity:1, $cell-width: 10px, $cell-height: 10px, $line-color: #fff);`

*Use example:*

`@include regular-graph-paper(.4, 10px, 10px, #2c3e50);`

---
**Graph paper mixin in lesscss**

*Default settings and variables*

`.layout(@layout-url: "../img/layout.jpg", @layout-width:100%, @layout-opacity: .5, @grid-opacity:0, @cell-width:10px, @cell-height:10px, @line-color:#fff);` - There are bunch of options as layout url(by default it sets to "../img/layout.jpg", so it seems that your layout in img folder that on the same level as css folder with current style), layout width(100% by default, you should set to width of layout picture), layout opacity(by default sets to 0.5) and graphing paper grid options - grid opacity( 0 as default option), cell width(10px by default), cell height(10px by default), line color(#fff by default).

*Use example:*

Layout without grid `.layout("../img/layout.jpg", .5, 1275px)` - there is image layout called layout.jpg with 50% transparency and max-width 1275px. You can see result on the second screenshot

Layout with grid `.layout("../img/layout.jpg", .5, 1275px, .4, 10px, 10px, #2c3e50)` - there is image layout called layout.jpg with 50% transparency, max-width 1275px and graph paper grid with 10x10px cells, 40% transparency and line color #2c3e50. See result on third screen.

**Graph paper mixin in scss**

*Default settings and variables*

`@mixin layout($layout-url: "../img/layout.jpg", $layout-opacity: .5, @layout-width:100%, $grid-opacity:0, $cell-width:10px, $cell-height:10px, $line-color:#fff);` - There are bunch of options as layout url(by default it sets to "../img/layout.jpg", so it seems that your layout in img folder that on the same level as css folder with current style), layout width(100% by default, you should set to width of layout picture), layout opacity(by default sets to 0.5) and graphing paper grid options - grid opacity( 0 as default option), cell width(10px by default), cell height(10px by default), line color(#fff by default).

*Use example:*

Layout without grid `@include layout("../img/layout.jpg", .5, 1275px)` - there is image layout called layout.jpg with 50% transparency and  max-width 1275px. You can see result on the second screenshot

Layout with grid `@include layout("../img/layout.jpg", .5, 1275px, .4, 10px, 10px, #2c3e50)` - there is image layout called layout.jpg with 50% transparency, max-width 1275px and graph paper grid with 10x10px cells, 40% transparency and line color #2c3e50. See result on third screen.

---

This is important:
---
- Please notice that z-index of grid and layout sets to 999, so you're unable to test your links by clicking them
- I recomend you to mix up these mixins to html or body tag, and it'll create pseudo elements with desirable content.

But don't worry about, it's all pretty simple and easy to use and very useful.

License
---
[MIT](http://adampritchard.mit-license.org/)