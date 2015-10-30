css## Pseudo Classes and Elements

What *Pseudo* actuallly means is: **not real or genuine**, i.e. being apparently rather than actually as stated. And in `CSS` we can also use or target elements *apparently* if we can't or don't want to target them directly.


### Pseudo Class

- A `CSS` `pseudo-class` is a keyword added to **selectors** that specifies a special state of the element to be selected. 

> For example `:hover` will apply a style when the user hovers over the element specified by the selector.

- **Pseudo-classes**, together with `pseudo-elements`, let you apply a style to an element not only in relation to the content of the document tree, but also in relation to external factors like the history of the navigator (`:visited`, for example), the status of its content (like `:checked` on some form elements), or the position of the mouse (like `:hover` which lets you know if the mouse is over an element or not).

Some popular `pseudo-classes` are:

#### `:active`, `:hover`, `:link` and `:visited` 


- The `:active` `CSS` pseudo-class matches when an element is being activated by the user. 
- It allows the page to give a feedback that the activation has been detected by the browser. When interacting with a mouse, this is typically the time between the user presses the mouse button and releases it. 
- The `:active` pseudo-class is also typically matched when using the keyboard tab key. It is frequently used on `<a>` and `<button>` `HTML` elements, but may not be limited to just those.
- This style may be overridden by any other link-related pseudo-classes, that is `:link`, `:hover`, and `:visited`, appearing in subsequent rules. In order to style the appropriate links, you need to put the `:active` rule after all the other link-related rules, as defined by the LVHA-order: `:link` — `:visited` — `:hover` — `:active`.

- The `:hover` `CSS` pseudo-class matches when the user designates an element with a pointing device, but does not necessarily activate it. This style may be overridden by any other link-related pseudo-classes, that is `:link`, `:visited`, and `:active`, appearing in subsequent rules. In order to style appropriately links, you need to put the :hover rule after the :link and `:visited` rules but before the `:active` one, as defined by the LVHA-order: `:link` — `:visited` — `:hover` — `:active`.

- The `:link` `CSS` pseudo-class lets you select links inside elements. This will select any link which has not yet been visited, even those already styled using selector with other link-related pseudo-classes like `:hover`, `:active` or `:visited`. In order to appropriately style links, you need to put the `:link` rule before the other ones, as defined by the LVHA-order: `:link` — `:visited` — `:hover` — `:active`. The `:focus` pseudo-class is usually placed right before or right after :hover, depending on the expected effect.

- The `:visited` `CSS` pseudo-class lets you select only links that have been visited. This style may be overridden by any other link-related pseudo-classes, that is `:link`, `:hover`, and `:active`, appearing in subsequent rules. In order to style appropriately links, you need to put the `:visited` rule after the `:link` rule but before the other ones, defined in the LVHA-order: `:link` — :`visited` — `:hover` — `:active`.


For Example:

```css
	a:link { color: blue } /* unvisited links */
	a:visited { color: purple } /* visited links */
	a:hover { font-weight: bold } /* user hovers */
	a:active { color: lime } /* active links */
```

#### `:checked`, `:disabled`, `:focus`

- The `:checked` `CSS` pseudo-class selector represents any radio `<input type="radio">`, checkbox `<input type="checkbox">` or option `<option> in a <select>` element that is checked or toggled to an on state. The user can change this state by clicking on the element, or selecting a different value, in which case the :checked pseudo-class no longer applies to this element, but will to the relevant one.

- The `:disabled` `CSS` pseudo-class represents any disabled element. An element is disabled if it can't be activated (e.g. selected, clicked on or accept text input) or accept focus. The element also has an enabled state, in which it can be activated or accept focus.

- The `:focus` `CSS` pseudo-class is applied when a element has received focus, either from the user selecting it with the use of a keyboard or by activating with the mouse (e.g. a form input).


For Example:

```css
	input:checked {
	  margin-left: 25px;
	  border: 1px solid blue;
	}

	input:disabled { 
		background: #ccc; 
	}

	input:focus { 
		color: red; 
	}

```


#### `:first`, `:first-child` and `:first-of-type`

- The `:first` page `CSS` pseudo-class describes the styling of the first page when printing a document.

- The `:first-child` `CSS` pseudo-class represents any element that is the first child element of its parent.

- The `:first-of-type` `CSS` pseudo-class represents the first sibling of its type in the list of children of its parent element.

For Example:

```css
	@page :first {
 	    margin: 2in 3in;
	}

	span:first-child {
    	background-color: lime;
	}

	div :first-of-type {
  		background-color: lime;
	}
```


#### `:last-child` and `:last-of-type`

- The `:last-child` `CSS` pseudo-class represents any element that is the last child element of its parent.

The `:last-of-type` `CSS` pseudo-class represents the last sibling with the given element name in the list of children of its parent element.

For Example:

```css
	ul li:last-child {
		background-color: lime;
	}

	ul li:last-of-type {
  		color: lime;
	}

```



#### `:not`

- The negation `CSS` pseudo-class, `:not(X)`, is a functional notation taking a simple selector X as an argument. 

- It matches an element that is not represented by the argument. X must not contain another negation selector.

- The specificity of the `:not` pseudo-class is the specificity of its argument. The `:not` pseudo-class does not add to the selector specificity, unlike other pseudo-classes.

For Example:

