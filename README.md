ondemand.js
===========

A minimalistic asynchronous script loader for modern desktop &amp; mobile browsers

What? Another one?!
-------------------

Yep. There are tons of loaders that do useful stuff like dependency management or dealing with old IE, so I decided to write a tiny script that does only one simple thing – loads a script and fires a queue of callbacks when done. Oh, and if the same script is requested again, it won't load it twice. No more features, less than 100 lines of annotated source.
