This is the logical extension of two very useful mixins for debugging - `testbg()` and `testout()` - add semi-transparent background and outline to elements.
This tool is mixin, that applies to the root tag or global scope and can highlight specific or all elements and add to them colored outline. 
Shortcodes for these mixins you can find [here](https://github.com/orlovmax/lab/blob/master/miniature-wookie/_mixins-lib)

Inner variables and defaults: 
```sass
=ignition($scope: 'g', $target: none, $depth: 0, $bg-color: 'rgba(255,0,0,.3)', $out-color: 'none');
```


Let's talk about available options and their values:
`$scope` - define scope where mixin was applied. Values:
    * 'g' - refers to global, default scope, mixin could be applied in the global scope
    * 'l' - refers to local, use parent element when mixin activated inside selector
    * element-name - specific element might be used as a local scope for mixin, when it called globally
`$target` - start point, it defines mixin's targets and turn it on. It may take the next values:
    * none - mixin is disabled. This is default value
    * all - highlight all elements
    * target-name - highlight specific elements by their tags, classnames or id
`$depth` - define depth of highlighting using direct child selector. Take number as value, that mean level of highlight. 0 by default
`$bg-color` - background color of highlighted elements. rgba(255,0,0,.3) by default
`$out-color` - outline color of highlighted element

Examples of usage:

First one:
```sass
+ignition('g', 'all', 3);
```
In this case we'll highlight all elements inside body tags using this selector:
```css
body > *,
body > * > *,
body > * > * > * {
    // Highlight rules
}
```

Second one:
```sass
.test
    +ignition('l', 'all', 2);
```
Let's mix this mixin to `.test` element. In this case we'll highlight all elements inside `.test` using this selector:
```css
.test > *,
.test > * > * {
    // Highlight rules
}
```

Third one:
```sass
+ignition('div', 'all', 1);
```
Now call mixin from global scope and highlight all elements inside `div`
```css
div > * {
    // Highlight rules
}
```

Fourth one:
```sass
.test
    +ignition('l', '.target', 'all');
```
We call mixin locally within element with `.test` class name and highlight all elements with `.target` class name
```css
.test .target {
    // Highlight rules
}
```