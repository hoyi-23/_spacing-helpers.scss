# _spacing-helpers.scss
_spacing-helpers.scss

```
/*
這個迴圈可以讓我們快速使用自訂的 margin padding
使用的方式: 
.mr-1 which gives margin-right 0.5rem
.mr-2 gives MARGIN to the RIGHT 1rem.
.mt-3 gives MARGIN to the TOP 2.25rem.
.pb-4 gives PADDING to the BOTTOM of 2.5rem
.pl-5 gives PADDING to the LEFT of 2.875rem
第一個單字 "m" or "p" 代表 MARGIN or PADDING
第二個單字 "t", "b", "l", or "r" 代表 TOP, BOTTOM, LEFT, or RIGHT
數字的部分 都可以自己調整到需要的大小 這裡是使用rem作為單位 也可以改為px等
*/


$spacer: 1rem !default;
$spacers: (
  0: 0,
  1: $spacer * 0.5,
  2: $spacer,
  3: $spacer * 2.25,
  4: $spacer * 2.5,
  5: $spacer * 2.875,
  6: $spacer * 3.125,
);

$sides: (top, bottom, left, right); // Leave this variable alone

@each  $space, $spaceamount in $spacers {
  @each $side in $sides {
    .m#{str-slice($side, 0, 1)}-#{$space} {
      margin-#{$side}: #{$spaceamount} !important;
    }
  
    .p#{str-slice($side, 0, 1)}-#{$space} {
      padding-#{$side}: #{$spaceamount} !important;
    }
  }
}
```
