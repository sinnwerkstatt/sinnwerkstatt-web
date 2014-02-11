# CSS Hacks

## CSS Browser detection

* [Firefox](http://stackoverflow.com/a/5874150/2510374)
```css
/* Detects Firefox */
@-moz-document url-prefix() {
    /* Add Firefox Specific CSS here */
}
```
* [Chrome](http://stackoverflow.com/a/4403749/2510374)
```css
@media screen and (-webkit-min-device-pixel-ratio:0) {
  /* Chrome- and Safari-specific CSS here*/
}
```
