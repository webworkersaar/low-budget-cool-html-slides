<!-- .slide: data-state="layout-title" data-transition="zoom" -->

# ![Title](../images/title-logo.jpg)

## HTML <del>sucks</del> <ins>rocks</ins>!

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# `<a>` Element `ping` Attribute

<blockquote>
 <i class="fa fa-quote-left text-secondary " aria-hidden="true"></i>
A space-separated list of URLs. When the link is followed, the browser will send POST requests with the body PING to the URLs. Typically for tracking.
</blockquote>

Use-cases: Tracking user behaviour

JS Alternative: [Beacon API](https://developer.mozilla.org/en-US/docs/Web/API/Beacon_API)

---

# `<a>` Element `ping` Attribute

## Example 1

```html
<a
  href="#/2/0/2"
  ping="https://20210301webworkersaar.requestcatcher.com/callbacks/myping"
>
  `ping` Example with local links
</a>
```

<a href="#/2/0/2" ping="https://20210301webworkersaar.requestcatcher.com/callbacks/myping" >`ping` Example with local links</a>

<iframe src="https://20210301webworkersaar.requestcatcher.com/"
     style="width:100%; height:500px; border:0; border-radius: 4px; overflow:hidden;"
     title="a-ping-attribute"
     allow="accelerometer; ambient-light-sensor; camera; encrypted-media; geolocation; gyroscope; hid; microphone; midi; payment; usb; vr; xr-spatial-tracking"
     sandbox="allow-forms allow-modals allow-popups allow-presentation allow-same-origin allow-scripts"
   ></iframe>
---

# `<a>` Element `ping` Attribute

## Example 2

<a href="https://codesandbox.io/s/a-ping-attribute-spb95?file=/src/index.js" target="_blank">Another `ping` Example - external links</a>

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# `<a>` Element `download` Attribute

<blockquote>
 <i class="fa fa-quote-left text-secondary " aria-hidden="true"></i>
Prompts the user to save the linked URL instead of navigating to it. Can be used with or without a value.
</blockquote>

Without specific filename: `<a href="..." download>`

With filename: `<a href="..." download="foo.html">`

<code class="code-primary">Use-case</code> If you don't want to open the file inplace with an embedded viewer..

<code class="code-primary">Alternative</code> Server side content-disposition...?

<code class="code-info">Note:</code> This only works for same-origin URLs, or the `blob:` and `data:` schemes.

---

# `<a>` Element `download` Attribute

## Example

```html
<a href="#" download>Download me</a>
<a href="#" download="slides.html">Download me as slides.html</a>
```

<iframe src="../examples/a-download-attribute.html" style="width:100%; height:500px; border:0; border-radius: 4px; overflow:hidden;"></iframe>

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# CSS :target selector

<blockquote>
 <i class="fa fa-quote-left text-secondary " aria-hidden="true"></i>
The :target CSS pseudo-class represents a unique element (the target element) with an id matching the URL's fragment.
</blockquote>

<code class="code-primary">Use-case</code> SPA

<code class="code-primary">Alternative</code> JS-based routing

---

# CSS :target selector

## <a href="https://codesandbox.io/s/css-target-selector-ow5vq" target="_blank">Example</a>

---

## Example for `:target` Selector

<a href="https://john-doe.neocities.org/#home" target="_blank">john-doe.neocities.org</a>

---

# HTML and controlled Word-breaks

Example for controlled Word-breaks `<wbr>`

Explain Use-case

![word-break-html](../images/wbr.png)

[Example ](../examples/wbr-word-break.html)

---

# Inline Text markup

<iframe src="../examples/inline-text-markup.html" style="width:100%; height: 50vh; border:0; border-radius: 4px; overflow:hidden;"></iframe>

---

# How to check for JavaScript availability without JavaScript?

Simple way to check for JS availability with `<noscript>` and cookies:

Requires cookies!

```html
<noscript>
  <meta http-equiv="Set-Cookie" content="hasjs=false; path=/" />
  <meta http-equiv="Refresh" content="0" />
</noscript>
```

[Article](https://www.codeproject.com/Tips/1217469/How-to-Detect-if-Client-has-JavaScript-Enabled-Dis)

---

# Display Form validation state via CSS

https://jsfiddle.net/thomasdarimont/yp3z4o7b/11/

<iframe width="100%" height="300" src="//jsfiddle.net/thomasdarimont/yp3z4o7b/3/embedded/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

---

# Fine-tuning `<input>` elements for File Uploads

File upload -> Restrict file types

`<input type="file" accept=".xls,.xlsx" />`

Allow upload of multiple files, or emails via `multiple` attribute.

- Allow to specify multiple files via `<input type=”file” multiple>`

- Allow to specify multiple comma separated email addresses via `<input type=”email” multiple>`

---

# Auto-complete in forms fine-tunen

[Article](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/autocomplete#values)

---

# Lazy loading of Images

Lazy loading for images "above the fold".

TODO add Example to show lazy loading

```html
<img src="foo.png" loading="lazy" />
```

[Article](https://web.dev/browser-level-image-lazy-loading/)

---

# Protect your users Privacy with `<a>` attributes

Explain the problem

- referrer
- opener
- nofollow

```html
<a href="https://www.example.com" rel="noopener noreferrer nofollow">Link</a>
```

[Article](https://pointjupiter.com/what-noopener-noreferrer-nofollow-explained/)

---

# Protect your users Privacy with default Referrer Policy

```html
<meta name="referrer" content="default" />
```

[Article](https://w3c.github.io/webappsec-referrer-policy/#referrer-policy)

---

# Change form Method via `<input>` Attribut `formmethod`

Change http method to submit form for input elements via formmethod attribute

[Artikel](https://html.spec.whatwg.org/multipage/form-control-infrastructure.html#attr-fs-formmethod)

---

# Simple autocompletion with `<datalist>`

Explain

Use-case

```html
<label for="ice-cream-choice">Choose a flavor:</label>
<input list="ice-cream-flavors" id="ice-cream-choice" name="ice-cream-choice" />

<datalist id="ice-cream-flavors">
  <option value="Chocolate"></option>
  <option value="Coconut"></option>
  <option value="Mint"></option>
  <option value="Strawberry"></option>
  <option value="Vanilla"></option>
</datalist>
```

<label for="ice-cream-choice">Choose a flavor:</label>
<input list="ice-cream-flavors" id="ice-cream-choice" name="ice-cream-choice" />

<datalist id="ice-cream-flavors">
  <option value="Chocolate"></option>
  <option value="Coconut"></option>
  <option value="Mint"></option>
  <option value="Strawberry"></option>
  <option value="Vanilla"></option>
</datalist>

https://developer.mozilla.org/en-US/docs/Web/HTML/Element/datalist

---

# Built-in expandables with `<details>` & `<summary>`

```html
<details>
  <summary>System Requirements</summary>
  <p>
    Requires a computer running an operating system. The computer must have some
    memory and ideally some kind of long-term storage. An input device as well
    as some form of output device is recommended.
  </p>
</details>
```

<details>
  <summary>System Requirements</summary>
  <p>Requires a computer running an operating system. The computer
  must have some memory and ideally some kind of long-term storage.
  An input device as well as some form of output device is
  recommended.</p>
</details>

https://developer.mozilla.org/en-US/docs/Web/HTML/Element/details

---

# Integrate animated SVGs in HTML

https://jsfiddle.net/thomasdarimont/wm3Lh0fu/4/

<iframe width="100%" height="300" src="//jsfiddle.net/zrhL1jqx/embedded/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>