```css
	:not(selector) { 
		style properties 
	}

	p:not(.classy) { 
		color: red; 
	}

	body :not(p) { 
		color: green; 
	}
	
```


#### `:nth-child`, `:nth-last-child`, `:nth-last-of-type` and `:nth-of-type`

- The `:nth-child(an+b)` `CSS` pseudo-class matches an element that has an+b-1 siblings before it in the document tree, for a given positive or zero value for n, and has a parent element. More simply stated, the selector matches a number of child elements whose numeric position in the series of children matches the pattern an+b.

- The `:nth-last-child` `CSS` pseudo-class matches an element that has an+b-1 siblings after it in the document tree, for a given positive or zero value for n, and has a parent element.

- In effect, it functions the same as :nth-child except it selects items counting backwards from the end of element series, not the start.

- The `:nth-last-of-type` `CSS` pseudo-class matches an element that has an+b-1 siblings with the same element name after it in the document tree, for a given positive or zero value for n, and has a parent element. See :nth-child for a more thorough description of the syntax of its argument.

- The `:nth-of-type` `CSS` pseudo-class matches an element that has an+b-1 siblings with the same element name before it in the document tree, for a given positive or zero value for n, and has a parent element. See :nth-child for a more thorough description of the syntax of its argument. This is a more flexible and useful pseudo selector if you want to ensure you're selecting the same type of tag no matter where it is inside the parent element, or what other different tags appear before it.

For Example:

```css
	
	element:nth-child(an + b) { 
		style properties 
	}


	tr:nth-child(2n+1)
	    Represents the odd rows of an HTML table.

	tr:nth-child(odd)
	    Represents the odd rows of an HTML table.

	tr:nth-child(2n)
	    Represents the even rows of an HTML table.

	tr:nth-child(even)
	    Represents the even rows of an HTML table.

	span:nth-child(0n+1)
	    Represents a span element which is the first child of its parent; this is the same as the :first-child selector.

	span:nth-child(1)
	    Equivalent to the above.

	span:nth-child(-n+3)
	    Matches if the element is one of the first three children of its parent and also a span. 

	element:nth-last-child(an + b) { style properties }

    tr:nth-last-child(-n+3) { /* the last 3 siblings */
		background-color: lime;
	}

	element:nth-last-of-type(an + b) { style properties }

	span:nth-last-of-type(2) {
  		background-color: lime;
	}

	element:nth-of-type(an + b) { style properties }

	p:nth-of-type(2n+1) { 
		text-align: left; 
	}
	
	p:nth-of-type(2n) { 
		text-align: right; 
	}


```


### Pseudo Elements

- Just like pseudo-classes, pseudo-elements are added to selectors but instead of describing a special state, they allow you to style certain parts of a document. For example, the `::first-line` pseudo-element targets only  the first line of an element specified by the selector.


Some popular `pseudo-elements` are:

#### `::after` ( `:after` )

- The `CSS` `::after` pseudo-element matches a virtual last child of the selected element. It is typically used to add cosmetic content to an element by using the content CSS property. This element is inline by default.


For Example:

```css
	/* CSS2 syntax */
	element:after  { 
		style properties 
	}

	/* CSS3 syntax */
	element::after { 
		style properties 
	}


	.exciting-text::after {
  		content: "<- now this *is* exciting!"; 
  		color: green;
	}

	.boring-text::after {
   		content:    "<- BORING!";
   		color:      red;
	}

```

#### `::before` ( `:before` )

- `::before` creates a pseudo-element that is the first child of the element matched. It is often used to add cosmetic content to an element by using the content property. This element is inline by default.

For Example:

```css
	/* CSS3 syntax */
	element::before { 
		style properties 
	}

	/* CSS2 obsolete syntax (only needed to support IE8) */
	element:before  { 
		style properties 
	}

	/* inserts content before every p element */
	p::before { 
		content: "Hello world!"; 
	}

	q::before { 
	  content: "«";
	  color: blue;
	}
	q::after { 
	  content: "»";
	  color: red;
	}


```

#### `::first-letter` ( `:first-letter` )

- The `::first-letter` `CSS` pseudo-element selects the first letter of the first line of a block, if it is not preceded by any other content (such as images or inline tables) on its line.

For Example:

```css
	p::first-letter { /* Use :first-letter if support for IE 8 or earlier is needed */
	  color: red;
	  font-size: 130%;
	}
```


#### `::first-line` ( `:first-line` )

- The `::first-line` `CSS` pseudo-element applies styles only to the first line of an element. The amount of the text on the first line depends of numerous factors, like the width of the elements or of the document, but also of the font size of the text. As all pseudo-elements, the selectors containing ::first-line does not match any real HTML element.

For Example:

```css
	p::first-line { 
		text-transform: uppercase 
	}

```


#### `::selection`

- The ::selection CSS pseudo-element applies rules to the portion of a document that has been highlighted (e.g. selected with the mouse or another pointing device) by the user.

For Example:

```css
	/* draw any selected text yellow on red background */
	::-moz-selection { color: gold;  background: red; }
	::selection      { color: gold;  background: red; } 

	/* draw selected text in a paragraph white on black */
	p::-moz-selection { color: white;  background: black; }
	p::selection      { color: white;  background: black; }

```

----
Go back to `CSS` [Table of Content](css.md)


