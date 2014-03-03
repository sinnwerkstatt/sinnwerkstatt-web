# Social links

Examples how to add social links to Django templates.

## Facebook
* [Share Dialog](https://developers.facebook.com/docs/plugins/share/)
* [Like Button](https://developers.facebook.com/docs/plugins/like-button/)

```html
<a class="share-link decoration-none" href="https://www.facebook.com/sharer/sharer.php?u={{ request.build_absolute_uri }}" target="_blank">
  <img class="pad-right-s" src="{% static "images/social-icons/facebook.png" %}"/>
</a>
```

## Twitter

```html
<a class="share-link decoration-none" href="http://twitter.com/home?status=Check out {{ request.build_absolute_uri }}" target="_blank">
  <img class="pad-right-s" src="{% static "images/social-icons/twitter.png" %}"/>
</a>
```

## Pinterest

```html
<a class="share-link decoration-none"
   href="http://pinterest.com/pin/create/button/?url={{ request.build_absolute_uri }}&amp;media={% if request.is_secure %}https://{% else %}http://{% endif %}{{ request.get_host }}{% thumbnail object.image 450x400 crop %}&amp;description=Your description"
   target="_blank">
  <img class="pad-right-s" src="{% static "images/social-icons/pinterest.png" %}"/>
</a>
```

## Google+

```html
<a class="share-link decoration-none" href="https://plus.google.com/share?url={{ request.build_absolute_uri }}" target="_blank">
  <img class="pad-right-s" src="{% static "images/social-icons/googleplus.png" %}" alt="Share on Google+"/>
</a>
```

## Common

### Javascript
Open the links in a small window

```javascript
$('.share-link').click(function () {
    window.open(this.href,
      '',
      'menubar=no,toolbar=no,resizable=yes,scrollbars=yes,height=600,width=600');
    return false;
});
```
### CSS
No text decoration

```css
.share-link:hover {
  text-decoration: none;
}
```
