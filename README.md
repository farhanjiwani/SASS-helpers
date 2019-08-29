# SASS-helpers
My goto SASS helpers when I am starting a project. 
**NOTE:** This is a new work in progress.


## Table of Contents
1. [Normalize](https://github.com/farhanjiwani/SASS-helpers#normalize)
    1. [Custom Resets](https://github.com/farhanjiwani/SASS-helpers#custom-resets)
1. [Initial Measurements](https://github.com/farhanjiwani/SASS-helpers#initial-measurements)
    1. [Breakpoints](https://github.com/farhanjiwani/SASS-helpers#breakpoints)
    1. [Gutters](https://github.com/farhanjiwani/SASS-helpers#gutters)
1. [Fonts](https://github.com/farhanjiwani/SASS-helpers#fonts)
    1. [Custom `font-family` mixin](https://github.com/farhanjiwani/SASS-helpers#custom-font-family-mixin)
1. [Accessibility](https://github.com/farhanjiwani/SASS-helpers#accessibility)
    1. [`sr-only`](https://github.com/farhanjiwani/SASS-helpers#sr-only)
1. [Animation](https://github.com/farhanjiwani/SASS-helpers#animation)
    1. [Easing](https://github.com/farhanjiwani/SASS-helpers#easing)
    1. [Keyframe Animation Template](https://github.com/farhanjiwani/SASS-helpers#keyframe-animation-template)

## Normalize
* [normalize.css](https://github.com/farhanjiwani/SASS-helpers/blob/master/normalize.css)
* A CSS reset by [@necolas](https://github.com/necolas/normalize.css/)
* **NOTES**: 
    * `box-sizing` is *not* set to `border-box` for all elements by default.
    * Base font size not set

### Custom Resets
* [_initializations.scss](https://github.com/farhanjiwani/SASS-helpers/blob/master/_initializations.scss)
* My additional defaults after normalization

#### Element Intializations
* global `box-sizing` set to `boder-box`
* horizontal rule `height` set to `1px`

#### Font Initializations
* base `font-size` set to `10px` for simple rem calculations
* default `font-size` set to `1.6rem` (`16px`)
* global `-webkit-font-smoothing` set to `antialiased;`
* headings `h1` to `h6` get initial `font-size` and `margin` rules


## Initial Measurements

### Breakpoints
* [Initial widths](https://github.com/farhanjiwani/SASS-helpers/blob/master/_variables.scss#L1-L11)
* somewhat based on Google Chrome's inspector device toolbar default breakpoints

### Gutters
* [Initial gutters](https://github.com/farhanjiwani/SASS-helpers/blob/master/_variables.scss#L14-L19)


## Fonts
* Custom `font-family` mixin: [@fntDefault](https://github.com/farhanjiwani/SASS-helpers/blob/master/_mixins.scss#L1-L19)


## Accessibility

### `.sr-only`
* [@mixin sr-only](https://github.com/farhanjiwani/SASS-helpers/blob/master/_accessibility.scss#L1-L18)
* Taken from "Improved .sr-only" by [@ffoodd](https://gist.github.com/ffoodd/000b59f431e3e64e4ce1a24d5bb36034) and made into mixin
* Class name previously used in Bootstrap 3

```sass
/* Example Usage: */
.sr-only,
.my-selector {
    @include sr-only;
}
```


## Animation

### Easing

#### My Default Easing: 
```sass
$defaultEasing: 0.3s ease-in-out 0s;
```

### Keyframe Animation Template

#### Example 1 - From-To
```sass
.my-animation-class {
    // shorthand:
    //   easing | duration | delay | iterations | direction | name
    animation: linear 1.25s 2s 6 alternate pulsate;
}

@keyframes pulsate { 
    from { 
        opacity: 1;
    } 
    
    to { 
        opacity: 0;
    }  
}
```

* `animation-iteration-count`: postive number (including float) or `infinite`
* `animation-direction`: `normal`, `reverse`, `alternate`, `alternate-reverse`