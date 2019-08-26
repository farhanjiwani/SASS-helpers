# SASS-helpers
My goto SASS helpers when I am starting a project. 
**NOTE:** This is a new work in progress.


## Table of Contents
1. Normalize
1. Initial Measurements
    1. Breakpoints
    1. Gutters
1. Accessibility
    1. `sr-only`
1. Animation
    1. Easing


## Normalize
* [normalize.css](https://github.com/farhanjiwani/SASS-helpers/blob/master/normalize.css)
* A CSS reset by [@necolas](https://github.com/necolas/normalize.css/)
* **NOTE**: `box-sizing` is *not* set to `border-box` for all elements by default.


## Initial Measurements

### Breakpoints
* [Initial widths](https://github.com/farhanjiwani/SASS-helpers/blob/master/_variables.scss#L1-L11)
* somewhat based on Google Chrome's inspector device toolbar default breakpoints

### Gutters
* [Initial gutters](https://github.com/farhanjiwani/SASS-helpers/blob/master/_variables.scss#L14-L19)

## Accessibility

### `.sr-only`
* [@mixin sr-only](https://github.com/farhanjiwani/SASS-helpers/blob/master/_accessibility.scss#L1-L18)
* Taken from "Improved .sr-only" by [@ffoodd](https://gist.github.com/ffoodd/000b59f431e3e64e4ce1a24d5bb36034) and made into mixin
* Previously used in Bootstrap 3

```sass
/* Example Usage: */
.sr-only,
.my-selector {
    @include sr-only;
}
```


## Animation

### Easing
* My default easing: `$defaultEasing: 0.3s ease-in-out 0s;`