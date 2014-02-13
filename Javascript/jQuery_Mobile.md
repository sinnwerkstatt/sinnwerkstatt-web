# jQuery Mobile

Site: http://jquerymobile.com/

## Docu
* [Demos and Documentation](http://jquerymobile.com/demos/) - [Page & dialogs](http://jquerymobile.com/demos/1.2.1/docs/pages/index.html) is very important!
* [Demos](http://view.jquerymobile.com/master/demos/)
* [Widgets](http://api.jquerymobile.com/category/widgets/)

## Examples
* [jqmgallery](http://www.jqmgallery.com/)

## Radio Input change event
* ```$(document).on('change', '.js-answer-input', function(){});``` [Docu](http://stackoverflow.com/a/17422648/2510374)

## Optimize

* Use [FastClick](https://github.com/ftlabs/fastclick)
* Remove hoverDelay

```javascript
function optimizeSpeed() {
var hoverDelay = $.mobile.buttonMarkup.hoverDelay = 0;
$.mobile.defaultPageTransition = 'none';
$.mobile.defaultDialogTransition = 'none';
}
optimizeSpeed();

window.addEventListener('load', function() {
    FastClick.attach(document.body);
}, false);
```

## Themes

* [jQuery Mobile iOS7 Theme](https://github.com/ququplay/jquery-mobile-ios7-theme)

## Blogs

*[gajotres](http://www.gajotres.net/), [Top 7 Mobile application HTML5 frameworks](http://www.gajotres.net/top-7-mobile-application-html5-frameworks/)

