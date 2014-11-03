#Miniature-wookie - just another mixin lib
This is a set of useful mixins for [Sass\Scss](http://sass-lang.com/) and [Less](http://lesscss.org/) and simple grid system for common projects.

Why "miniature-wookie"? - I don't know, it's just github repo naming advice ;)

## Contents
* [Quick start](#quick-start)
    - [Elements lib](#elements-lib)
    - [Grid system](#grid-system)
    - [Layout tools](#layout-tools)
* [Conclusion](#conclusion)
* [TODO](#todo)
* [Changelog](#changelog)
* [License](#license)

## Quick start
Ok, for now there are three mixin libs like common elements, grid and weird mixn for pixel perfect dev. Just include it to your stylesheet and apply desirable mixin. Each lib have their own readme with detailed explanations.

### Elements lib

### Grid system

### Layout tools
It's nice set with two mixins, that allows to develop on the principle of pixel-perfect. It contains two separate mixins: first - layout mixin, the second - graph paper that positioned over the page.
Usage is very simple: first you need to import the library and apply mixin to <body> tag, with desired options. This will result in the imposition of `layout.jpg` over web page. Image width will be equal to 100% and opacity - 50%. Optionally available "graph paper" default grid is not shown because its opacity is equal to zero. See more at `layout-tools_README` or in [this tutorial](http://orlovmax.com/lab/tools/pixel-perfect-dev)

## Conclusion
As you can see elements library was based on the similar or same properties as original css, but makes code more "dry" and clean .You should use autoprefixer instead of most mixins in this lib. But for dev - it's ok.

This grid system mixin lib was created for one of my bicycles - Inclusion framework. I like it because as it based on calc() css3 property, it allows me to create fluid nested grid with fixed gutters and make some fallback for non-feature-rich browsers.

Layout tools - just quick-created mixin for pixel perfect dev. Put layout image as semi-transparent background to the body tag. That's easy and useful.

## TODO
* Quick start section readmy
* Demo
* Less grid system
* Extends and generated classes for grid system

## Changelog
* (November 3, 2014)
    - Layout tools added
* (October 28, 2014)
    - Grid system added

## License
[MIT](http://opensource.org/licenses/MIT)
