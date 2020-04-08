# Creativa - Popup
This is a simple library that allows you to create awesome popups importing just one JavaScript file.
## Getting started
You can import the JS file in two ways:
1. Using the HTTPS link to the file: https://creativajs.altervista.org/popup/creativa-popup.js
2. With offline file. If you want to use the offline file just download the archive here and import the **creativa-popup.js** file in your HTML.
## Where is the CSS?
The CSS will be automatically included from the **creativa-popup.js** file inside the HTML head.
## Responsive
The popup will adapt to every screen.
## Tested browsers
- Chrome
- Firefox
- Microsoft Edge
## Examples
You can download the archive from GitHub and try the **example.html** file.
## Basic syntax
```
popup('title', 'text', 'icon', 'image', extra);
```
- ### Title
This is a simple string that defines the title for the popup.
- ### Text
Here you can write the plain text that will be shown inside the popup.
- ### Icon
This parameter defines the popup icon that will be on top of the box. You can use default icons:
- info
- success
- error

...or you can put your own URL to the image of the icon (png, jpg, gif).
- ### Image
Here you can write the URL of an image that will be shown inside the popup.
- ### Extra
This is an object where you can specify other parameters to personalize the popup.
- **Content:** you can put a string that specify custom content for the poup (such as HTML, or other text) that will be shown under the plain text. In order to use this parameter you have to specify another parameter: **isPage**: this is a boolean that says if the content is plain text content or it is an URL to another page that will be loaded as content inside the popup.
```
// Including plain text content
popup('Title', 'Text', 'icon', 'image', { content: '<button>Test</button>', isPage: false }

// Including content from another page
popup('Title', 'Text', 'icon', 'image', { content: 'another-page.html', isPage: true }
```
- **Unclosable popup:** you can specify this parameter to avoid the popup to close.
```
popup('Title', 'Text', 'icon', 'image', { isBlocked: true }
```
- **Open/close animations:** the default open/close animation for the popup is the **fade** but you can set other default animations:
  - bubble
  - card-left
  - card-right
```
popup('Title', 'Text', 'icon', 'image', { openAnimation: 'card-left', closeAnimation: 'card-right' }
```
... or you can create your own animation inside your CSS file. Just give a name to the animation an then add *-popup-animation-open* or *-popup-animation-close*; for example, if my animation is called **dragon** I'll create the CSS animations with these names: **dragon-popup-animation-open** and **dragon-popup-animation-close** and inside the popup function I'll set the **dragon** string.
- **Custom size:** you can use different width and height for the popup.
```
popup('Title', 'Text', 'icon', 'image', { width: '300px', height: '400px' }
```
This is CSS so you can use every type of unit of measure (px, %, em ecc...)
## Conclusions
Of course you can use every option you want and mix them together.