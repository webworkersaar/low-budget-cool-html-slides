<!-- .slide: data-state="layout-title" class="bg-dark" data-transition="zoom" -->

# ![Title](../images/title-logo.jpg)

## HTML <del>sucks</del> <ins>rocks</ins>!

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Edit Content on any Page

<blockquote>
 <i class="fa fa-quote-left text-secondary " aria-hidden="true"></i>
The <code>contenteditable</code> attribute allows to enable live editing of text content for HTML elements.
</blockquote>

<code class="code-primary">Use-cases</code> Adjust content for screenshots.

```html

&lt;body contenteditable>
...
&lt;/body>

```

<ul>
<li><a href="https://www.zeit.de/index" target="_blank">Let's make some good news</a></li>
<li><a href="https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Editable_content" target="_blank">Learn more about contenteditable on MDN</a></li>
<ul>

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
  href="#/3/0/2"
  ping="https://20210301webworkersaar.requestcatcher.com/callbacks/myping"
>
  `ping` Example with local links
</a>
```

<a href="#/3/0/2" ping="https://20210301webworkersaar.requestcatcher.com/callbacks/myping" >`ping Example with local links`</a>

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
The <code>:target</code> CSS pseudo-class represents a unique element (the target element) with an id matching the URL's fragment.
</blockquote>

<code class="code-primary">Use-case</code> SPA like View navigation.

<code class="code-primary">Alternative</code> JS-based routing

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# CSS :target selector
<ul>
<li><a href="https://codesandbox.io/s/css-target-selector-ow5vq" target="_blank"><code>:target Selector Example 1</code></a></li>
<li><a href="https://john-doe.neocities.org/#home" target="_blank"><code>:target Selector Example 2</code></a></li>
</ul>

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Dealing with long words in Markup

<blockquote>
 <i class="fa fa-quote-left text-secondary " aria-hidden="true"></i>
Controlling the word-breaks in long words.
</blockquote>

<ul>
<li>Using the <code>&lt;wbr></code> element</li>
<li>Using the “soft hyphen” <code>&amp;shy;</code> unicode character</li>
<li>Using CSS propertoes like <code>work-break</code>,<code>white-space</code> or <code>overflow-wrap</code> etc.</li>
</ul>

<code class="code-primary">Use-case</code> Improve readability

<code class="code-primary">Alternatives</code> <a href="https://www.cjcid.com/articles/wrapping-long-words-css-html/" target="_blank">Plenty of</a>

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Control Word-breaks with HTML

## <a href="../examples/wbr-word-break.html" target="_blank">Example</a>

![word-break-html](../images/wbr.png)

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Control Word-breaks with CSS

## <a href="https://www.cjcid.com/articles/wrapping-long-words-css-html/#white-space" target="_blank">Example</a>

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Inline Text Markup

<blockquote>
 <i class="fa fa-quote-left text-secondary " aria-hidden="true"></i>
Allows to specify additional text-level semantics.
</blockquote>

```html
<h1>Inline Text Markup</h1>
<h2><pre>kbd</pre></h2>
<p>
  Please press <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>Entf</kbd> to close the
  app.
</p>

<h2>sub, sup and var</h2>
<p>H<sub>2</sub>O</p>

<p>Satz des Pythagoras: 
<var>a</var><sup>2</sup> + <var>b</var><sup>2</sup> = <var>c</var><sup>2</sup>
</p>

<h2><del>del</del>, <ins>ins</ins></h2>
<p>HTML <del>sucks</del> <ins>rocks</ins>!</p>

<p>Marking text:
  This you can <mark>mark text</mark> to highlight a reference.
  </p>

```

<iframe src="../examples/inline-text-markup.html" style="width:100%; height: 50vh; border:0; border-radius: 4px; overflow:hidden;"></iframe>

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Display Form Validation State via CSS

<blockquote>
 <i class="fa fa-quote-left text-secondary " aria-hidden="true"></i>
Allows quick feedback to users. Validations can also be customized with JavaScript.
</blockquote>

```html
<form>
  <label for="email">Email</label>
  <input type="email" 
    id="email" 
    name="myemail" 
    autocomplete="off"
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
    name="myemail" 
    autocomplete="off" 
    placeholder="Enter your email"
    >
  <span></span>
</form>
</code>

<a href="https://jsfiddle.net/thomasdarimont/yp3z4o7b/11/" target="_blank">Form validation example</a>

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Fine-tuning `<input>` elements for File Uploads

<blockquote>
 <i class="fa fa-quote-left text-secondary " aria-hidden="true"></i>
Allows to control uploadable files, by restricting allowed file types and allowing selection multiple file.
</blockquote>

`<input type="file" accept=".xls,.xlsx" />`

You can allow upload of multiple files via `multiple` attribute.

```html
<input type=”file” multiple>
```

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Control auto-completion in Forms

<blockquote>
 <i class="fa fa-quote-left text-secondary " aria-hidden="true"></i>
The HTML <code>autocomplete</code> attribute is available on <code>&lt;input></code> elements that take a text or numeric value as input, <code>&lt;textarea></code> elements, <code>&lt;select></code> elements, and <code>&lt;form></code> elements. <code>autocomplete</code> lets web developers specify what automated assistance in filling out form field values is provided.
</blockquote>

