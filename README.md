# [volcareso.js](https://volcareso.github.io/volcareso.js/)

[![Join the chat at https://gitter.im/volcareso-js/volcareso.js](https://badges.gitter.im/volcareso-js/volcareso.js.svg)](https://gitter.im/volcareso-js/volcareso.js?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

_A multi talented JavaScript library._

## Usage

```html
<script src="https://volcareso.github.io/volcareso.js/volcareso.min.js"></script>
```

That's it! The power is in your hands now!

### Selecting elements

```javascript
$$('<css_compatible_selector>').action();
```

where `<css_compatible_selector>` is a selector that you'd use to select elements in CSS \([see here](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors)\), e.g: `#id_selector`, `.class-selector`, `tagname-selector` and `action` is any method (from below) that performs some action.

### Hiding elements

```javascript
$$('body').hide();
```

## Listening to events

```javascript
$$('element').on('eventName', function () {
  alert('i have ears!');
});
```

where, `eventName` is any event as [described here](https://developer.mozilla.org/en-US/docs/Web/Events#event_listing).

### Appending or prepending text to elements

```javascript
// appending
$$('element').append('appendedText');

// prepending
$$('element').prepend('prependedText');
```

### Reading and setting attributes:

```javascript
// reading attributes
$$('element').attr('class');

// settings attributes
$$('element').attr('class', 'foo_bar');
```

### Changing CSS properties

```javascript
$$('element').css('property', 'value');
// e.g.:
$$('element').css('text-align', 'center');
```

### Fetch remote content

```javascript
$$('element').load('https://url-to-file.com/abs/path/to/FILE.txt');

// load with credentials:
$$('element').load(
  'https://url-to-file.com/abs/path/to/FILE.EXT',
  'username',
  'password'
);
```

### Handling cookies

```javascript
$$().setCookie('cookieKey', 'cookieVal', 'expiryDate', 'path');

$$().getCookie('cookieKey');
```

### Append elements

```javascript
$$('elementToAppendTo').addElm('elem', 'id');
```

### Local Storage

```javascript
$$().storage('action', '[key]', '[value]');

/// action list:
/// "clear" clears the local storage (key, value not required)
/// "get" gets the item with specified key (value not required)
/// "set" set the key with the respective value
/// "remove" remove the item with the specified key (value not required)
```

## Toggle (hide and show state)

```javascript
$$('element').toggle();
```

## Text-to-speech

```javascript
$$().read('message'); // reads "message"

$$('element').read(); // reads the text inside 'element'
```

### Basic data about client

```javascript
$$().data.lang.userAgent.os.cookies.vender.online.version.mobileType.doNotTrack; //en_US //Mozilla/5.0 (Linux; Android 6.0.1; Moto G (4)) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.114 Mobile Safari/537.36" //linux x86_64 // true //Google.inc // true id online //5.0 //4g //true is turned on

$$().data; //returns all data in an object
```

## Fingerprinting (sort of):

```javascript
$$().fingerprint(key); //sets the fingetprint on the user machine
$$().checkFingerprint(key); // returns true if the fingerprints are matched (else false)

// e.g.:

if ($$().checkFingerprint('user1')) {
  console.log('not a new user');
} else {
  console.log('new user');
}

$$().fingerprint('user1');
```

### Custom elements

```javascript
$$().recycle('custom-element', '<p>an element </p>');
```

Now, when we use `<custom-element></custom-element>` anywhere in the html document, it will be replaced with the `html` markup given in the second parameter. This way you can reuse the same code again.

### Dynamic data (sort of a PoC)

```javascript
new react({
  el: 'body',
  data: {
    hello: 'world',
  },
});
// replaces {{ hello }} with world in element body
// inspired from Vue.js
```

### for contribution to this repo, see [contributing.md](https://github.com/volcareso/volcareso.js/blob/main/CONTRIBUTING.md)
