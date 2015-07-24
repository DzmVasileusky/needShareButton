#needShareButton 1.0.0
##Do you need share button dropdown? Here you go!

###Short facts
* Pure Javascript, no need to use jQuery
* 21 social networks and mailto links
* 2 different view styles
* Easily configurable position of dropdown
* Possibility to set options via data-attributes
* Browsers: Firefox, Chrome, Safari, iOS, Android, IE9+

Written by: Dzmitry Vasileuski

###License
Released under the MIT license - http://opensource.org/licenses/MIT

##Getting started

###Step 1: Add required files from dist directory

Download the package from this repository and include needsharebutton.min.js and needsharebutton.min.css.

```html
<!-- needPopup Javascript file -->
<script src="js/needsharebutton.min.js"></script>
<!-- needPopup CSS file -->
<link href="css/needsharebutton.min.css" rel="stylesheet" />
```

###Step 2: Create HTML markup

Create an empty element, which will be the wrapper of our button and dropdown.
You can add data-attributes to easily configure script.

```html
<span id="share-button" class="need-share-button-default"></span>
```

###Step 3: Call needShareButton initialization

Just place `new needShareDropdown(document.getElementById('share-button'));` in your javascript code.

```javascript
new needShareDropdown(document.getElementById('share-button'));
```

##Customization

There are two ways to set settings.

The first way is to add data-attributes with `data-share` prefix.
```html
<div id="share-button" class="need-share-button-default" data-share-icon-style="box" data-share-networks="Mailto,Twitter,Pinterest,Facebook,GooglePlus,Linkedin"></div>
```
The second way is to send settings object with script initialization.
```javascript
new needShareDropdown(document.getElementById('share-button'), {
  iconStyle: 'box',
  boxForm: 'vertical',
  networks: 'Mailto,Twitter,Pinterest,Facebook,GooglePlus,Linkedin'
});
```

That's all. Please, enjoy to use.

###Options

**iconStyle**
View style
```
default: 'default'
options: 'default', 'box'
```

**boxForm**
In the box view you can configure links position
```
default: 'horizontal'
options: 'horizontal', 'vertical'
```

**position**
Dropdown position relatively to button
```
default: 'bottomCenter'
options: 'topLeft', 'topRight', 'topCenter', 'middleLeft', 'middleRight', 'bottomLeft', 'bottomRight', 'bottomCenter'
```

**buttonText**
Text on the share button
```
default: 'Share'
options: Any string
```

**url**
Shared page url
```
default: Current page url
options: Any url
```

**title**
Shared page title
```
default: Current page title
options: Any string
```

**image**
Shared page preview image
```
default: Current page preview image
options: Any image src
```

**description**
Shared page description
```
default: Current page description
options: Any string
```

**networks**
Which social network buttons to show
```
default: 'Mailto,Twitter,Pinterest,Facebook,GooglePlus,Reddit,Delicious,Tapiture,StumbleUpon,Linkedin,Slashdot,Technorati,Posterous,Tumblr,GoogleBookmarks,Newsvine,Pingfm,Evernote,Friendfeed,Vkontakte,Odnoklassniki,Mailru'
options: Any of the network name's from pervios row comma separated
```