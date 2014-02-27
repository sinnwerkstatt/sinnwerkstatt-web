# Django Templates

## Cookies

### Server-side

Read:

* ``self.request.COOKIES.get('cookie_name')``

### Client-side

Set with [jquery.cookie](https://github.com/carhartl/jquery-cookie):

* ``$.cookie('cookie_name', 'cookie_value');``


## Comparison

### String and Integer
* ``{% if ìnt_value == str_value|add:0 %}``

## Quality Guidelines

### Editor
* If the user enters a text in the Django admin, always display this text with the filters ```linebreaksbr|urlize```, e.g. ```{{ object.text|linebreaksbr|urlize }}```

### Translations

### URLs
