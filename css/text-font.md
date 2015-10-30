## Text/Font 

Using `CSS` we can modify content on our web-page viz in the end of the day is **Text** only.

### Font Family ( `font-family` )

- The `font-family` `CSS` property lets you specify a prioritized list of font family names and/or generic family names for the selected element. 
- Values are separated by a comma `, `  to indicate that they are alternatives. The browser will select the first font on the list that is installed on the computer or that can be downloaded using a `@font-face` at-rule.

- Web authors should always add at least **one generic family** in a font-family list, since there's no guarantee that a specific font is installed on the computer or can be downloaded using a @font-face at-rule. The generic family lets the browser select an acceptable fall-back font when needed.

> It is often convenient to use the shorthand property font to set font-size and other font related properties all at once.

For example:

```css
	body {
		font-family: "Consolas", Courier New, lucida console, monospace;
	}
```

#### Values

- `<family-name>`
    - The name of a font family. For example, **"Times"** and **"Helvetica"** are font families. Font family names **containing whitespace should be quoted**.

- `<generic-name>`
    - Generic font families are a fall-back mechanism, a means of preserving some of the style sheet author's intent when none of the specified fonts are available. Generic family names are keywords and must not be quoted. A generic font family should be the last item in the list of font family names. The following keywords are defined:

