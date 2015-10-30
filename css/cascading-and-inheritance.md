## Cascading and Inheritance

`CSS` works on the concept of **Cascading** and **Inheritance** as:


### Cascading

Three main sources of style information form a cascade. They are:
1. The browser's default styles for the markup language.
2. Styles specified by a user who is reading the document.
3. The styles linked to the document by its author. These can be specified in three places:
	 - In an external file.
	 - In a definition at the beginning of the document, use this method only for styles that are used only on that page.
	 - On a specific element in the body of the document, this is the least maintainable method, but can be used for testing.

The user's style modifies the browser's default style. The document author's style then modifies the style some more.


Theoretically for instance when you read this document in a browser:

- part of the style that you see comes from your browser's defaults for `HTML`,

- part of the style might come from customized browser settings or a customized style definition file.

- and part of the style comes from stylesheets linked to the document by the server.

Practically when you open your sample document in your browser:

- the `<strong>` elements are **bolder** than the rest of the text as this comes from the browser's *default style* for `HTML`,

- the `<strong>` elements are ![red](http://i.imgur.com/XdvurDz.jpg) as this comes from your own sample stylesheet.

- the `<strong>` elements also inherit much of the `<p>` element's style, because they are its children. In the same way, the `<p>` element inherits much of the `<body>` element's style.

> For styles in the cascade, author's stylesheets have priority, then reader's stylesheets, then in the last it comes browser's default.

> For inherited styles, a child node's own style has priority over style inherited from its parent.



### Inheritance

Lets say for example we have this `HTML`:

```html
	<p>
	  <strong>C</strong>ascading
	  <strong>S</strong>tyle
	  <strong>S</strong>heets
	</p>
```

now we should write some `CSS` for it also like:

```css
p { 
	text-decoration: underline; 
	color: darkorange; 
}
strong { 
	color: red 
}
```

then it will render on your browser as:

![paragraph css preview](http://i.imgur.com/CypoXXK.jpg)

Here you can easily observer that, `<strong>` element inherits the *properties* of its parent element and renders it on the browser while overriding its parent's `CSS` property with its own.

> Writing parent's `CSS` before child's is more logical because in your document the `<p>` element is the parent of the `<strong>` element.

----
Go back to `CSS` [Table of Content](css.md)