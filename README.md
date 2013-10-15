# Responsive Web Design - Demo

This demo is intended to present the basics of responsive web design.

This demo was given as part of the [Educause 2013 Responsive Web Design workshop](http://www.educause.edu/annual-conference/2013/seminar-18a-responsive-web-design-separate-registration-required).

## Usage

The demo is divided into five steps:

1. Converting fixed-width designs to fluid-width designs
2. Adding media queries for collapse
3. Adding media queries for intermediate and extra-large behaviors
4. Hiding content to reduce scrolling
5. Using a polyfill to present responsive images

To this end, there is a `base.css` file that defines the fixed width style, 
and then steps 1 - 4 may be arrived at by adding `step-X.css` files where `X` 
is the step to arrive at, plus all earlier steps.

For example, the `head` for step 3 reads:

```html
<head>
<meta charset="UTF-8">
<title>Travel Blog</title>
<link href="./css/base.css" rel="stylesheet" type="text/css">
<link href="./css/step-1.css" rel="stylesheet" type="text/css">
<link href="./css/step-2.css" rel="stylesheet" type="text/css">
<link href="./css/step-3.css" rel="stylesheet" type="text/css">
</head>
```

For step 5, add the Javascript files in `js` to the `head` as well:

```html
<head>
<meta charset="UTF-8">
<title>Travel Blog</title>
<link href="./css/base.css" rel="stylesheet" type="text/css">
<link href="./css/step-1.css" rel="stylesheet" type="text/css">
<link href="./css/step-2.css" rel="stylesheet" type="text/css">
<link href="./css/step-3.css" rel="stylesheet" type="text/css">
<link href="./css/step-4.css" rel="stylesheet" type="text/css">
<script type="text/javascript" src="js/matchMedia.js"></script>
<script type="text/javascript" src="js/matchMedia.addListener.js"></script>
<script type="text/javascript" src="js/picturefill.js"></script>
</head>
```

Additionally, for step 5, convert the main content images from an `img` tag to 
using the Picturefill syntax such as:

```html
<span data-picture data-alt="">
      <span data-src="images/city1-360.jpg"></span>
      <span data-src="images/city1-480.jpg" data-media="(min-width: 361px)"></span>
      <span data-src="images/city1.jpg"     data-media="(min-width: 481px)"></span>
      <noscript>
          <img src="images/city1.jpg" alt="">
      </noscript>
</span>
``` 

## License

This demo is open-source software licensed under the BSD 3-clause license. The 
full text of the license may be found in the `LICENSE` file.

### Credits

This demo was written by Eric Bollens and Amos Williams.

This demo takes advantage of several outstanding open-source products:

* [Respond.js](https://github.com/scottjehl/Respond/blob/master/respond.src.js) - MIT/GPLv2 - Scott Jehl (c) 2012-13
* [Picturefill](https://github.com/scottjehl/picturefill/blob/master/picturefill.js) - MIT/GPLv2 - Scott Jehl (c) 2012
* [matchMedia.js](https://github.com/paulirish/matchMedia.js/blob/master/matchMedia.js) - MIT/BSD - Scott Jehl, Paul Irish, Nicholas Zakas, David Knight (c) 2012
* [matchMedia.addListener.js](https://github.com/paulirish/matchMedia.js/blob/master/matchMedia.addListener.js) - MIT/BSD - Scott Jehl (c) 2012

