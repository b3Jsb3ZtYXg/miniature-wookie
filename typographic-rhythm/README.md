# Typographic rhythm generator for SASS, SCSS and Stylus

Mixin library to create a typographic system using scale and vertical rhythm.
In general this tool was inspired by Gridlover, ModularScale and Compass vertical rhythm tool.

## Demo
You can find [Demo](http://codepen.io/orlovmax/pen/jbGwYW) and [playground](http://codepen.io/orlovmax/pen/RWZgJz) on Codepen. Feel free to play with different options and combinations. Also, check out other versions of this mixin for Stylus and Scss in my profile.

## TYPOGRAPHYC RHYTHM MIXIN

`typographic-rhythm($level: $tr_level-factor, $base-fz: $tr_base-font-size, $lh: $tr_base-line-height, $scale: $tr_scale-factor, $top: $tr_top-space, $bottom: $tr_bottom-space)`

$tr_level-factor - means exponent number of repeated multiplication of the scale factor (number >= 0 or 'auto')
It relates with scale of different text elements and defines how should one element should be bigger than common text
$tr_base-font-size - in general this is the font size of common text in paragraph (in px)
$tr_base-line-height - line height of common text in paragraph (number >= 1)
$tr_scale-factor - defines scaling proportion of elements (number > 1)
$tr_top-space - type of the element's top space (string, could be 'margin', 'padding' or 'none')
$tr_bottom-space - type of the element's bottom space (string, could be 'margin', 'padding' or 'none')

NOTE: If you want to set options as mixin's parameters, please use the next settings: `typographic-rhythm($level, $base-fz, $lh, $scale, $top, $bottom)`

## Usage with default settings (ex. SASS)
```sass
// Defaults from mixin file
$tr_level-factor: 'auto'
$tr_base-font-size: 20px
$tr_base-line-height: 1.4
$tr_scale-factor: 1.5
$tr_top-space: 'margin'
$tr_bottom-space: 'margin'

// Demo style
h1
    +typographic-rhythm()
h2
    +typographic-rhythm()
h3
    +typographic-rhythm()
p
    +typographic-rhythm()
```

In this example we use auto level mode, so we'll get the next css:

```css
h1 {
    font-size: 68px;
    line-height: 84px;
    margin-top: 56px;
    margin-bottom: 28px;
}

h2 {
    font-size: 45px;
    line-height: 56px;
    margin-top: 56px;
    margin-bottom: 28px;
}

h3 {
    font-size: 30px;
    line-height: 56px;
    margin-top: 28px;
    margin-bottom: 28px;
}
p {
    font-size: 20px;
    line-height: 28px;
    margin-top: 28px;
    margin-bottom: 28px;
}
```

As you can see mixin defined the parent selector and applied related level, so the H1 tag is three times scaled using scale factor than common paragraph. That's the point.
Let's see what changes if we'll use other settings.

## Usage with manual settings (ex. SASS)
```sass
h1
    +typographic-rhythm(4, $top: 'padding', $bottom: 'none')
h2
    +typographic-rhythm(3)
h3
    +typographic-rhythm(0)
p
    +typographic-rhythm(0)
```

And generated css
```css
h1 {
    font-size: 101px;
    line-height: 112px;
    padding-top: 56px;
}

h2 {
    font-size: 68px;
    line-height: 84px;
    margin-top: 56px;
    margin-bottom: 28px;
}

h3 {
    font-size: 20px;
    line-height: 28px;
    margin-top: 28px;
    margin-bottom: 28px;
}
p {
    font-size: 20px;
    line-height: 28px;
    margin-top: 28px;
    margin-bottom: 28px;
}
```


## TYPOGRAPHYC SPACE MIXIN
And now it's time for the second mixin - typographic space mixin. It allows to add top and bottom spaces according to our general rhythm. It's useful when we have a deal with some decorated elements, when top or bottom space should be included into content area or excluded from there.

`typographic-space($top: $tr_top-space, $bottom: $tr_bottom-space, $level: $tr_level-factor, $base-fz: $tr_base-font-size, $lh: $tr_base-line-height)`


$tr_top-space - type of the element's top space (string, could be 'margin', 'padding' or 'none')
$tr_bottom-space - type of the element's bottom space (string, could be 'margin', 'padding' or 'none')
$tr_level-factor - means exponent number of repeated multiplication of the scale factor (number >= 0 or 'auto')
It relates with scale of different text elements and defines how should one element should be bigger than common text
$tr_base-font-size - in general this is the font size of common text in paragraph (in px)
$tr_base-line-height - line height of common text in paragraph (number >= 1)

NOTE: If you want to set options as mixin's parameters, please use the next settings: `typographic-space($top, $bottom, $level, $base-fz, $lh)`

## Usage with default settings (ex. SASS)
```sass
// Defaults from mixin file
$tr_level-factor: 'auto'
$tr_base-font-size: 20px
$tr_base-line-height: 1.4
$tr_scale-factor: 1.5
$tr_top-space: 'margin'
$tr_bottom-space: 'margin'

// Demo style
h1
    +typographic-rhythm($top: 'none', $bottom: 'padding')
    +typographic-space($top: 'padding')

ul
    +typographic-space($top: 'padding')

```

In this example we use auto level mode, so we'll get the next css:

```css
h1 {
    font-size: 68px;
    line-height: 84px;
    padding-top: 56px;
    padding-bottom: 28px;
}

ul{
    padding-top: 28px;
    margin-bottom: 28px;
}
```

As you can see this mixin allows to use margins and paddings that relate to our typographic rhythm.

That's all for now. Maybe later I'll extend this readme and add more examples.
