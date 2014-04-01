##NEWS: jsPanel has a new homepage##

###[http://jspanel.de](http://jspanel.de/)###

Copyright &copy; 2014 Stefan Sträßer | [stefanstraesser.eu](http://stefanstraesser.eu)

For a bunch of examples and the api documentation please visit [jspanel.de](http://jspanel.de/)

<br><br>

## CHANGELOG ##

---

### Version 1.3.1 ###

**Bugfix** in the resize behaviour when using option.position with bottom and/or right

### Version 1.3.0 ###

**Bugfix** in option.size.width / option.size.height when using a function returning 0

**Changes:**

+ option.size.width < 150 will result in default width

+ option.size.height < 93 will result in default height

**Added functionality**

+ When using functions to calculate option.size.width/height or option.position.top/left/bottom/right the functions receive the jsPanel as argument

+ Start event of draggable feature has a function attached by default in order to make the draggable feature properly usable when using option.position.bottom/right in combination with option.size.width/height 'auto'

+ New method .front() - will replace .movetoFront() which is deprecated

---

### Version 1.2.0 ###

**Added options**

+ **option.autoclose** allows the jsPanel to close automatically after a specified time

+ **option.controls** allows to configure the buttons in the header

**Improved options:**

+ **size: { width: 'auto', height: 'auto' }** can now be abbreviated with **size: 'auto'**

+ **position: { top: 'auto', left: 'auto' }** can now be abbreviated with **position: 'auto'**

+ **position: { top: 'center', left: 'center' }** can now be abbreviated with **position: 'center'**

+ **position** now additionally accepts values for bottom and right **{ bottom: 0, right: 0 }**

+ **automatic centering** now also works when width and/or height are set to 'auto', unless loading content is delayed because of using an asynchronous ajax request or the callback function to load the content

+ **additional shortcuts for option.position:**<br>
'top left' | 'top center' | 'top right' | 'center right' | 'bottom right' | 'bottom center' | 'bottom left' | 'center left'

+ **overflow** now alternatively accepts a string to set the css property overflow

+ **resizable and draggable** can be disabled

---

### Version 1.1.1 ###

+ **Bugfix** Content area of the jsPanel did not resize when resizing a maximized jsPanel with the jQuery-UI resize handle.

+ **Change** For z-index management the script internally now uses the jQuery-UI method zIndex()

+ **Change** New clearfix css definition in _jsPanel.css_

---

### Version 1.1.0 ###

+ **Improvement:** Removed the settings for **_containment_** in the default settings objects for **_option.resizable_** and **_option.draggable_**.
The default settings are unnecessary and caused problems when the jsPanel was bigger in size than the containing parent element.

+ **Improvement:** Code for **_option.load_** improved. See the documentation for details.

+ **Improvement:** Correction in _jsPanel.css_

+ **Added functionality:** The settings object for **_option.ajax_** now optionally accepts functions that will be passed to _$.ajax().done()_, _$.ajax().fail()_, _$.ajax().always()_ and _$.ajax().then()_.
See the documentation for details on how to use this settings.

---

### Version 1.0.1 ###

+ **Bugfix:** Error when using **_option.id_** with a user defined function to generate an id for the jsPanel.