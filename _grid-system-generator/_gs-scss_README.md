# Simple and flexible grid for SCSS 
There are four mixins: grid container, grid column, grid row, push and pull. Grid container and grid row are the same mixin.

* Grid system container mixin, should be used for grid container and rows.
* Column mixin has next variables: column count for current element, total column count in row, horizontal gutter and vertical gutter and their fallbacks. By default it sets to 1 column of 12 total columns wit 2% gutters.
* Offset mixin allows to push column left or pull it right on some distance. Expected settings: distance-column count to move on, total column count in row, horizontal gutter like in other columns. By default it sets to 1 column of 12 total columns with 2% gutters.

## Predefined settings
$gs_width: 100%;
$gs_gutter-width: 0; 
$gs_gutter-height: 0;
$gs_gutter-width-fallback: 0;   

$column_count: 1; 
$column_total-count: 12;
$column_gutter-height: 2%;  
$column_gutter-width: 2%;   
$column_gutter-height-fallback: 2%; 
$column_gutter-width-fallback: 2%;
$column_height: auto;

**Grid ontainer mixin**

Inner variables and defaults: 
```scss
@mixin gs($gs_width, $gs_gutter-width, $gs_gutter-height, $gs_gutter-width-fallback)
```
Example of usage: 
```scss
@include gs();
```
---

**Column mixin**

Inner variables and defaults: 
```scss
@mixin gs-column($column_count, $column_total-count, $column_gutter-width, 
            $column_gutter-height, $column-height, $column_gutter-width-fallback, $column_gutter-height-fallback, $gs-width)
```
Example of usage: 
```scss
@include gs-column(1,12,1%,10px,80px,2%, 10px);
```
---

**Push**

Inner variables and defaults: 
```scss
@mixin gs-push( $column_count, $column_total-count, $column_gutter-width, $column_gutter-width-fallback, $gs_width)
```
Example of usage: 
```scss
@include gs-push(1,12,1%);
```
---

**Pull**

Inner variables and defaults: 
```scss
@mixin gs-pull( $column_count, $column_total-count, $column_gutter-width, $column_gutter-width-fallback, $gs_width)
```
Example of usage: 
```scss
@include gs-pull(4,12,1%);
```
---

## Demo and tutorial
Check tutorial and usage examples [here](http://orlovmax.com/lab/tools/miniature-wookie_grid-system)