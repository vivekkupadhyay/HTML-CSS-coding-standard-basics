## CSS Selectors

`CSS` has its own terminology to describe the `CSS` language.

For example

```css
	strong {
		color: red;
	}
```

In `CSS` terminology: this entire line is a rule. This rule starts with **strong**, which is a **selector**. It selects which elements in the **DOM** the rule applies to.


> The part inside the curly braces `{ ... }` is the **declaration**.

> The keyword `color` is a **property**, and `red` is a **value**.

> The semicolon ` ; ` after the property-value pair separates it from other property-value pairs in the same declaration.


### Class selectors

- Use the `class` **attribute** in an element to assign the element to a named `class`. It is up to you what name you choose for the `class`. Multiple elements in a document can have the same `class` value.

> In your stylesheet, type a **full stop** (period) ` . ` before the class name when you use it in a selector.

### ID selectors

- Use the `id` **attribute** in an element to assign an `ID` to the element. It is up to you what name you choose for the `ID`. The `ID` name **must be unique** in the document.

> In your stylesheet, type a number sign (hash) before the ID when you use it in a selector.


For Example:

This `HTML` tag has both a `class` attribute and an `id` attribute:

```html
<p class="student" id="teacher">
```

- The `id` value, **teacher**, must be unique in the document, but other tags in the document can have the same `class` name, **student**.

- In a `CSS` stylesheet, this rule makes all the elements with `class` **student** ![green text](http://i.imgur.com/f1rsyiE.jpg).

```css
	.student {
	  color: green;
	}
```

- This rule makes the one element with the id principal bold:

```css
	#teacher {
	  font-weight: bold;
	}
```


----
Go back to `CSS` [Table of Content](css.md)