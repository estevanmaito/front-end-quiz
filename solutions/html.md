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

As the [W3C recommends](https://www.w3.org/TR/2007/NOTE-i18n-html-tech-lang-20070412/#ri20050208.095812479):

> In short, this document recommends that you always declare the language of content to support text-processing needs. We recommend that you do so using attributes in the html element (to set the default language for the whole document) and on any element containing content in a different language.

Read more: https://www.w3.org/International/questions/qa-html-language-declarations

https://html.spec.whatwg.org/multipage/dom.html#the-lang-and-xml:lang-attributes