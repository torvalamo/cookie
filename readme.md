# Cookie

Add to your document:

```html
<head>
  <script src="cookie.js"></script>
</head>
```

This adds a `cookie` function to the global `window` object.

## Usage:

To set a cookie:

```js
cookie(key, value, ttl)

// Set myCookie=123 that expires in one hour
cookie('myCookie', 123, 3600)
> true

// Set yourCookie=456 that expires at session end
cookie('yourCookie', 456)
> true

// Set hisCookie=789 that expires next year
var d = new Date()
d.setUTCFullYear(d.getUTCFullYear()+1)
cookie('hisCookie', 789, d.toUTCString())
> true
```

To get a cookie:

```js
cookie(key)

// Get myCookie
cookie('myCookie')
> 123

// Get an unknown cookie
cookie('theirCookie')
> null
```

To unset/delete a cookie:

```js
cookie(key, null)

// Delete hisCookie
cookie('hisCookie', null)
> true
```

# Props

This lib is just a stripped down version of the small framework found at https://developer.mozilla.org/en-US/docs/Web/API/Document/cookie for use with my own projects. If you like it, feel free to use it as you will.

# License

Knock Yourself Out License v1.0
by torvalamo

KNOCK YOURSELF OUT.