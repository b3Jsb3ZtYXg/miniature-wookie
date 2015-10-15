# Typographic rhythm generator for SASS, SCSS and Stylus

Mixin library to create a typographic system using scale and vertical rhythm.
In general this tool was inspired by Gridlover, ModularScale and Compass vertical rhythm tool.

## Demo
You can find [Demo](http://codepen.io/orlovmax/pen/jbGwYW) and [playground](http://codepen.io/orlovmax/pen/RWZgJz) on Codepen. Feel free to play with different options and combinations. Also, check out other versions of this mixin for Stylus and Scss in my profile.

## What we have
There is one general mixin with a few options:

`typo-rhythm($level-factor, $base-font-size, $base-line-height, $scale-factor)`

* $level-factor - means exponent number of repeated multiplication of the scale factor (number >= 0 or 'auto')
It relates with scale of different text elements and defines how should one element should be bigger than common text
* $base-font-size - in general this is the font size of common text in paragraph (in px)
* $base-line-height - line height of common text in paragraph (number >= 1)
* $scale-factor - defines scaling proportion of elements (number > 1)

## Usage with default settings (ex. SASS)
```sass
// Defaults from mixin file
$level-factor: 'auto'
$base-font-size: 20px
$base-line-height: 1.4
$scale-factor: 1.5

// Demo style
h1
	+typo-rhythm()
h2
	+typo-rhythm()
h3
	+typo-rhythm()
p
	+typo-rhythm()
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
Let's see what changes if we'll use other settings. I'll change only level, but feel free to experiment with other options - it could give pretty interesting results.

## Usage with manual settings (ex. SASS)
```sass
h1
	+typo-rhythm(4)
h2
	+typo-rhythm(3)
h3
	+typo-rhythm(0)
p
	+typo-rhythm(0)
```

And generated css
```css
h1 {
  font-size: 101px;
  line-height: 112px;
  margin-top: 56px;
  margin-bottom: 28px;
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

That's all for now. Maybe later I'll extend this readme and add more examples.
