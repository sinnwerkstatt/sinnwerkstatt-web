CSS
===

Table of Contents
-----------------
1. [Approach](#approach)
2. [Format](#format)
  1. [Property Order](#property-order)
3. [Selectors](#selectors)
4. [Layout](#layout)
5. [Research](#research)
5. [Not Decided](#not-decided)


<a name="approach"></a>
1. Approach
-----------

This CSS coding guide is created based on:
* CSS best practices.
* the [Topcoat Coding Guidlines](https://github.com/topcoat/topcoat/wiki/Coding-Guidelines).
* our own needs.


<a name="format"></a>
2. Formatting
-----------

Use consistent formatting in order to increase understanding and legibility.

* One selector per line
* Use one space between selector and first bracket
* Use one space between property and value after `:`
* Always add a semicolon after property value
* Use double quotes
* Do not specify units for a zero value
* Include a space after each comma in a comma separated property list
* Separate each ruleset by an empty line

```css
.selector-1,
.selector-2 {
    box-sizing: border-box;
    display: block;
    font-family: helvetica, arial, sans-serif;
    color: #333;
    background: 0 0 #666 no-repeat url("../img/bg_img.png");
}

.selector-a,
.selector-b {
    padding: 10px;
}

```

<a name="property-order"></a>
2.1. Property Order
-----------

Property order should be in [2][structural](#2) order of importance.

```css
.selector {
    /* Positioning */
    position: absolute;
    z-index: 10;

    /* Display & Box Model */
    display: inline-block;
    overflow: hidden;
    box-sizing: border-box;
    width: 100px;
    height: 100px;
    padding: 10px;
    border: 10px solid #333;
    margin: 10px;

    /* Visual styles */
    background: #000;
    color: #fff;
    font-family: sans-serif;
    font-size: 16px;
    text-align: right;

    /* Vendor prefixed styles */
    -webkit-user-select: none;
}
```



<a name="selectors"></a>
3. Selectors
------------

TopCoat is designed to be modular and component focused. The styles are created to be
as portable as possibe while keeping performance as the top goal.

* Do not use IDs. They decrease [5][portability](#5)
```css
    /* NO */
    #header {
        position: absolute;
    }

```

* Do not over qualify selectors because it impacts [1][performance](#1)
```css
    /* NO */
    ul li.button.large.blue {
        background: salmon;
    }
```

* Use class names for specificity to increase [1][performance](#1). Info: [Read more about](http://coding.smashingmagazine.com/2007/07/27/css-specificity-things-you-should-know/) and [calculate](http://josh.github.io/css-explain/) specificity.
```css
    /* YES */
    .list-item {
        border: 1px solid #666;
    }
```

* Use component oriented naming [3][conventions](#3)
```css

    /*
     * Base reset components
     * Use the naming convention:
     * {component}-{name}__{subcomponent}--{modifier}
     * 
     */

    /* Component */
    .button-group

    /* Component Modifier */
    .button-group--large

    /* Subcomponent */
    .button-group__button

    /* Subcomponent Modifier */
    .button-group__button--cta

    /*
     * Themed components
     * Use the naming convention:
     * {theme}-{component}-{name}__{subcomponent}--{modifier}
     */

    /* Component */
    .topcoat-button-group

    /* Component Modifier */
    .topcoat-button-group--large

    /* Subcomponent */
    .topcoat-button-group__button

    /* Subcomponent Modifier */
    .topcoat-button-group__button--cta

```



<a name="layout"></a>
4. Layout
------
Layout should be handled by a layout specific class. You should not mix layout and
visual styling in one class definition.

```css
.topcoat-header--dark {
    background: #c6c8c8;
}

/* ... Layout section */

.span-3 {
    width: 33.333%
}

```

```html
    <header class="topcoat-header--dark span-3"></header>
```


<a name="research"></a>
5. Research
--------

By importance of inclusion:

* [<a name="1">1</a>][Github CSS performance](https://vimeo.com/54990931) ([PDF](https://speakerdeck.com/jonrohan/githubs-css-performance))
* [<a name="2">2</a>][Idiomatic CSS](https://github.com/necolas/idiomatic-css)
* [<a name="3">3</a>][SUIT CSS component methodology](https://github.com/necolas/suit)
* [<a name="4">4</a>][KSS style comments](https://github.com/kneath/kss)
* [<a name="5">5</a>][CSS Wizardy](https://github.com/csswizardry/CSS-Guidelines)
* [<a name="6">6</a>][CSS Property Order](http://css-tricks.com/poll-results-how-do-you-order-your-css-properties/)
* [<a name="7">7</a>][CSSLint](https://github.com/stubbornella/csslint)
* [<a name="8">8</a>][RECESS](http://twitter.github.com/recess/)
* [<a name="9">9</a>][Styleguide Reference list](http://css-tricks.com/css-style-guides/)


<a name="not-decided"></a>
6. Not Decided:
--------


* Do not use tag selectors. They decrease [5][portability](#5) and it can impact [1][performance](#1) _*see over qualified_
```css
    /* NO */
    header {
        color: blue;
    }
```
