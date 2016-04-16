# jQuery Image Reader

[![Join the chat at https://gitter.im/indosystem/jquery-image-reader](https://badges.gitter.im/indosystem/jquery-image-reader.svg)](https://gitter.im/indosystem/jquery-image-reader?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
A jQuery plugin that previews image very fast without needing to upload to your server.

This plugin implement FileReader API so you can asynchronously read the contents and avoid server uploads of raw user files.  You can also pre-treat content before you manually upload user content to your servers.

## Demo
[http://indosystem.github.io/jquery-image-reader](http://indosystem.github.io/jquery-image-reader)

## Usage
```html
<!-- HTML -->
<input type="file" id="upload-file" multiple /><br/>
<div id="image-preview"></div>
```

```js
// JS
$('#upload-file').imageReader();

// or
$('#upload-file').imageReader({
  destination: '#image-preview'
});

// callback
$('#upload-file').imageReader({
	onload: function(img) {
		// your callback code
		console.log({
			width: img.width,
			height: img.height
		});
		$(img).css('margin-top', '20px');
	}
});
```

## Install
```
bower install jquery-image-reader
```

## Browser compatibility
The Uncompressed file implement new features from the JavaScript ECMA-262 specification (ES6) while the compressed file has transpiled using Babel.js into equivalent code.
 
Tested on Chrome 49, Safari 9.1, Firefox 43. 

[https://developer.mozilla.org/en-US/docs/Web/API/FileReader#Browser_compatibility] (https://developer.mozilla.org/en-US/docs/Web/API/FileReader#Browser_compatibility)

## License
The MIT License (MIT)
