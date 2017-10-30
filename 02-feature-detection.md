# Feature Detection



Modern web development places less reliance on a feature detection library, but one is still sometimes useful if you have to support old browsers.

1. Go to the [Modernizr](https://modernizr.com) web page. Download the development version of Modernizr.

2. Create a new web page. Include in it:

    1. Modernizr (at the top of the page), and
    2. a “no-js” classname in your <html> element.



## Detecting Support for JavaScript Features

Add a JavaScript that checks the Modernizr object:

``` javascript
if (Modernizr.cryptography) {
	// script to run if cryptography is supported
} else {
	// script to run if cryptography is not supported
}
```

In the body of the if statement, alert the user with a message, saying whether or not cryptography is supported.


## Loading a Polyfill

Modernizr doesn’t just detect features (whether CSS or JavaScript). It enables you to load polyfills if a feature isn’t available.

This part of Modernizr is based on [yepnope](yepnopejs.com). In Modernizr, it’s called Modernizr.load. So for example, if geolocation is available, we just use it; if not, we load a geolocation polyfill:

``` javascript
Modernizr.load({
  test : Modernizr.geolocation,
  yep  : 'normal.js',
  nope : ['polyfill.js', 'wrapper.js']
});
```

The “yep” means “yes, this feature is already supported by the browser”, and if so we just load ‘normal.js’. If “nope”, we load other files instead.

Go to https://github.com/Modernizr/Modernizr/wiki/HTML5-Cross-Browser-Polyfills and browse through some of the available polyfills.

## Stretch Task 1

If time is available, download a polyfill and use Modernizr.load to load it if the browser does not support that feature.

One feature you could try is the `<dataset>` element if you have a browser that doesn't support it, perhaps with [this](https://github.com/Fyrd/purejs-datalist-polyfill) polyfill.

## Stretch Task 2

You can also perform feature detection manually. This can be better if you only have one or two features to detect and it's just not worth the extra overhead of loading Modernizr.

To feature detect manually, see this [MDN](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Cross_browser_testing/Feature_detection#JavaScript) table.

Try to find a feature from this list that may or may not be supported in your browsers:

- geolocation
- `<input type="color">`
- custom protocol handling
- accept attribute for file input
- dialog element
- ambient light sensor
- beacon API
- BroadcastChannel
- Service Workers
