# Meteor-ribbon

Nitro Ribbon packaged for Meteor. Nitro Ribbon is a user interface element inspired
by Microsoft Office for Mac OSX. The original package can be found at
[https://github.com/NitroLabs/nitro-ribbon](https://github.com/NitroLabs/nitro-ribbon).

# Demo
A live demo of the interface is available here [ribbon.meteor.com](http://ribbon.meteor.com).
The source code for this demo is available at https://github.com/NitroLabs/meteor-ribbon-demo

# Usage
Install from atmoshpere:

```sh
meteor add nitrolabs:ribbon
```

Usage instructions the same as
[https://github.com/NitroLabs/nitro-ribbon](https://github.com/NitroLabs/nitro-ribbon)
except the style and javascript files a automatically included by this package.

```html
<head>
</head>

<body>
    {{>NitroRibbon}}
</body>

<template name="NitroRibbon">
    <div class="nitro-ribbon" data-role="tabs">
        <div class="ribbon-header"></div>
        <div class="ribbon-content"></div>
    </div>
</template>
```

Build the menu once Meteor has rendered the page

```javascript
Template.NitroRibbon.rendered = function(){
	var a = $('.nitro-ribbon');
	a.ribbon(config);

	// Bind events to the menu buttons
	a.ribbon('folder-button').click(function(event){
		console.log('Folder button clicked');
	});
}
```

# Development
This package is actively maintained and supported by [NitroLabs](http://www.nitrolabs.com/).
Pull requests and feature suggestions welcome.


# License
Apache 2.0