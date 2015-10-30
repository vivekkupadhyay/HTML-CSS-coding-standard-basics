## Display

- The `display` `CSS` property specifies the type of rendering box used for an element. 
- In `HTML`, default display property values are taken from behaviors described in the `HTML` specifications or from the browser/user default stylesheet.
- In addition to the many different display box types, the value none lets you turn off the display of an element; when you use none, all descendant elements also have their display turned off. The document is rendered as though the element doesn't exist in the document tree.


For Example:

```css

display: none;
/* Turns off the display of an element (it has no effect on layout); all descendant elements also have their display turned off. The document is rendered as though the element did not exist.
To render an element box's dimensions, yet have its contents be invisible, see the visibility property. */


display: inline;
/* The element generates one or more inline element boxes. */


display: block;
/* The element generates a block element box. */


display: inline-block;
/* The element generates a block element box that will be flowed with surrounding content as if it were a single inline box (behaving much like a replaced element would) */


display: inline-table;
/* The inline-table value does not have a direct mapping in HTML. It behaves like a <table> HTML element, but as an inline box, rather than a block-level box. Inside the table box is a block-level context. */


display: table;
/* These elements behave like  <table> HTML elements. It defines a block-level box. */


display: table-cell;
/* These elements behave like <td> HTML elements. */


display: table-row;
/* These elements behave like <tr> HTML elements. */


display: flex;
/* The element behaves like a block element and lays out its content according to the flexbox model. */


display: inline-flex;
/* The element behaves like an inline element and lays out its content according to the flexbox model. */


/* Global values */
display: inherit;
display: initial;
display: unset;

```


### Overflow ( `overflow` )

- The `overflow` property specifies whether to clip content, render scrollbars or just display content when it overflows its block level container.

- Using the `overflow` property with a value different to visible (its default) will create a new block formatting context. This is technically necessary — if a float intersected with the scrolling element it would forcibly rewrap the content. The rewrap would happen after each scroll step, leading to a slow scrolling experience.

- In order for the `overflow` property to have an effect, the block level container must either have a bounding height (height or max-height) or have white-space set to nowrap.

### overflow-x ( `overflow-x` ) ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `overflow-x` property specifies whether to clip content, render a scroll bar, or display overflow content of a block-level element, when it overflows at the left and right edges.

### overflow-y ( `overflow-y` ) ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `overflow-y` property specifies whether to clip content, render a scroll bar, or display overflow content of a block-level element, when it overflows at the top and bottom edges.


#### Values

- `visible`
    - Default value. Content is not clipped, it may be rendered outside the content box.
- `hidden`
    - The content is clipped and no scrollbars are provided.
- `scroll`
    - The content is clipped and desktop browsers use scrollbars, whether or not any content is clipped. 
    - This avoids any problem with scrollbars appearing and disappearing in a dynamic environment. Printers may print overflowing content.
- `auto`
    - Depends on the user agent. Desktop browsers like Firefox provide scrollbars if content overflows. 


For Example:

```css
	/* Content is not clipped */
	overflow: visible;
	overflow-x: visible;
	overflow-y: visible;

	/* Content is clipped, with no scrollbars */
	overflow: hidden;
	overflow-x: visible;
	overflow-y: visible;

	/* Content is clipped, with scrollbars */
	overflow: scroll;
	overflow-x: visible;
	overflow-y: visible;

	/* Let the browser decide */
	overflow: auto;
	overflow-x: visible;
	overflow-y: visible;

	/* Global values */
	overflow: inherit;
	overflow-x: visible;
	overflow-y: visible;
	overflow: initial;
	overflow-x: visible;
	overflow-y: visible;
	overflow: unset;
	overflow-x: visible;
	overflow-y: visible;

```



----
Go back to `CSS` [Table of Content](css.md)