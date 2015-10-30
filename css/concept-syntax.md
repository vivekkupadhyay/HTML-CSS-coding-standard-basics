## Concept & Syntax

I personally think "why should we use `CSS`?" will be a pointless question whereas "how to use `CSS`?" will be having high shares and everyone now will be eager to use it, so lets begin.

- The main idea behind using `CSS` is to manage look and feel of any `HTML` page, that *how it should appear on browser?* and *how you can highlight the major and important content on any `HTML` document?*
- And the main advantage of using `CSS` over `HTML` is that the styling can be kept entirely separate from the content.
- The basic goal of the `CSS` language is to allow a browser engine to paint elements of the page with specific features, like *colors*, *positioning*, or *decorations*. The CSS syntax reflects this goal and its basic building blocks are:
	- The *property* which is an identifier, that is a human-readable name, that defines which feature is considered.
    - The *value* which describe how the feature must be handled by the engine. Each property has a set of valid values, defined by a formal grammar, as well as a semantic meaning, implemented by the browser engine.


### CSS declarations

- Setting `CSS` properties to specific values is the core function of the `CSS` language, and **a property and value pair is called a declaration**.

- Any `CSS` engine calculates which declarations apply to every single element of a page in order to appropriately lay it out, and to style it as:


<div align="center"><img src="http://i.imgur.com/FKjlnL8.png" align="center" alt="CSS declarations" /></div><br />



> Both *properties* and *values* are *case-sensitive* in `CSS`. The pair is separated by a colon, ` : `, and *white spaces before, between, and after* properties and values, but not necessarily inside, are ignored.


### CSS Readability

- You can add `white space` and `comments` to your **stylesheets** to make them more **readable**.
	- `white space` means actual spaces, tabs and new lines. You can add white space to make your stylesheets more readable.
	- `comments` in `CSS` begin with ` /* ` and end with ` */ `. You can use comments to make actual comments in your stylesheet, and also to comment out parts of it temporarily for testing purposes.

- You can also group `selectors` together, when the same style rules apply to elements selected in different ways.

For Examples:

> Some people like the compact layout that we have been using, only splitting a line when it becomes very long:

```css
/* style for initial vegetable carrot */
.carrot {color: orange; text-decoration: underline; font-style: italic;}
```

> Some people prefer one property-value per line:

```css
.carrot
{
color: orange;
text-decoration: underline;
font-style: italic;
}
```

> Some people use indention—two spaces, four spaces, or a tab are common:

```css
.carrot {
  color: orange;
  text-decoration: underline;
  font-style: italic;
}
```

> Some people like everything to line up vertically (but a layout like this is difficult to maintain):

```css
.carrot
    {
    color           : orange;
    text-decoration : underline;
    font-style      : italic;
    }
```

> Some people use mixed whitespace to enhance readability.

```css
/* style for all vegetables */
.vegetable         { color: green; min-height:  5px; min-width:  5px }
.vegetable.carrot  { color: orange;    height: 90px;     width: 10px }
.vegetable.spinach { color: darkgreen; height: 30px;     width: 30px }
```


----
Go back to `CSS` [Table of Content](css.md)
