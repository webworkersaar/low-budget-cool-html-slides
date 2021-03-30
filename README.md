# Low Budget, Cool HTML

## Links

- [HTML Spec](https://html.spec.whatwg.org/multipage/)

## Demos

- [x] ping attribut bei <a href="..."> links (https://codesandbox.io/s/a-ping-attribute-spb95)
- [x] [download attribute bei links](examples/a-download-attribute.html) (https://codesandbox.io/s/a-download-file-15msu)
- [x] [CSS :target selector für SPA like verhalten ohne JS](examples/css-target-selector) (https://codesandbox.io/s/css-target-selector-ow5vq)
- [x] [wbr für Worttrennung](examples/wbr-word-break.html) (https://codesandbox.io/s/dialog-and-word-break-xd16k?file=/index.html)
- [x] [Abkürzungen und Definitionen](examples/abbr-element.html)
- [ ] [sub, sup, del, ins](examples/inline-text-markup.html)

## Sonstige Beispiele

- HTML Dialog Element (https://codesandbox.io/s/dialog-and-word-break-xd16k?file=/index.html)
- [ ] Klick auf Label Element zum schnellzugriff auf ein Input Field <label>Foo<input name="foo"></label> ... da braucht man kein for="..."
- [ ] <template> Element -> okay, das ist insbesondere mit JS Nützlich...
- [ ] contenteditable attribute
- [ ] Einfacher Weg auf der Serverseite herauszufinden ob der aktuelle User-Agent JS aktiviert hat (https://www.codeproject.com/Tips/1217469/How-to-Detect-if-Client-has-JavaScript-Enabled-Dis)
- [ ] loading="lazy" attribute for image https://web.dev/browser-level-image-lazy-loading/
- [ ] rel=noopener, noreferrer,nofollow https://pointjupiter.com/what-noopener-noreferrer-nofollow-explained/
- [ ] Default Referrer Policy <meta name="referrer" content="default">https://w3c.github.io/webappsec-referrer-policy/#referrer-policy
- [ ] Change http method to submit form for input elements via formmethod attribute https://html.spec.whatwg.org/multipage/form-control-infrastructure.html#attr-fs-formmethod
- [ ] [10 rare HTML tags](https://code.tutsplus.com/articles/10-rare-html-tags-you-really-should-know--net-3908)
- [ ] [Hidden features of HTML](https://stackoverflow.com/questions/954327/hidden-features-of-html)
- [ ] [5 HTML tricks](https://www.geeksforgeeks.org/top-5-html-tricks-that-you-should-know/)
- [ ] Built-in autocompletion with input and datalist: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/datalist
- [ ] Built-in expandable with details and summary: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/details
- [ ] SVG animations with CSS: https://css-tricks.com/animating-svg-css/

# RayVeal

Rayveal is an opinionated version of the awesome [reveal.js](https://github.com/hakimel/reveal.js/). The main difference an approach to creating slides that is [markdown centered](https://github.github.com/gfm/) with the ability to create multiple presentations in the same project.

This, plus the pre-installation of convenient plugins and libraries make it easier to create your presentations quickly using markdown. That helps me focus on writing and not on laying out presentations.

You can see the demo at [rayveal.tech](http://rayveal.tech).

## Instructions

Instead of creating HTML files, you simply create one or more `*.md` files in the `docs/slides` folder. A server is required in order to use RayVeal properly...since the markdown files have to be loaded dynamicaly, so upload the contents of the `build` folder to a server.

## Installing Locally with NPM (optional)

Optionally, you can just run the presentation locally (great when you can't guarantee a network connection), There's a live preview server provided.

1. Grab/Fork from [repo](http://github.com/planetoftheweb/rayveal)
1. `build` folder has presentation
1. `docs/slides/demo.md` subfolder has sample markdown
1. `slides/index.json` has a list of presentations (optional)

## Running locally

1. Run `$ npm install` from your terminal
1. Edit `docs/slides/demo.md` or add `*.md files`
1. Run `$ npm start` from your terminal
1. Generates the `docs/slides/index.json` file (index)
1. Creates a live reload server

## Pre-installed libraries

Pre-installed libraries like [Font Awesome](https://fontawesome.com/?from=io) will let you easily add icons to your presentation, while a lightweight version of bootstrap, which you can customize for your own needs, lets you use things like buttons, table, cards, list-groups and form styles if you need them. You can customize what's included with an `npm run bootstrap-light` command.

- [Font Awesome](https://fontawesome.com/?from=io)
- [Lightweight Bootstrap](https://getbootstrap.com)

If you want to control what gets included in the `bootstrap-light.css` file, you can edit the `src/bootstrap-light/scss/bootstrap.scss` file.

## Pre-installed plugins

There are lots of great [reveal.js plugins](https://github.com/hakimel/reveal.js/wiki/Plugins,-Tools-and-Hardware) and I added the awesome [menu plugin](https://github.com/denehyg/reveal.js-menu), so that you can hit the `m` key and get a list of your presentations.

## Persistent toolbar

One of the problems I often have when doing presentation is making sure that people have the URL to the presentation as well as contact and other important information. So, I created a persistent toolbar at the bottom of every slide.

It auto-hides after 5 seconds, but you can bring it back by using the `t` key. You can find it in the index.html file and put your own HTML there.

## Fragments by default

Another way in which RayVeal differs from reveal is in the way it handles fragments. I don't like to show a lot of text in my presentations, but write short bullet points that I want people to consume one at a time. Therefore, fragments are on by default, just write your normal bullet points and they will show one at a time.

## contenteditable code

Another way that Rayveal differs is that when you write code blocks by either using the <code>&grave;</code> character or <code>&grave;&grave;&grave;</code> codeblocks, Rayveal makes those automatically have the `contenteditable` attribute. I demo a lot of code, so it's nice to be able to edit my codeblocks or even anything with the code tag.

## Code options

I created some additional styles that are not in bootstrap.

### Colored code blocks

You can use `code` blocks with different colors

```html
<code class="code-primary">primary</code>
<code class="code-success">success</code>
<code class="code-info">info</code>
<code class="code-warning">warning</code>
<code class="code-danger">danger</code>
```

### Tooltips

I'm not importing the Bootstrap JavaScript or the Bootstrap Grid, so I created my own way of doing a simple tooltip using CSS.

```html
<a class="tooltip" href="#">`tooltips`<span>For overlay explanations</span></a>
on rollover
```

### Code Sample Lists

There's also a style that I need for some of my own coursework, which lets you create lists with code samples that change color in each line. Here's the code:

```md
- `sample`
  - NUM: `one` `two` `three`
  - NUM: `four` `five` `six`
  - NUM: `seven` `eight` `nine`
  - NUM: `ten` `eleven` `twelve`
  - NUM:<br>
    `thirteen` `fourteen` `fifteen`
```

But it's better if you look at these in the [demo](https://rayveal.tech)

## Slide Templates

Reveal.js lets you add style tags, classes and data attributes in comments, so I used these to create different slide templates. There are three right now.

### Title Slide

`<!-- .slide: data-state="title" -->`

This is the title slide that appears at the beginning of the [demo](https://rayveal.tech). Blue background, large fonts.

### Page with Icons

`<!-- .slide: data-state="hasicon" -->`

A page that has a title with a Font Awesome icon in it. The spacing has to be different.

### Circles

`<!-- .slide: data-state="circles" -->`

In this page, each bullet point becomes a circle. Just a different way to help the user focus.

## More

Take a look at the [demo](https://rayveal.tech) for more examples, I'm really excited about some of the stuff you can do with Bootstrap's card and list-group components. I'd love to add more components and other layouts in the future.
