# Tobi
[![Version](https://img.shields.io/badge/version-1.6.1-0437fd.svg)](https://github.com/rqrauhvmra/Tobi/releases)
[![License](https://img.shields.io/badge/license-MIT-0437fd.svg)](https://github.com/rqrauhvmra/tobi/blob/master/LICENSE.md)
![Dependecies](https://img.shields.io/badge/dependencies-none-0437fd.svg)

Simple lightbox script without dependencies.

[Play on CodePen](https://codepen.io/collection/nbqJVV)

![.flex__*](https://rqrauhvmra.com/tobi/snapshot.png)

## Features

- No dependencies
- Simple and light-weight
- Keyboard support: Prev/Next keys allows to navigate through items, close the lightbox with the escape key
- Touch gestures: Drag/Swipe to navigate through items, close the lightbox with a vertical drag/swipe
- Support for images, iframes and inline HTML

## Install

### Download

CSS: `css/tobi.min.css` minified, or `css/tobi.css` un-minified

JavaScript: `js/tobi.min.js` minified, or `js/tobi.js` un-minified

### Package managers

npm: `npm install rqrauhvmra__tobi --save`

## Usage

Initialize the script by running:

```js
var tobi = new Tobi()
```

The HTML code may look like this:

```html
<a href="path/to/image.jpg" class="lightbox">
  <img src="path/to/thumbnail.jpg" alt="I am a caption">
</a>
```

or

```html
<a href="path/to/image.jpg" class="lightbox">
  Open image
</a>
```

For inline HTML the HTML code may look like this:

```html
<a href="#" data-type="html" data-target="#selector" class="lightbox">
  Open HTML content / video or something else
</a>

<div id="selector">
  // ...
</div>
```

For iframes the HTML code may look like this:

```html
<a href="https://www.wikipedia.org/" data-type="iframe" class="lightbox">
  Open Wikipedia
</a>
```

## Options

You can pass an object with custom options as an argument.

```js
var tobi = new Tobi({
  captions: false
})
```

The following options are available:

| Property | Type | Default | Description |
| --- | --- | --- | --- |
| selector | string | ".lightbox" | All elements with this class triggers the lightbox. |
| captions | bool | true | Display captions, if available. |
| captionsSelector | "self", "img" | "img" | Set the element where the caption is. Set it to "self" for the `a` tag itself |
| captionAttribute | string | "alt" | Get the caption from given attribute. |
| nav | bool, "auto" | "auto" | Display navigation buttons. "auto" hides buttons on touch-enabled devices. |
| navText | string | ["inline svg", "inline svg"] | Text or HTML for the navigation buttons. |
| close | bool | true | Display close button. |
| closeText | string | "inline svg" | Text or HTML for the close button. |
| counter | bool | true | Display current image index |
| keyboard | bool | true | Allow keyboard navigation. |
| zoom | bool | true | Display zoom icon. |
| zoomText | string | "inline svg" | Text or HTML for the zoom icon |
| docClose | bool | true | Closes the lightbox when clicking outside |
| swipeClose | bool | true | Swipe up to close lightbox |
| scroll | bool | false | Hide scrollbars if lightbox is displayed |
| draggable | bool | true | Use dragging and touch swiping |
| threshold | number | 20 | Touch and mouse dragging threshold (in px) |

## API

```javascript
var tobi = new Tobi({
  // Options
})

tobi.open(2)  // Opens the lightbox on image 3 (first is 0)
tobi.next()   // Shows the next image in the lightbox
tobi.prev()   // Shows the previous image in the lightbox
tobi.close()  // Closes the lightbox

// Adds an element dynamically
var newElement = document.querySelector('.new-image')
tobi.add(newElement)
```

## Browser support

Tobi has been tested in the following browsers (all the latest versions):

- Firefox
- Firefox on Android
- Chrome
- Chrome on Android
- Safari
- Internet Explorer
- Edge

## Missing stuff

- Possibility to group
- Better dragging / swiping

## Contributing

- Report issues
- Open pull request with improvements
- Spread the word

## Notes

If you do anything interesting with this code, please let me know. I'd love to see it.