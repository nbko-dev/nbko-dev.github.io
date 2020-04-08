---
layout: post
title: Semantic Markup
tags:
  - markup
  - semantic tag	
  - responsive web
---

# Semantic Elements

This document is written as summary from [this article](https://guide.freecodecamp.org/html/html5-semantic-elements/).

## **List of new semantic elements**

The semantic elements added in HTML5 are:

- `<article>`
- `<aside>`
- `<details>`
- `<figcaption>`
- `<figure>`
- `<footer>`
- `<header>`
- `<main>`
- `<mark>`
- `<nav>`
- `<section>`
- `<summary>`
- `<time>`

Elements such as `<header>`, `<nav>`, `<section>`, `<article>`, `<aside>`, and `<footer>` act more or less like `<div>` elements. They group other elements together into page sections. However where a `<div>` tag could contain any type of information, it is easy to identify what sort of information would go in a semantic `<header>` region.

## Benefits of semantic elements

```html
<header></header>
<section>
	<article>
		<figure>
			<img>
			<figcaption></figcaption>
		</figure>
	</article>
</section>
<footer></footer>

<div id="header"></div>
<div class="section">
	<div class="article">
		<div class="figure">
			<img>
			<div class="figcaption"></div>
		</div>
	</div>
</div>
<div id="footer"></div>
```

1. easier to read
2. greater accessibility
3. consistent code

## `<section>` and `<article>`

The `<section>` and `<article>` elements are conceptually similar and interchangeable. To decide which of these you should choose, take note of the following:

1. An article is intended to be independently distributable or reusable.
2. A section is a thematic grouping of content.

    <section>
      <p>Top Stories</p>
      <section>
        <p>News</p>
        <article>Story 1</article>
        <article>Story 2</article>
        <article>Story 3</article>
      </section>
      <section>
        <p>Sport</p>
        <article>Story 1</article>
        <article>Story 2</article>
        <article>Story 3</article>
      </section>
    </section>

## `<header>` and `<hgroup>`

The `<header>` element is generally found at the top of a document, a section, or an article and usually contains the main heading and some navigation and search tools.

```html
<header>
  <h1>Company A</h1>
  <ul>
    <li><a href="/home">Home</a></li>
    <li><a href="/about">About</a></li>
    <li><a href="/contact">Contact us</a></li>
  </ul>
  <form target="/search">
    <input name="q" type="search" />
    <input type="submit" />
  </form>
</header>
```

The `<hgroup>` element should be used where you want a main heading with one or more subheadings.

```html
<hgroup>
  <h1>Heading 1</h1>
  <h2>Subheading 1</h2>
  <h2>Subheading 2</h2>
</hgroup>
```

**!** The `<header>` element can contain any content, but the `<hgroup>` element can only contain other headers, that is `<h1>` to `<h6>` and including `<hgroup>`.

## `<aside>`

The `<aside>` element is intended for content that is not part of the flow of the text in which it appears, however still related in some way. This of `<aside>` as a sidebar to your main content.

```html
<aside>
  <p>This is a sidebar, for example a terminology definition or a short background to a historical figure.</p>
</aside>
```

`<nav>` in `<aside>` : As a local navigation. Global navi is located in `<header>`

```html
<nav>
  <ul>
    <li><a href="/home">Home</a></li>
    <li><a href="/about">About</a></li>
    <li><a href="/contact">Contact us</a></li>
  </ul>
</nav>
```

## `<figure>` and `<figcaption>`

`<figure>` is for wrapping your image content around it, and `<figcaption>` is to caption your image.

```html
<figure>
  <img src="https://en.wikipedia.org/wiki/File:Shadow_of_Mordor_cover_art.jpg" alt="Shadow of Mordor" />
  <figcaption>Cover art for Middle-earth: Shadow of Mordor</figcaption>
</figure>
```

## `<footer>`

Just like the `<header>` the content is generally metainformation, such as author details, legal information, and/or links to related information. It is also valid to include `<section>` elements within a footer.

```html
<footer>&copy;Company A</footer>
```