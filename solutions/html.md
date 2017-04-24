### 1) What does a ```doctype``` do?

The ```doctype``` tells the user agent (aka web browsers) what type of HTML document it is intended to parse. This makes sure the document will be parsed the same way by different browsers.

The simplest and most reliable doctype declaration to use is the one defined in HTML5:

```html
<!DOCTYPE html>
```

Read more: https://www.w3.org/QA/2002/04/valid-dtd-list.html


### 2) What's the difference between full standards mode, almost standards mode and quirks mode?

In **quirks mode**, layout emulates nonstandard behavior in Navigator 4 and Internet Explorer 5. This is essential in order to support websites that were built before the widespread adoption of web standards.

In **full standards mode**, the behavior is (hopefully) the behavior described by the HTML and CSS specifications.

In **almost standards mode**, there are only a very small number of quirks implemented.

Read more: https://developer.mozilla.org/en-US/docs/Quirks_Mode_and_Standards_Mode

### 3) What's the difference between HTML and XHTML?

XHTML is XML, HTML is not. XHTML's rules follow XML's stricter rules, like closing tag for each opening tag and attributes must have a value.

### 4) Are there any problems with serving pages as ```application/xhtml+xml```?

Serving pages as ```application/xhtml+xml``` will cause Internet Explorer 8 to show a download dialog box for an unknown format instead of displaying your page, as the first version of Internet Explorer with support for XHTML is Internet Explorer 9.

Read more: https://developer.mozilla.org/en-US/docs/Quirks_Mode_and_Standards_Mode#XHTML

### 5) How do you serve a page with content in multiple languages?

This is a tricky question. Not in the sense that the answer to it is difficult, but it requires interpretation. Note that a page with **content** in multiple languages is the same page with different sections in different languages, which isn't the same as interpreting this as serving a page in multiple languages, in which case you would consider multiple ways of serving it, like multiple files, each one in a different language. It may seem obvious until you google for this exact same question and read people's answers.

First of all, you should always use a language attribute on the ```html``` tag to declare the default language of the text in the page. When the page contains content in another language, add a language attribute to an element surrounding that content.

```html
<!DOCTYPE html>
<html lang="en-US">
  <!-- Content omitted for the sake of clarity -->
  <p>This is a paragraph in the default language, english.</p>
  <p lang="pt-BR">Enquanto que este é um parágrafo em português.</p>
</html>
```

