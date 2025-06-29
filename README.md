# Continuous Corner Radius Library

This library provides SwiftUI-style continuous corner radius effects for the web.

## Quick Start

1. Copy these files to your project:
   - `continuous-corner.js`
   - `continuous-rounding.css`

2. Link the CSS in your HTML:
```html
<link rel="stylesheet" href="continuous-rounding.css">
```

3. Register the worklet in your HTML:
```html
<script>
    if ('paintWorklet' in CSS) {
        CSS.paintWorklet.addModule('continuous-corner.js');
    }
</script>
```

## Usage

Add the `--continuous-rounding` property to any element:

```html
<div style="--continuous-rounding: 25px">
    Your content here
</div>
```


## Browser Support

Requires browsers that support the CSS Paint API (Houdini).
Modern versions of Chrome, Edge, and Opera are supported.

## Examples

```html

<div class="my-box" style="--continuous-rounding: 75px">
    This box will have smooth continuous corners
</div>


<div class="my-box" style="--continuous-rounding: 75px;
                           --continuous-rounding-bottom-left: 0;
                           --continuous-rounding-bottom-right: 0;">
    This box will have smooth continuous corners only on the top side
</div>


<div class="my-box" style="--continuous-rounding-top-left: 10px;
                           --continuous-rounding-top-right: 50vw;
                           --continuous-rounding-bottom-right: 100px;
                           --continuous-rounding-bottom-left: 150px;">
    This box will have complete custom smooth continuous corners</span>
</div>


<!-- Example to use the library not via style="" but within CSS classes -->
<style>
    .my-custom-box {
        /* your other class styles go here */
        --continuous-rounding-top-left: 50px;
        --continuous-rounding-bottom-left: 50px;
    }
</style>

<!-- the .continuous-rounding class has to be attached to the element, too -->
<div class="my-custom-box continuous-rounding">
    This box will have continuous corners defined in my__class
</div>
```

That's it! Enjoy your smooth continuous corners!
