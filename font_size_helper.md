# font_size_helper.scss

font_size_helper.scss

```
$sizer: 1rem !default;
$sizes: (
  1: $sizer * 5,
  2: $sizer * 4,
  3: $sizer * 1.5,
  4: $sizer * 1.25,
);

@each $size, $sizeamount in $sizes{
  .fs-#{$size}{
    font-size: #{$sizeamount} !important;
  }
}
```