As [W3C recommends](https://www.w3.org/TR/2007/NOTE-i18n-html-tech-lang-20070412/#ri20050208.095812479):

> In short, this document recommends that you always declare the language of content to support text-processing needs. We recommend that you do so using attributes in the html element (to set the default language for the whole document) and on any element containing content in a different language.

Read more: https://www.w3.org/International/questions/qa-html-language-declarations

https://html.spec.whatwg.org/multipage/dom.html#the-lang-and-xml:lang-attributes

### 6) What kind of things must you be wary of when design or developing for multilingual sites?

- Declare the language of content (ex: ```<html lang="en-US">```)
- If needed, setup right-to-left text direction by adding ```dir="rtl"``` to the ```html``` tag or only to the required elements
- Localize date and time formats
- Don't decide for the user their preferred language. Let the user choose, or at least change to another language
- Present language options
- Some languages are more "wordy". A button "add to cart" might be translated in Dutch to "aan winkelwagen toevoegen". Consider this when designing
- URL structure. You can identify your website using a country top-level domain (ccTLD) like .br for Brazil or .uk for United Kingdom. It's also possible to make the country clear in the URL using a subdomain (ex: france.example.com) or a subdirectory (eg: example.com/fr)

Read more: https://webdesign.tutsplus.com/articles/tips-for-designing-and-building-a-multilingual-website--cms-24708

https://www.w3.org/International/techniques/authoring-html?collapse

### 7) What are ```data-``` attributes good for?

```data-``` attributes allow us to store extra information on standard, semantic HTML. This information may be used by scripts or CSS.

```html
<section id="car" data-size="3"></section>
```

```js
const section = document.querySelector('#car');

section.dataset.size // "3"
```

```css
section[data-size='3'] { width: 300px; }
section::before { content: attr(data-size); }
```

Read more: https://developer.mozilla.org/en-US/docs/Learn/HTML/Howto/Use_data_attributes

https://www.sitepoint.com/use-html5-data-attributes/

### 8) Consider HTML5 as an open web platform. What are the building blocks of HTML5?

A non-exausting list of things brought by HTML5:

- Semantics, via new elements like ```main```, ```article```, ```section```, ```header```, etc
- Storage, with ```localStorage```  and ```sessionStorage```
- Conectivity, with WebRTC, web workers and web sockets
- Graphics, with the ```canvas``` element, support for SVG and WebGL
- Multimedia, with ```video``` and ```audio```
- new APIs like offline, web storage, drag-and-drop, history, geolocation
- new ```input``` types like ```tel```, ```email```, ```color```, ```range```

Read more: https://www.w3.org/TR/html5-diff/

https://developer.mozilla.org/pt-BR/docs/Web/HTML/HTML5

### 9) Describe the difference between a ```cookie```, ```sessionStorage``` and ```localStorage```.

```sessionStorage``` and ```localStorage``` are part of the Web Storage API and they are meant primarily for client-side storage, while ```cookies``` are primarily for reading server-side.

You can send data from the web storage to a server, but it has to be done purposefully, while ```cookies``` are sent to the server within every request.

```sessionStorage``` stores data during the page session so, if you close the tab/window, data will be deleted. ```localStorage``` also stores data on the client-side, but data persists even when the browser is closed and reopened. ```cookies``` 

```cookies``` only allow you to store strings. ```sessionStorage``` and ```localStorage``` allow you to store JavaScript primitives but not Objects or Arrays (it is possible to JSON serialise them to store them using the APIs).

Read more: https://html.spec.whatwg.org/multipage/webstorage.html#the-sessionstorage-attribute

https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API

https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies

### 10) Describe the difference between ```<script>```, ```<script async>``` and ```<script defer>```.

```<script>``` is the HTML element used to embed or reference an executable script.

```<script async>``` indicates to the browser that it should, if possible, execute the script asynchronously.

```<script defer>``` indicates to the broswer that it should execute the script after the document has been parsed, but before firin DOMContentLoaded.

Read more: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script

### 11) Why is it generally a good idea to position CSS ```<link>```s between ```<head></head>``` and JS ```<script>```s just before ```</body>```? Do you know any exceptions?

By default, CSS is treated as a **render blocking** resource, which means that the browser won't render any processed content until the CSSOM is constructed.

The browser steps on rendering:

1. Process HTML markup and build the DOM tree.
1. Process CSS markup and build the CSSOM tree.
1. Combine the DOM and CSSOM into a render tree.
1. Run layout on the render tree to compute geometry of each node.
1. Paint the individual nodes to the screen.

If either the DOM or CSSOM were modified, you would have to repeat the process in order to figure out which pixels would need to be re-rendered on the screen.

By default, JavaScript execution is **parser blocking**. When the browser encounters a script tag, DOM construction pauses until the script finishes executing. Also, JavaScript exectution pauses until the CSSOM is ready.

The script is executed at the exact point where it is inserted in the document. When the HTML parser encounters a script tag, it pauses its process of constructing the DOM and yields control to the JavaScript engine; after the JavaScript engine finishes running, the browser then picks up where it left off and resumes DOM construction.

In other words, our script block can't find any elements later in the page because they haven't been processed yet! Or, put slightly differently: executing our inline script blocks DOM construction, which also delays the initial render.

Read more: https://html.spec.whatwg.org/multipage/semantics.html#the-link-element

https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css

https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript

### 12) What is progressive rendering?

It's the name given to techniques for rendering content as soon as possible.

Read more: https://jakearchibald.com/2016/streams-ftw/

https://medium.com/ben-and-dion/progressive-rendering-a-killer-and-under-appreciated-feature-of-the-web-97c789b608c1

### 13) Have you used different HTML templating languages before?

This one is personal, but here are some HTML templating languages:

- [Mustache](https://mustache.github.io/)
- [Handlebars](http://handlebarsjs.com/)
- [Pug](https://pugjs.org)
- [EJS](http://www.embeddedjs.com/)

### 14) What were some of the key goals and motivations for the HTML5 specification?

- Better support for web applications
- Make web content authoring more uniform
- Native integration with interfaces like GPS, camera, etc
- Eliminate plugins

### 15) What are some of the key new features in HTML5?

Web workers, offline storage, drag-and-drop, new semantic elements, audio and video.

### 16) What are “web workers”?

Web Workers are a mechanism by which a script operation can be made to run in a background thread separate from the main execution thread of a web application. The advantage of this is that laborious processing can be performed in a separate thread, allowing the main (usually the UI) thread to run without being blocked/slowed down.

Read more: https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API

https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Using_web_workers

### 17) How do you indicate the character set being used by an HTML5 document? How does this differ from older HTML standards?

By placing the following meta right after ```<head>```:

```html
<meta charset="utf-8">
```

This replaces the need for ```<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">``` although that syntax is still allowed.

Read more: https://www.w3.org/TR/html5-diff/#character-encoding

[Declaring the character set with the <meta charset>](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5/Introduction_to_HTML5#Declaring_the_character_set_with_the_<meta_charset>)