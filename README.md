# The "breeze-client" package

This is the official package for the Breeze core client-side libraries, drawn from sources in the [home repository on github](https://github.com/Breeze/breeze.js "github: breeze.js").

To install with bower, open a terminal or command window and enter:

`bower install breeze-client`

>Case matters! Be sure to spell "breeze-client" in all lowercase.

[Learn more about Breeze](http://www.getbreezenow.com/breezejs "breezejs").

## Structure

The most widely used Breeze client library is "breeze.debug.js". It conbines both the
base Breeze functionality and the default adapters for Knockout and Angular applications.

>but not the "breeze.bridge.angular" adapter used by most Angular apps. See next.

### adapters
The "adapters" directory holds scripts for every core Breeze adapter. Adapters implement breeze feature-extension-points for specific application environments.  For example, the "breeze.ajax.jQuery.js" script provides a jQuery implementation of
the Breeze "ajax" interface for communicating with remote services via XMLHttpRequest (XHR).

Some of these adapters (like "breeze.ajax.jQuery.js") are embedded in
"breeze.debug.js". You should not load them again if you're loading "breeze.debug.js".

Others (like "breeze.bridge.angular" and "breeze.modelLibrary.backbone.js") are not embedded. You will have to load these adapter scripts separately if you need their capabilities.

If you choose to run with "breeze.**base**.debug.js" instead of "breeze.debug.js" (see next), you must load *every* required adapter script separately.

### build

The "build" directory holds the scripts generated from the core Breeze sources.

* **breeze.debug.js** - the base client library and selected default adapters.
* **breeze.base.debug.js** - the base client library without any adapters.
* **breeze.min.js** - the minified default client library.
* **breeze.base.min.js** - the minified base client library.

## No Breeze Labs!

This package **does not include the Breeze Labs**.

**Breeze Labs**