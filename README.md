# SCSS Mixin Media Breakpoints

Package for integrating `SCSS Mixin Media Breakpoints` in a web environment.

![npm](https://img.shields.io/npm/v/@bu0nq/scss-mixin-media-breakpoints?style=for-the-badge)
![npm](https://img.shields.io/npm/dt/@bu0nq/scss-mixin-media-breakpoints?style=for-the-badge)
___

## Installation

This package can be deployed automatically using NPM:

```
npm i @bu0nq/scss-mixin-media-breakpoints
```

## Usage

Import in your project depending on your setup:

```scss
@use "@bu0nq/scss-mixin-media-breakpoints" as *;
```

## List mixins

* media-breakpoint-min(size)
* media-breakpoint-max(size)
* media-breakpoint-min-max(size, size)

## Change variables

You can redefine the default values of variables when importing a `mixin`:

```scss
@use "@bu0nq/scss-mixin-media-breakpoints" as * with (
    $breakpoint-xxs: 480px,
    $breakpoint-xs: 640px,
    $breakpoint-sm: 768px,
    $breakpoint-md: 1024px,
    $breakpoint-lg: 1280px,
    $breakpoint-xl: 1440px,
    $breakpoint-xxl: 1536px,
);
```

## Change namespace

You can change the namespace during import and use the `mixin` with a different namespace:

```scss
@use "@bu0nq/scss-mixin-media-breakpoints" as mixin;

.demo {
    @include mixin.media-breakpoint-min-max(xl) {
        background-color: hsl(120, 100%, 25%);
    }
}
```
