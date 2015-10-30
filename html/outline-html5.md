## Outlining HTML5

In `HTML5`, outlining of the **document** is quite easy and simple, all you have to do is just define contents section-wise. All content lying inside the `<body>` **element** is part of a `<section>`. **Sections** in `HTML5` can be nested. Beside the main `<section>`, defined by the `<body>` **element**, `<section>` limits are defined either explicitly or implicitly. Explicitly-defined sections are the content within `<body>`,  `<section>`,  `<article>`,  `<aside>`, and `<nav>` tags.

### Header/Footer

`HTML5` also introduces two new **elements** that can be used to mark up the *header* and the *footer* of a section:

- Header tag ( `<header>` )
  - It defines a *page header*, typically containing the *logo* and *name of the site* and possibly a *horizontal menu* — or *section header*.

> Despite its name, it is not necessarily positioned at the beginning of the page or section.

```html
	<header>LexCorp</header>
```

- Footer tag ( `<footer>` )
	- It defines *a page footer*, typically containing the *copyright and legal notices* and sometimes some *links* or *section footer*, containing perhaps the section's *publication date*, *license information*, etc.

> Despite its name, it is not necessarily positioned at the end of the page or section.


```html
	<footer>© 2015 WARNER BROS. ENT. ALL RIGHTS RESERVED. TM & © DC COMICS.</footer>
```

### Navigation tag ( `<nav>` )
- It represents a section of a page that links to other pages or to parts within the page: *a section with navigation links*.

> Not all links of a document must be in a `<nav>` element, which is intended only for major block of *navigation links*, typically the `<footer>` element often has a list of links that don't need to be in a `<nav>` element.
> A document may have several `<nav>` elements, for example, one for site navigation and one for intra-page navigation.
> User agents, such as screen readers targeting disabled users, can use this element to determine whether to omit the initial rendering of this content.


```html
	<nav>
	  <ul>
		<li><a href="#">Home</a></li>
		<li><a href="#">About</a></li>
		<li><a href="#">Contact</a></li>
	  </ul>
	</nav>
```

### Section tag ( `<section>` )

- It represents a generic *section* of a document, i.e. a thematic grouping of content, typically with a heading. 
- Each `<section>` should be identified, typically by including a heading `<h1>` - `<h6>` element as a child of the `<section>` element.

> If it makes sense to separately syndicate the content of a `<section>` element, use an `<article>` element instead.
> Do not use the `<section>` element as a generic container; this is what `<div>` is for, especially when the sectioning is only for styling purposes. 
> A rule of thumb is that a section should logically appear in the outline of a document.

#### HTML4

```html
	<div>
	  <h2>LexCorp</h2>
	  <img src="main-logo.png" alt="LexCorp" title="LexCorp" />
	</div>
```

#### HTML5

```html
	<section>
	  <h2>LexCorp</h2>
	  <img src="main-logo.png" alt="LexCorp" title="LexCorp" />
	</section>
```

### Media Tags

- `HTML5` introduces *built-in media support* via the `<audio>` and `<video>` elements, offering the ability to *easily embed media* into `HTML` documents.


- Video tag ( `<video>` )
 	- It is used to *embed video* content. It may contain *several video sources*, represented using the *src attribute* or the `<source>` element, the browser will choose the most suitable one.


```html
	<video width="480" controls poster="https://www.videodomain.org/images/videoPreview.gif" >
	 <!-- Video with Multiple Sources -->
	  <source src="https://www.videodomain.org/download/videoPreview.mp4" type="video/mp4">
	  <source src="https://www.videodomain.org/download/videoPreview.ogv" type="video/ogg">
	  <source src="https://www.videodomain.org/download/videoPreview.webm" type="video/webm">
	  Your browser doesn't support HTML5 <code>&lt;video&gt;<code> tag.
	  <!-- Video with subtitles -->
	  <track kind="subtitles" src="videoPreview.en.vtt" srclang="en" label="English">
	</video>
```

- Audio tag ( `<audio>` )
	- It is used to *embed sound* content in documents. It may contain *several audio sources*, represented using the *src attribute* or the `<source>` element; the browser will choose the most suitable one.

```html
	<audio  controls="controls" poster="https://www.videodomain.org/images/videoPreview.gif" >
	 <!-- Video with Multiple Sources -->
	  <source src="https://www.videodomain.org/download/videoPreview.mp4" type="video/mp4">
	  <source src="https://www.videodomain.org/download/videoPreview.ogv" type="video/ogg">
	  <source src="https://www.videodomain.org/download/videoPreview.webm" type="video/webm">
	  Your browser doesn't support HTML5 <code>&lt;audio&gt;<code> tag.
	  <!-- Video with subtitles -->
	    <track kind="captions" src="videoPreview.en.vtt" srclang="en" label="English">
	</audio>
```


### Graphic Tags
- One of the most exciting additions that `HTML5` offers to draw free-form graphics on a drawing surface known as the `<canvas>` and `<svg>`.

- Canvas tag ( `<canvas>` )
	- It is used to *draw graphics* using scripting (usually `JavaScript`).
	- It can be used to *draw graphs*, make photo composition or simple (and not so simple) animations.

```html
	 <canvas width="200" height="100"></canvas> 
```


- SVG aka Scalable Vector Graphics tag ( `<svg>` )
    - It can be used to nest a standalone `<svg>` fragment inside the current document (for example an HTML document) as long as the `<svg>` is not the root element. This standalone fragment has its own viewport and coordinate system.

```html
	<svg width="150" height="100" viewBox="0 0 3 2">
    	<rect width="1" height="2" x="0" fill="#008d46" />
    	<rect width="1" height="2" x="1" fill="#ffffff" />
    	<rect width="1" height="2" x="2" fill="#d2232c" />
  	</svg>
```

### A simple HTML5 document

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="utf-8" />
		<meta http-equiv="X-UA-Compatible" content="IE=edge" />
		<meta name="viewport" content="width=device-width, initial-scale=1" />
		<title>LexCorp</title>
	</head>
	<body>
		<!-- site wrapper -->
		<section class="page-wrapper"> 
		  <!-- header section -->
		  <header>
		    <h1>LexCorp</h1>
		    <!-- Site logo -->
		    <img src="http://i.imgur.com/goPWBCd.jpg" width="300" height="45" alt="LexCorp" title="LexCorp" />
		    <!-- navigation section -->
		    <nav>
		      <ul>
		        <li><a href="#" title="Home">Home</a></li>
		        <li><a href="#" title="About">About</a></li>
		        <li><a href="#" title="Contact">Contact</a></li>
		      </ul>
		    </nav>
		  </header>
		  <!-- content section -->
		  <section> LEXCORP IS BUILDING A BETTER TOMORROW, TODAY. <br />
		    <br />
		    LEXCORP PROVIDES EXPERTISE AND RESEARCH TO THE GLOBAL MARKETPLACE AND CROSS-INDUSTRY INNOVATIONS THAT TRANSFORM AND INSPIRE. <br />
		    <br />
		    WE BUILD PRODUCTS THAT HELP MILLIONS OF HOMES, BUSINESSES AND GOVERNMENTS WORK BETTER. <br />
		    <br />
		  </section>
		  <!-- footer section -->
		  <footer>© 2015 WARNER BROS. ENT. ALL RIGHTS RESERVED. TM & © DC COMICS.</footer>
		</section>
	</body>
</html>
```

![Simple HTML5 document](http://i.imgur.com/nFThGcb.jpg)

----
Go back to `HTML` [Table of Content](html.md)