Some examples for the <code>autocomplete</code> attribute
<ul>
<li><code>off</code></li>
<li><code>on</code></li>
<li><code>name</code></li>
<li><code>email</code></li>
<li><code>username</code></li>
<li><code>new-password</code></li>
<li><code>current-password</code></li>
<li><code>one-time-code</code></li>
<li>... and many many more <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/autocomplete#values">as shown in this article</a></li>
</ul>

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Adjust Form behaviour via `<input>`

<blockquote>
 <i class="fa fa-quote-left text-secondary " aria-hidden="true"></i>
Sometimes it is useful to change the form behaviour for specifc input fields.
</blockquote>

<code class="code-primary">Use-case</code> handle different form submission via single form.

<ul>
<li><code>formaction</code> URL to use for form submission.</li>
<li><code>formmethod</code> HTTP method to use for form submission.</li>
<li><code>formnovalidate</code> Bypass form control validation for form submission.</li>
<li><code>formtarget</code> The browsing context into which to load the response returned by the server after submitting the form.</li>
</ul>

[See more about input elements here](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Simple auto-completion with `<datalist>`

<blockquote>
 <i class="fa fa-quote-left text-secondary " aria-hidden="true"></i>
The HTML <code>&lt;datalist></code> element contains a set of <code>&lt;option></code> elements that represent the options available to choose from within other controls.
</blockquote>

<code class="code-primary">Use-case</code> provide a lean auto-completion without JavaScript.

```html
<label for="ice-cream-choice">Choose a flavor:</label>
<input list="ice-cream-flavors" id="ice-cream-choice" name="ice-cream-choice" />

<datalist id="ice-cream-flavors">
  <option value="Chocolate"></option>
  <option value="Chai-Latte"></option>
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
  <option value="Chai-Latte"></option>
  <option value="Coconut"></option>
  <option value="Mint"></option>
  <option value="Strawberry"></option>
  <option value="Vanilla"></option>
</datalist>

<a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/datalist">See more about datalist on MDN</a>

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Custom details sections

<blockquote>
 <i class="fa fa-quote-left text-secondary " aria-hidden="true"></i>
The HTML Details Element <code>&lt;details></code> creates a disclosure widget in which information is visible only when the widget is toggled into an <code>"open"</code> state. A summary or label must be provided using the <code>&lt;summary></code> element.
</blockquote>

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

<a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/details">See more about details on MDN</a>



---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Lazy-Loading of Images

<blockquote>
 <i class="fa fa-quote-left text-secondary " aria-hidden="true"></i>
Lazy loading is a strategy to identify resources as non-blocking (non-critical) and load these only when needed. It's a way to shorten the length of the critical rendering path, which translates into reduced page load times.
</blockquote>

The <code>loading</code> attribute of an <code>&lt;img></code> element indicates how the browser should load the image.

<ul>
<li><code>eager</code> Loads the image immediately, regardless of whether or not the image is currently within the visible viewport (default).</li> 
<li><code>lazy</code> Defers loading the image until it reaches a calculated distance from the viewport, as defined by the browser.</li>
</ul>

```html
<img src="foo.png" loading="lazy" />
```

[This article explains the loading attribute in depth](https://web.dev/browser-level-image-lazy-loading/)

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

## Lazy-Loading of Images in Action

<blockquote>
 <i class="fa fa-quote-left text-secondary " aria-hidden="true"></i>
You can speed up the loading of a page quite a but by using lazy loading.</blockquote>

<a href="https://sczvj.sse.codesandbox.io/lazy" target="_blank">Lazy Image loading example</a>

<a href="https://codesandbox.io/s/admiring-wind-sczvj?file=/src/lazy.html" target="_blank">Code</a>

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Adjust data sent when clicking an `<a>`

<blockquote>
 <i class="fa fa-quote-left text-secondary " aria-hidden="true"></i>
Sometimes you want to adjust what information is sent when you click on a link. For this you can use the <code>rel</code> attribute of a <code>&lt;a></code> element.
</blockquote>

<ul>
<li><code>noreferrer</code> Prevents the browser, when navigating to another page, to send this page address, or any other value, as referrer via the Referer: HTTP header.</li>
<li><code>noopener</code> Instructs the browser to open the link without granting the new browsing context access to the document that opened it. This means Window.opener will be null.</li>
<li><code>nofollow</code> Indicates that the linked document is not endorsed by the author of this one, for example if it has no control over it, if it is a bad example or if there is commercial relationship between the two (sold link).</li>
</ul>

```html
<a href="https://www.example.com" rel="noopener noreferrer nofollow">Link</a>
```

<ul>
<li><a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Link_types">More about different link types on MDN</a></li>
<li><a href="https://pointjupiter.com/what-noopener-noreferrer-nofollow-explained/">More about policies like noopener noreferrer nofollow</a></li>
</ul>

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# Embed SVGs in HTML

<blockquote>
 <i class="fa fa-quote-left text-secondary " aria-hidden="true"></i>
Sometimes it is useful to integrate <code>&lt;svg></code> elements directly into the DOM of your page instead of loading them as an image.
</blockquote>

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

<a href="https://jsfiddle.net/thomasdarimont/wm3Lh0fu/4/" target="_blank">Animated SVG Example</a>

<a href="https://developer.mozilla.org/en-US/docs/Web/SVG/Element">More about the svg element on MDN</a>

---

<!-- .slide: data-state="layout-title" class="bg-dark" -->

# What's your favorite Low-Budget but cool HTML trick?

???
