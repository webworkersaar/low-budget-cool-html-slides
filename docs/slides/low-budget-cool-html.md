<!-- .slide: data-state="layout-title"  -->

# Low budget, cool HTML

## HTML <del>sucks</del> <ins>rocks</ins>!

---

<!-- .slide: data-state="layout-title" data-transition="zoom" class="bg-dark"-->

# `<a>` Attribute

---

<!-- .slide: data-transition="none" -->

# <a href="https://codesandbox.io/s/a-ping-attribute-spb95" target="_blank">`ping`</a>

<iframe src="https://codesandbox.io/embed/a-ping-attribute-spb95?fontsize=14&hidenavigation=1&theme=dark"
     style="width:100%; height:500px; border:0; border-radius: 4px; overflow:hidden;"
     title="a-ping-attribute"
     allow="accelerometer; ambient-light-sensor; camera; encrypted-media; geolocation; gyroscope; hid; microphone; midi; payment; usb; vr; xr-spatial-tracking"
     sandbox="allow-forms allow-modals allow-popups allow-presentation allow-same-origin allow-scripts"
   ></iframe>

---

# `download` Attribut

```html
<a href="#" download>Download me</a>
```

<iframe src="../examples/a-download-attribute.html" style="width:100%; height:500px; border:0; border-radius: 4px; overflow:hidden;"></iframe>

---

# CSS :target selector (für SPA Verhalten)

<iframe src="../examples/css-target-selector.html" style="width:100%; height:500px; border:0; border-radius: 4px; overflow:hidden;"></iframe>

---

# HTML und Zeilenumbrüche

![word-break-html](../images/wbr.png)

---

# HTML und Zeilenumbrüche

<iframe src="../examples/wbr-word-break.html" style="width:100%; height: 50vh; border:0; border-radius: 4px; overflow:hidden;"></iframe>

---

# Inline Text markup

<iframe src="../examples/inline-text-markup.html" style="width:100%; height: 50vh; border:0; border-radius: 4px; overflow:hidden;"></iframe>

---

Einfacher Weg auf der Serverseite herauszufinden ob der aktuelle User-Agent JS aktiviert hat.

```html
<noscript>
  <meta http-equiv="Set-Cookie" content="hasjs=false; path=/" />
  <meta http-equiv="Refresh" content="0" />
</noscript>
```

[Artikel](https://www.codeproject.com/Tips/1217469/How-to-Detect-if-Client-has-JavaScript-Enabled-Dis)

---

Upload von files -> Datei typen beschränken

`<input type=”file”>` -> Mehrere dateien hochladen mit multiple attribute

`<input type="file" accept=".xls,.xlsx" />`

---

# Form validierungsstatus über CSS anzeigen

<iframe width="100%" height="300" src="//jsfiddle.net/thomasdarimont/yp3z4o7b/3/embedded/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

---

# Auto-complete in forms fine-tunen

[Artikel](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/autocomplete#values)

---

# Lazy loading

```html
<img src="foo.png" loading="lazy" />
```

[Artikel](https://web.dev/browser-level-image-lazy-loading/)

---

# rel=noopener,<br/> noreferrer,<br/>nofollow

[Artikel](https://pointjupiter.com/what-noopener-noreferrer-nofollow-explained/)

---

# Default Referrer Policy

```html
<meta name="referrer" content="default" />
```

[Artikel](https://w3c.github.io/webappsec-referrer-policy/#referrer-policy)

---

# input `formmethod` Attribut

Change http method to submit form for input elements via formmethod attribute

[Artikel](https://html.spec.whatwg.org/multipage/form-control-infrastructure.html#attr-fs-formmethod)

---

# Autocompletion mit `<datalist>`

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

# `<details>` & `<summary>` - Built-in expandables

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

# Animierte SVGs

<iframe width="100%" height="300" src="//jsfiddle.net/zrhL1jqx/embedded/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>
