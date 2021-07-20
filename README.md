# 常用的 mixin.scss

## 圖片取代文字 hide-text
```
@mixin hide-text{
    text-indent: 101%;
    white-space: nowrap;
    overflow: hidden;
}
```

## background-image
```
@mixin zoomimage{
    background-position: center center;
    background-repeat: no-repeat;
    -webkit-background-size: cover;
    -moz-background-size: cover;
    background-size: cover;
}
```

## RWD
```
@mixin sm{
    @media (min-width:576px) {
        @content        
    };
};
@mixin md{
    @media (min-width:768px) {
        @content        
    };
};
@mixin lg{
    @media (min-width:992px) {
        @content        
    };
};
@mixin xl{
    @media (min-width:1140px) {
        @content        
    };
};
@mixin xxl{
    @media (min-width:1320px) {
        @content        
    };
};
```
