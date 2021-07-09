# theme-color-helpers.scss
_spacing-helpers.scss

```
$primary: rgb(202, 176, 180);
$secondary: #891818;
$notice: #891818;
$white: #fff;
$black: #333;
$dark: #666;
$light: #f3f3f3;

$theme-color: (
  primary:  $primary,
  secondary: $secondary,
  notice: $notice,
  white: white,
  black: $black,
  dark: $dark,
  light: $light,
);


@each $theme, $color in $theme-color{
  .text-#{$theme}{
    color: #{$color} !important;
  };
  .bg-#{$theme}{
    background-color: #{$color} !important;
  }
};
```
