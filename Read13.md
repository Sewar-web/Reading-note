# local storage

* local storage is one of the areas where native client applications have held an advantage over web applications

* These values may be stored in the registry, INI files, XML files, or some other place according to platform convention

**Cookies were invented early in the web’s history, and indeed they can be used for persistent local storage of small amounts of data. But they have three potentially dealbreaking downsides:**

1. Cookies are included with every HTTP request, thereby slowing down your web application by needlessly transmitting the same data over and over


2. Cookies are included with every HTTP request, thereby sending data unencrypted over the internet (unless your entire web application is served over SSL)


3. Cookies are limited to about 4 KB of data — enough to slow down your application (see above), but not enough to be terribly useful


**What we really want is**

* a lot of storage space
* on the client
* that persists beyond a page refresh
* and isn’t transmitted to the server


* In the beginning, there was only Internet Explorer. 
* userData allows web pages to store up to 64 KB of data per domain, in a hierarchical XML-based structure.

* In 2002, Adobe introduced a feature in Flash 6 that gained the unfortunate and misleading name of “Flash cookies.” Within the Flash environment, the feature is properly known as Local Shared Objects. Briefly, it allows Flash objects to store up to 100 KB of data per domain. Brad Neuberg developed an early prototype of a Flash-to-JavaScript bridge called AMASS (AJAX Massive Storage System), but it was limited by some of Flash’s design quirks. By 2006, with the advent of ExternalInterface in Flash 8, accessing LSOs from JavaScript became an order of magnitude easier and faster. Brad rewrote AMASS and integrated it into the popular Dojo Toolkit under the moniker dojox.storage. 



* In 2007, Google launched Gears, an open source browser plugin aimed at providing additional capabilities in browsers. 
  

  * In the meantime, Brad Neuberg and others continued to hack away on dojox.storage to provide a unified interface to all these different plugins and APIs. By 2009, dojox.storage could auto-detect (and provide a unified interface on top of) Adobe Flash, Gears, Adobe AIR, and an early prototype of HTML5 storage that was only implemented in older versions of Firefox.


**INTRODUCING HTML5 STORAGE**

function supports_html5_storage() {
  try {
    return 'localStorage' in window && window['localStorage'] !== null;
  } catch (e) {
    return false;
  }
}



interface Storage {
  getter any getItem(in DOMString key);
  setter creator void setItem(in DOMString key, in any data);
};
Calling setItem() with a named key that already exists will silently overwrite the previous value. Calling getItem() with a non-existent key will return null rather than throw an exception.

Like other JavaScript objects, you can treat the localStorage object as an associative array. Instead of using the getItem() and setItem() methods, you can simply use square brackets. For example, this snippet of code:

var foo = localStorage.getItem("bar");
// ...
localStorage.setItem("bar", foo);
…could be rewritten to use square bracket syntax instead:

var foo = localStorage["bar"];
// ...
localStorage["bar"] = foo;
There are also methods for removing the value for a given named key, and clearing the entire storage area (that is, deleting all the keys and values at once).

interface Storage {
  deleter void removeItem(in DOMString key);
  void clear();
};




**TRACKING CHANGES TO THE HTML5 STORAGE AREA**
If you want to keep track programmatically of when the storage area changes, you can trap the storage event. The storage event is fired on the window object whenever setItem(), removeItem(), or clear() is called and actually changes something. For example, if you set an item to its existing value or call clear() when there are no named keys, the storage event will not fire, because nothing actually changed in the storage area.



**LIMITATIONS IN CURRENT BROWSERS**
In talking about the history of local storage hacks using third-party plugins, I made a point of mentioning the limitations of each technique, such as storage limits. I just realized that I haven’t mentioned anything about the limitations of the now-standardized HTML5 Storage. I’ll give you the answers first, then explain them. The answers, in order of importance, are “5 megabytes,” “QUOTA_EXCEEDED_ERR,” and “no.”

“5 megabytes” is how much storage space each origin gets by default. This is surprisingly consistent across browsers, although it is phrased as no more than a suggestion in the HTML5 Storage specification. One thing to keep in mind is that you’re storing strings, not data in its original format. If you’re storing a lot of integers or floats, the difference in representation can really add up. Each digit in that float is being stored as a character, not in the usual representation of a floating point number.

The most important part of this function is the caveat that I mentioned earlier in this chapter, which I’ll repeat here: Data is stored as strings. If you are storing something other than a string, you’ll need to coerce it yourself when you retrieve it. For example, the flag for whether there is a game in progress (gGameInProgress) is a Boolean. In the saveGameState() function, we just stored it and didn’t worry about the datatype:

localStorage["halma.game.in.progress"] = gGameInProgress;
But in the resumeGame() function, we need to treat the value we got from the local storage area as a string and manually construct the proper Boolean value ourselves:

gGameInProgress = (localStorage["halma.game.in.progress"] == "true");
Similarly, the number of moves is stored in gMoveCount as an integer. In the saveGameState() function, we just stored it:

localStorage["halma.movecount"] = gMoveCount;
But in the resumeGame() function, we need to coerce the value to an integer, using the parseInt() function built into JavaScript:

gMoveCount = parseInt(localStorage["halma.movecount"]);


BEYOND NAMED KEY-VALUE PAIRS: COMPETING VISIONS
While the past is littered with hacks and workarounds, the present condition of HTML5 Storage is surprisingly rosy. A new API has been standardized and implemented across all major browsers, platforms, and devices. As a web developer, that’s just not something you see every day, is it? But there is more to life than “5 megabytes of named key/value pairs,” and the future of persistent local storage is… how shall I put it… well, there are competing visions.

One vision is an acronym that you probably know already: SQL. In 2007, Google launched Gears, an open source cross-browser plugin which included an embedded database based on SQLite. This early prototype later influenced the creation of the Web SQL Database specification. Web SQL Database (formerly known as “WebDB”) provides a thin wrapper around a SQL database, allowing you to do things like this from JavaScript:

↶ actual working code in 4 browsers

openDatabase('documents', '1.0', 'Local document storage', 5*1024*1024, function (db) {
  db.changeVersion('', '1.0', function (t) {
    t.executeSql('CREATE TABLE docids (id, name)');
  }, error);
});