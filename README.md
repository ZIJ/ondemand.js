ondemand.js
===========

A minimalistic asynchronous script loader for modern desktop &amp; mobile browsers

What? Another one?!
-------------------

Yep. There are tons of loaders that do useful stuff like dependency management or dealing with old IE, so I decided to write a tiny script that does only one simple thing – loads a script and fires a queue of callbacks when done. Oh, and if the same script is requested again, it won't load it twice. No more features, less than 100 lines of annotated source.

Usage
-----

```javascript
ondemand.require("./js/bigScript.js", function()){
	// first handler called just after script is loaded and executed
	console.log("bigScript.js available 1");
});

ondemand.require("./js/bigScript.js", function()){
	// second handler runs just after first one 
	console.log("bigScript.js available 2");
});

// somewhen later
ondemand.require("./js/bigScript.js", function()){
	// third handler executes immediately
	console.log("bigScript.js available 3");
});
```