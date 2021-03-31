<!-- .slide: data-state="layout-title" class="bg-dark" data-transition="zoom" -->

# ![Title](../images/title-logo.jpg)

## HTML <del>sucks</del> <ins>rocks</ins>!

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# `<a>` Element `ping` Attribute

<blockquote>
 <i class="fa fa-quote-left text-secondary " aria-hidden="true"></i>
A space-separated list of URLs. When the link is followed, the browser will send POST requests with the body PING to the URLs. Typically for tracking.
</blockquote>

<code class="code-primary">Use-cases</code> Tracking user behaviour

<code>JS Alternative</code> [Beacon API](https://developer.mozilla.org/en-US/docs/Web/API/Beacon_API)

---

<!-- .slide: class="bg-dark" -->

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

<!-- .slide: class="bg-dark" -->

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

<code class="code-primary">Use-case</code> If you don't want to open the file inplace with an embedded viewer.

<code class="code-primary">Alternative</code> Server side content-disposition...?

<code class="code-info">Note:</code> This only works for same-origin URLs, or the `blob:` and `data:` schemes.

---

<!-- .slide: class="bg-dark" -->

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

<!-- .slide: class="bg-dark" -->

# CSS :target selector

## <a href="https://codesandbox.io/s/css-target-selector-ow5vq" target="_blank">Example</a>

---

<!-- .slide: class="bg-dark" -->

## Example for `:target` Selector

<a href="https://john-doe.neocities.org/#home" target="_blank">john-doe.neocities.org</a>

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# HTML & CSS for wrapping long words

<code class="code-primary">Use-case</code> Readability

<code class="code-primary">Alternatives</code> <a href="https://www.cjcid.com/articles/wrapping-long-words-css-html/" target="_blank">A lot!</a>

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# HTML and controlled Word-breaks

## <a href="../examples/wbr-word-break.html" target="_blank">Example</a>

![word-break-html](../images/wbr.png)

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# CSS and controlled Word-breaks

## <a href="https://www.cjcid.com/articles/wrapping-long-words-css-html/#white-space" target="_blank">Example</a>

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Inline Text Markup

```html
<h1>Inline Text Markup</h1>
<h2><pre>kbd</pre></h2>
<p>
  Please press <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>Entf</kbd> to close the
  app.
</p>
<h2>sub and sup</h2>
<p>H<sub>2</sub>O</p>
<p>Satz des Pythagoras: a<sup>2</sup> + b<sup>2</sup> = c<sup>2</sup></p>
<h2><del>del</del>, <ins>ins</ins></h2>
<p>HTML <del>sucks</del> <ins>rocks</ins>!</p>
```

<iframe src="../examples/inline-text-markup.html" style="width:100%; height: 50vh; border:0; border-radius: 4px; overflow:hidden;"></iframe>

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Display Form Validation State via CSS

```html
<form>
  <label for="email">Email</label>
  <input type="email" 
    id="email" 
    name="email" 
    placeholder="Enter your email"
    >
  <span></span>
</form>
```

```css
input[type='email'] {
  width: 200px;
}

input[type='email']:invalid {
  border: 1px solid red;
}

input[type='email']:invalid + span::after {
    color:red;
    content: " x";
}

input[type='email']:valid + span::after {
    color:green;
    content: " ✔";
}
```

<code>
<style>
  input[type='email'] {
  width: 400px;
}

input[type='email']:invalid {
  border: 1px solid red;
}

input[type='email']:invalid + span::after {
    color:red;
    content: " x";
}

input[type='email']:valid + span::after {
    color:green;
    content: " ✔";
}
</style>
<form>
  <label for="email">Email</label>
  <input type="email" 
    id="email" 
    name="email" 
    placeholder="Enter your email"
    >
  <span></span>
</form>
</code>

<a href="https://jsfiddle.net/thomasdarimont/yp3z4o7b/11/" target="_blank">Form Validation State Example</a>

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Fine-tuning `<input>` elements for File Uploads

File upload -> Restrict file types

`<input type="file" accept=".xls,.xlsx" />`

Allow upload of multiple files, or emails via `multiple` attribute.

- Allow to specify multiple files via `<input type=”file” multiple>`

- Allow to specify multiple comma separated email addresses via `<input type=”email” multiple>`

<style>
  input[type='email'] {
  width: 400px;
}

input[type='email']:invalid {
  border: 1px solid red;
}

input[type='email']:invalid + span::after {
    color:red;
    content: " x";
}

input[type='email']:valid + span::after {
    color:green;
    content: " ✔";
}
</style>
<form>
  <label for="email">Email</label>
  <input type="email" 
    id="email" 
    name="email" 
    placeholder="Enter your email"
    multiple
    >
  <span></span>
</form>
---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Auto-completion in Forms

The HTML autocomplete attribute is available on <input> elements that take a text or numeric value as input, <textarea> elements, <select> elements, and <form> elements. autocomplete lets web developers specify what if any permission the user agent has to provide automated assistance in filling out form field values, as well as guidance to the browser as to the type of information expected in the field.

For example:
- "off"
- "on"
- "name"
- "email"
- "username"
- "new-password"
- "current-password"
- "one-time-code"
- ... any many many more

[Article](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/autocomplete#values)

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Lazy-Loading for Images

<blockquote>
 <i class="fa fa-quote-left text-secondary " aria-hidden="true"></i>
Lazy loading is a strategy to identify resources as non-blocking (non-critical) and load these only when needed. It's a way to shorten the length of the critical rendering path, which translates into reduced page load times.
</blockquote>

Indicates how the browser should load the image:

- eager: Loads the image immediately, regardless of whether or not the image is currently within the visible viewport (default).
- lazy: Defers loading the image until it reaches a calculated distance from the viewport, as defined by the browser.

```html
<img src="foo.png" loading="lazy" />
```

[Article](https://web.dev/browser-level-image-lazy-loading/)

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

## Example Lazy-Loading

<a href="https://sczvj.sse.codesandbox.io/lazy" target="_blank">Lazy Image loading example</a>

<a href="https://codesandbox.io/s/admiring-wind-sczvj?file=/src/lazy.html" target="_blank">Code</a>

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Additional values for `rel` attribute of the `<a>` element.

Explain the problem

https://developer.mozilla.org/en-US/docs/Web/HTML/Link_types

- referrer
- opener
- follow

nofollow Indicates that the linked document is not endorsed by the author of this one, for example if it has no control over it, if it is a bad example or if there is commercial relationship between the two (sold link). This link type may be used by some search engines that use popularity ranking techniques.

noreferrer
Prevents the browser, when navigating to another page, to send this page address, or any other value, as referrer via the Referer: HTTP header.
(In Firefox, before Firefox 37, this worked only in links found in pages. Links clicked in the UI, like "Open in a new tab" via the contextual menu, ignored this).

nofollow Indicates that the linked document is not endorsed by the author of this one, for example if it has no control over it, if it is a bad example or if there is commercial relationship between the two (sold link). This link type may be used by some search engines that use popularity ranking techniques.

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Protect your users Privacy with default Referrer Policy

There are three fundamental values of the rel attribute of the anchor tag. They are noreferrer, noopener, and nofollow.

- rel="noopener" you use on all links opening in new tabs using the target _blank. There are security implications if you don’t use the noopener value on your links opening in new tabs. A malicious attacker can use the window.opener object to change the content and location of the originating page.
- rel="noreferrer" can serve a similar purpose as the noopener, especially in the older browsers. Hence, it makes sense to use them both. Additionally, noreferrer can affect your analytics and report traffic as direct instead of referral.
- rel="nofollow" will inform search engines not to pass the link juice to the linked page, and it will not pass PageRank. You can consider it as a value which is used when you want to link to some another page but without “endorsing” it. It is the only rel value on this list with a tangible effect on SEO efforts.


```html
<a href="https://www.example.com" rel="noopener noreferrer nofollow">Link</a>
```

[Article](https://pointjupiter.com/what-noopener-noreferrer-nofollow-explained/)

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Change form Method via `<input>` Attribut `formmethod`

Change http method to submit form for input elements via formmethod attribute

[Artikel](https://html.spec.whatwg.org/multipage/form-control-infrastructure.html#attr-fs-formmethod)

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Simple autocompletion with `<datalist>`

The HTML <datalist> element contains a set of <option> elements that represent the permissible or recommended options available to choose from within other controls.

<a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/datalist">Datalist at MDN</a>

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

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Built-in expandables with `<details>` & `<summary>`

The HTML Details Element (`<details>`) creates a disclosure widget in which information is visible only when the widget is toggled into an "open" state. A summary or label must be provided using the `<summary>` element.

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

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Integrate animated SVGs in HTML

https://developer.mozilla.org/en-US/docs/Web/SVG/Element

<a href="https://jsfiddle.net/thomasdarimont/wm3Lh0fu/4/" target="_blank">Animated SVG Example</a>

```html
<div>
  <h1>SVG in HTML!</h1>
  <svg viewBox="0 0 64 64" width="64" height="64">
    <circle id="spinner" cx="32" cy="32" r="16"></circle>
  </svg>
</div>
```

```css
/* What we want to animate */
#spinner {
  fill: yellow;

  /* Refer to the animation  */
  animation-name: spinner-ani;

  /* How should the animation be executed? */
  animation-duration: 1s;
  animation-iteration-count: infinite;
}

/* What should happen during the animation? */
@keyframes spinner-ani {
  from {
    fill: red;
    r: 5;
  }
  to {
    fill: yellow;
    r: 32;
  }
}
```
