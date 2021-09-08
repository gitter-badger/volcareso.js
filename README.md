# [volcareso.js](https://volcareso.github.io/volcareso.js/)
A multi talented Javascript library
## IMPORT:
``` html
<script src="https://volcareso.github.io/volcareso.js/volcareso.js"></script>
```
### THATS IT! THE POWER IN YOUR HANDS NOW!

## SELECTION:
``` javascript
$$('selected element').action();
// selected element means => .by_class | #by_id | by_tageName
```

## DEMO:
``` javascript
$$('body').hide();
```

## ADD AN EVENT LISTENER:
``` javascript 
$$('element').on('eventName', function(){
alert('i have ears!');
})
```

## APPEND OR PREPEND STUFF:
## APPEND:
``` javascript
$$('element').append('appendedText');
```

## PREPEND:
``` javascript
$$('element').prepend('prependedText')
```

## ATTRIBUTES:
``` javascript
$$('element').attr('class')
// returns body (or the class specified)

$$('element').attr('class', 'foo_bar')
// sets properties to values
```

## CHANGING CSS:
``` javascript
$$('element').css(propertie, value)
EX:
$$('element').css('text-align', 'center')
```

## AJAX:
### LOAD REMOTE FILE CONTENT:
``` javascript
$$("element").ajax("https://url-to-file.com/TXT.txt", "get")
// sets the innerHTML value to the remote file value (changed the text)
```

## COOKIES:

#### SET COOKIE:
``` javascript
$$().setCookie("username", "hashtag", "session", "/"); //key, value, expires, path
```

#### GET COOKIES:
``` javascript
$$().getCookie("username");
//returns "hashtag"
```

## ADD ELEMENT:

``` javascript
$$('elementToAppendTo').addElm('p', 'idAssigned')
// element added
```

### ACCESS USING:
``` javascript
$$('#idAssigned').action();
```

## LOCAL STORAGE:

``` javascript
$$().storage(action, key, value)

// action list:
// "clear" clears the local storage
// "get". Gets the iten with specified key
// "set" set the key with the respective value
// "remove" remove the item with the specified key
```

## TOOGLE HIDE AND SHOW:

``` javascript
$$(".element").toogle();
```

## READ MESSAGES AND TEXT IN ELEMENTS:

``` javascript
$$().read("message");
OR READ THE TEXT INSIDE AN ELEMENT

$$('body').read();
```

NOTE: THE ELEMENT SHOULDNT HAVE SOME HTML CODE ELSE THAT WOULS BE ALSO READ!

## DATA COLLECTION (BASIC):

``` javascript
$$().data
  .lang //en_US
  .userAgent //Mozilla/5.0 (Linux; Android 6.0.1; Moto G (4)) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.114 Mobile Safari/537.36"
  .os //linux x86_64
  .cookies // true
  .vender //Google.inc
  .online // true id online
  .version //5.0
  .mobileType //4g
  .doNotTrack //true is turned on

  $$().data //returns all data in a json format
```

## FINGERPRINTING (KIND OF):

``` javascript
$$().fingerprint(key); //sets the fingetprint on the user machine
$$().checkFingerprint(key); // trturns true id the fingerprints are matched (else false)

//example

if ($$().checkFingerprint('user1')) {
console.log('not a new user');
}else{
console.log('new user');
}

$$().fingerprint('user1');
```

## REUSABLE COMPONENTS:

#### MAKE A COMPONENT:
``` javascript
$$().recycle('custom-element', '<p>an element </p>')
```

NOW WHEN YOU DECLARE `<custom-element></custom-element>`
IT WILL POPULATE WITH THE HTML MARKUP GIVEN IN THE SECOND SECTION

THIS WAY, YOU CAN REUSE THIS CODE FROM A SINGLE FILE


## REACTIVE DATA
``` javascript
new react({
  el: 'body', 
  data: {
    hello: 'world'
  }
})

// replaces {{ hello }} with world in element body
// inspired from vue.js
```