![Font family defined](http://i.imgur.com/NLCgFRQ.jpg)


### Font Size ( `font-size` )

- The `font-size` `CSS` property specifies the size of the font. 
- Setting the font size may, in turn, change the size of other items, since it is used to compute the value of the `em`, `rem` and `px`.

> **rem**, rem values were invented in order to sidestep the compounding problem. *rem values are relative to the root html element*, not the parent element. In other words, it lets you specify a font size in a relative fashion without being affected by the size of the parent, thereby eliminating compounding.

For example:

```css
	html {
  		font-size: 62.5%; /* font-size 1em = 10px on default browser settings */
	}
	span {
  		font-size: 1.6rem;
	}
```


> **em** (desired element pixel value / parent element font-size in pixels), Another way of setting the font size is with `em` values. The size of an em value is dynamic. When defining the font-size property, an em is equal to the size of the font that applies to the parent of the element in question. If you haven't set the font size anywhere on the page, *then it is the browser default, which is probably 16px. So, by default 1em = 16px, and 2em = 32px*. If you set a font-size of 20px on the body element, then 1em = 20px and 2em = 40px. *Note that the value 2 is essentially a multiplier of the current em size*.

For example:

```css
	body {
  		font-size: 62.5%; /* font-size 1em = 10px on default browser settings */
	}
	span {
  		font-size: 1.6em; /* 1.6em = 16px */
	}

```


> **px**, setting the font size in `pixel values` ( `px` ) is a good choice when you need pixel accuracy. A `px` value is static. This is an OS-independent and cross-browser way of literally telling the browsers to render the letters at exactly the number of pixels in height that you specified. The results may vary slightly across browsers, as they may use different algorithms to achieve a similar effect.

For example:

```css
	body {
  		font-size: 14px;
  	}	
```


### Font Style ( `font-style` )

- The `font-style` `CSS` property lets you select *italic* or *oblique* faces within a font-family.

#### Values

- Italic forms are generally cursive in nature while oblique faces are typically sloped versions of the regular face. Oblique faces can be simulated by artificially sloping the glyphs of the regular face.
	- `normal`
    	- Selects a font that is classified as normal within a font-family
	- `italic`
    	- Selects a font that is labeled italic, if that is not available, one labeled oblique
	- `oblique`
    	- Selects a font that is labeled oblique 

For example:

```css
	.normal {
	  font-style: normal;
	}

	.italic {
	  font-style: italic;
	}

	.oblique {
	  font-style: oblique;
	}
```

### Font Weight ( `font-weight` )

- The `font-weight` `CSS` property specifies the weight or boldness of the font. Some fonts are only available in normal and bold.

#### Values


- `normal`
    	- Normal font weight.
- `bold`
    	- Bold font weight.
- `lighter`
    	- One font weight lighter than the parent element.
- `bolder`
    	- One font weight darker than the parent element.
- 100 (Thin Hairline), 200(Extra Light (Ultra Light)), 300(Light), 400(Normal), 500(Medium), 600(Semi Bold (Demi Bold)), 700(Bold), 800(Extra Bold (Ultra Bold)), 900(Black (Heavy))

For Example:

```css
	/* Set paragraph text to be bold. */
	p { font-weight: bold; }

	/* Set h1 (level 1 heading) text to one step darker than
	   normal but less than a standard bold. */
	h1 { font-weight: 500; }

	/* Sets text enclosed within span tag to be one step lighter
	   than the parent. */
	span { font-weight: lighter; }
```

### Line Height ( `line-height` )

- On block level elements, the `line-height` property specifies the minimum height of line boxes within the element.


#### Values


- `normal`
    	- Depends on the user agent. Desktop browsers (including Firefox) use a default value of roughly 1.2, depending on the element's font-family.
- `number`
    	- The used value is this unitless `number` multiplied by the element's font size. The computed value is the same as the specified `number`. In most cases this is the preferred way to set line-height with no unexpected results in case of inheritance.
- `length`
    	- The specified `length` is used in the calculation of the line box height. See <length> values for possible units.
- `percentage`
    	- Relative to the font size of the element itself. The computed value is this `percentage`multiplied by the element's computed font size.

> Percentage and em values may have unexpected results, see "Notes" section. 

For Example:

```css
	/* All rules below have the same resultant line height */

	h2 { line-height: 1.2;   font-size: 10pt }   /* number */ 
	h2 { line-height: 1.2em; font-size: 10pt }   /* length */ 
	h2 { line-height: 120%;  font-size: 10pt }   /* percentage */
	h2 { line-height: 12pt;  font-size: 10pt }   /* length */

```


### Color ( `color` )

- The `color` property sets the foreground color of an element's text content, and its decorations. 
- It doesn't affect any other characteristic of the element; it should really be called text-color and would have been named so, save for historical reasons and its appearance in CSS Level 1.

> the `color` value must be a uniform color, which may include a transparency value from `CSS3` onwards. It can't be a `gradient` which is an `image` in CSS.

For Example:

```css
	h2 { color: red }
	h2 { color: #f00 }
	h2 { color: #ff0000 }
	h2 { color: rgb(255,0,0) }
	h2 { color: rgb(100%, 0%, 0%) }
	h2 { color: hsl(0, 100%, 50%) }

	/* 50% translucent */
	h2 { color: rgba(255, 0, 0, 0.5) } 
	h2 { color: hsla(0, 100%, 50%, 0.5) }
```

### Opacity ( `opacity` ) ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `opacity` `CSS` property specifies the transparency of an element, that is, the degree to which the background behind the element is overlaid.

- The value applies to the element as a whole, including its contents, even though the value is not inherited by child elements. Thus, an element and its contained children all have the same opacity relative to the element's background, even if the element and its children have different opacities relative to one another.

For Example:

```css
	/* Fully opaque */
	opacity: 1;
	opacity: 1.0;

	/* Translucent */
	opacity: 0.6;

	/* Fully transparent */
	opacity: 0.0;
	opacity: 0;

	/* Global values */
	opacity: inherit;
	opacity: initial;
	opacity: unset;
	background: rgba(0, 0, 0, 0.4);

```


### Text Align ( `text-align` )

- The `text-align` `CSS` property describes how inline content like text is aligned in its parent block element. text-align does not control the alignment of block elements itself, only their inline content.


#### Values


- `left`
    - The inline contents are aligned to the left edge of the line box.
- `right`
    - The inline contents are aligned to the right edge of the line box.
- `center`
    - The inline contents are centered within the line box.
- `justify`
    - The text is justified. Text should line up their left and right edges to the left and right content edges of the paragraph.

For Example:

```css
	/* Keyword values */
	h2 { text-align: left; }
	h2 { text-align: right; }
	h2 { text-align: center; }
	h2 { text-align: justify; }

	/* Global values */
	h2 { text-align: inherit; }
	h2 { text-align: initial; }
	h2 { text-align: unset; }

```

### Text Decoration ( `text-decoration` )

- The `text-decoration` `CSS` property is used to set the text formatting to `underline`, `overline`, `line-through` or blink.

- Text decorations draw across descendant elements. This means that it is not possible to disable on a descendant a text decoration that is specified on one of its ancestors.


#### Values

- `underline`
- `overline`
- `line-through` 


For Example:

```css
	h1.under {
		text-decoration: underline;
	}
	h1.over {
		text-decoration: overline;
	}
	p.line {
		text-decoration: line-through;
	}
	p.blink {
		text-decoration: blink;
	}
	a.none {
		text-decoration: none;
	}
	p.underover {
		text-decoration: underline overline;
	}
```


### Text Indent ( `text-indent` )

- The `text-indent` property specifies how much horizontal space should be left before the beginning of the first line of the text content of an element.

- Horizontal spacing is with respect to the left (or right, for right-to-left layout) edge of the containing block element's box.


#### Value

- `length`
    - Indentation is specified as an absolute `length`. Negative values are allowed. See <length> values for possible units.
- `percentage`
    - Indentation is a `percentage` of the containing block width.


For Example:

```css
	/* length values */
	h2 { 
		text-indent: 3em; 
	}

	/* <percentage> value relative to the containing block width */
	h3 { 
		text-indent: 30%; 
	}

```

### Text Overflow ( `text-overflow` ) ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `text-overflow` property determines how overflowed content that is not displayed is signaled to users. It can be clipped, display an ellipsis ('…', U+2026 Horizontal Ellipsis), or display a custom string.

<div align="center"><img src="http://i.imgur.com/tY8sKpJ.png" align="center" alt="text-overflow" /></div>


#### Value

- `clip`
    - This keyword value indicates to truncate the text at the limit of the content area, therefore the truncation can happen in the middle of a character. To truncate at the transition between two characters, the empty string value ('') must be used. The value clip is the default for this property.
- `ellipsis`
    - This keyword value indicates to display an ellipsis ('…', U+2026 Horizontal Ellipsis) to represent clipped text. The ellipsis is displayed inside the content area, decreasing the amount of text displayed. If there is not enough space to display the ellipsis, it is clipped.


For Example:

```css
	p {
	  white-space: nowrap;
	  width: 100%;                   
	  overflow: hidden;              /* "overflow" value must be different from "visible" */ 
	  text-overflow: ellipsis;
	}
```


### Text Shadow ( `text-shadow` ) ![CSS3](http://i.imgur.com/kcw73gq.png)
- The `text-shadow` property adds shadows to text. It accepts a comma-separated list of shadows to be applied to the text and text-decorations of the element.

- Each shadow is specified as an offset from the text, along with optional color and blur radius values.

- Multiple shadows are applied front-to-back, with the first-specified shadow on top.


#### Value

- `color`
    - Optional. Can be specified either before or after the offset values. If the color is not specified, a UA-chosen color will be used.

> If you want to ensure consistency across browsers, explicitly specify a color.

- `offset-x` - `offset-y`
    - Required. These`length` values specify the shadow's offset from the text.`offset-x` specifies the horizontal distance; a negative value places the shadow to the left of the text.`offset-y` specifies the vertical distance; a negative value places the shadow above the text. If both values are 0, then the shadow is placed behind the text (and may generate a blur effect when`blur-radius` is set).
- `blur-radius`
    - Optional. This is a <length> value. If not specified, it defaults to 0. The higher this value, the bigger the blur; the shadow becomes wider and lighter. 


For Example:

```css
	h2 {
	   text-shadow: 1px 1px 2px black;
	   color: white;
	}
```


### Text Transform ( `text-transform` )


- The `text-transform` `CSS` property specifies how to capitalize an element's text. It can be used to make text appear in all-uppercase or all-lowercase, or with each word capitalized.


#### Values

- `capitalize`
	- It is a keyword forcing the first letter of each word to be converted to uppercase. Other characters are unchanged.

> Authors should not expect capitalize to follow language-specific titlecasing conventions (such as skipping articles in English).

- `uppercase`
   - It is a keyword forcing all characters to be converted to uppercase.

- `lowercase`
    - It is a keyword forcing all characters to be converted to lowercase.

- `none`
   - It is a keyword preventing the case of all characters to be changed.


For Example:

```css
	p { 
		text-transform: none;
	}

	p { 
		text-transform: capitalize; 
	}

	p { 
		text-transform: uppercase; 
	}

	p { 
		text-transform: lowercase; 
	}

```


### Word Break ( `word-break` ) ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `word-break` CSS property is used to specify whether to break lines within words.


#### Values

- `normal`
    - Use the default line break rule.
- `break-all`
    - Word breaks may be inserted between any character for non-CJK (Chinese/Japanese/Korean) text.
- `keep-all`
    - Don't allow word breaks for CJK text.  Non-CJK text behavior is the same as for normal. 

For Example:

```css
	/* Keyword values */
	word-break: normal; 
	word-break: break-all; 
	word-break: keep-all;

	/* Global values */
	word-break: inherit;
	word-break: initial;
	word-break: unset;

```

### Word Wrap ( `word-wrap` ) ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `word-wrap` property is used to specify whether or not the browser may break lines within words in order to prevent overflow when an otherwise unbreakable string is too long to fit in its containing box.


#### Values

- `normal`
    - Indicates that lines may only break at normal word break points.
- `break-word`
    - Indicates that normally unbreakable words may be broken at arbitrary points if there are no otherwise acceptable break points in the line. 


For Example:

```css
	/* Keyword values */
	word-wrap: normal;
	word-wrap: break-word;

	/* Global values */
	word-wrap: inherit;
	word-wrap: initial;
	word-wrap: unset;

```


----
Go back to `CSS` [Table of Content](css.md)