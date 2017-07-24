# Sass-mixins
Deskrypcja.

## Helpful links for weird cases:
#### IE
For breaking too long strings into multiple lines, instead of `word-break: break-word` it's better to use `word-wrap: break-word`. IE supports it.

When setting `background-attachment: fixed` the image is 'jumping' in IE's, here's the [fix](https://stackoverflow.com/a/35700548)
#### IE9
[Box-shadow not displayed in table](http://stackoverflow.com/questions/5617455/box-shadow-on-ie9-doesnt-render-using-correct-css-works-on-firefox-chrome)
#### IE10
When using transform in keyframes, make sure to add all the values, even if they equal 0.
```
@keyframes close-notice
  0%
    +transform(translateX(-50%)) - DON'T
    +transform(translateY(0) translateX(-50%)) - DO
  100%
    +transform(translateY(-200%) translateX(-50%))
```    

[Flexbox cheatsheet](http://zomigi.com/blog/flexbox-syntax-for-ie-10/)

When `justify-content: space-between` is set, it won't work on inline (`span`) child elements, those need to be block.
#### FireFox
![lol](https://raw.githubusercontent.com/Darex1991/Sass-mixins/master/assets/firefox_icons.png)

It might happen that the fonticons are jagged/broken under Windows. In that case just pick the icons from Icomoon once again.

-
The placeholder text looks a bit different in Firefox, to keep it consistent add `opacity: 1` to it.
#### Safari
When creating a gradient that should go to transparent, instead of `$color-transparent` it's mandatory to set it as rgba, or Safari will render it as black.
```
background: linear-gradient(to right, $color-white 25%, rgba($color-white, 0) 65%)
```

Good hack for Safari >= 9
```
@supports (-webkit-flow-into: break)
```
#### CSS hacks
[Tooltip line break with `&#10;`](http://stackoverflow.com/questions/358874/how-can-i-use-a-carriage-return-in-a-html-tooltip)

[Nice collection of hacks](https://stackoverflow.com/questions/16348489/is-there-a-css-hack-for-safari-only-not-chrome)
