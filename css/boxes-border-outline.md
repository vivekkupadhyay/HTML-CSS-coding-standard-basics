## Boxes/Border/Outline

There are various properties in `CSS` using which we can manage to enhance the content display on our web-page apart from text/font styling.


### Box Shadow ( `box-shadow` )

- The `box-shadow` property describes one or more shadow effects as a comma-separated list. 
- It enables you to cast a drop shadow from the frame of almost any element. 
- If a `border-radius` is specified on the element with a box shadow, the box shadow takes on the same rounded corners. 
- The z-ordering of multiple box shadows is the same as multiple text shadows (the first specified shadow is on top).


#### Values

- `inset`
    - If not specified (default), the shadow is assumed to be a drop shadow (as if the box were raised above the content).
    - The presence of the inset keyword changes the shadow to one inside the frame (as if the content was depressed inside the box). Inset shadows are drawn inside the border (even transparent ones), above the background, but below content.

- `offset-x` - `offset-y`
    - These are two `length` values to set the shadow offset. `offset-x` specifies the horizontal distance. Negative values place the shadow to the left of the element. `offset-y` specifies the vertical distance. Negative values place the shadow above the element.
    - If both values are 0, the shadow is placed behind the element (and may generate a blur effect if `blur-radius` and/or <spread-radius> is set).

- `blur-radius`
    - This is a third `length` value. The larger this value, the bigger the blur, so the shadow becomes bigger and lighter. Negative values are not allowed. If not specified, it will be 0 (the shadow's edge is sharp).

- `spread-radius`
    - This is a fourth `length` value. Positive values will cause the shadow to expand and grow bigger, negative values will cause the shadow to shrink. If not specified, it will be 0 (the shadow will be the same size as the element).

- `color`
    - If not specified, the color used depends on the browser - it is usually the value of the color property, but note that Safari currently paints a transparent shadow in this case. 


For Example:

```css

	/* offset-x | offset-y | color */
	box-shadow: 60px -16px teal;

	/* offset-x | offset-y | blur-radius | color */
	box-shadow: 10px 5px 5px black;

	/* offset-x | offset-y | blur-radius | spread-radius | color */
	box-shadow: 2px 2px 2px 1px rgba(0, 0, 0, 0.2);

	/* inset | offset-x | offset-y | color */
	box-shadow: inset 5em 1em gold;

	/* Any number of shadows, separated by commas */
	box-shadow: 3px 3px red, -1em 0 0.4em olive;

```

![Box Shadow](http://i.imgur.com/7r3R7z3.jpg)


### Border ( `border` )

- The `border` `CSS` property is a shorthand property for setting the individual border property values in a single place in the style sheet. border can be used to set the values for one or more of: border-width, border-style, border-color.

- Like all shorthand properties, a missing value for one of the longhand properties is set to the corresponding initial value. Also note that border-image, though not settable using this shorthand, is reset to its initial value, that is, none. This allows to use border to reset any border settings set earlier in the cascade. As the W3C intends to preserve this property in future level of the spec, it is recommended to use this method to reset border settings


#### Values

- Border Width ( `border-width` )
    - The `border-width` property sets the width of the border of a box. Using the shorthand property `border` is often more convenient.
    - It is either a non-negative explicit `length` value or a keyword denoting the thickness of the bottom border.

- Border Style ( `border-style` )
    - The `border-style` property is a shorthand property for setting the line style for all four sides of the element´s border.

- Border Color ( `border-color` )
    - A `color` denoting the color of the border. If not set, its default value is the value of the element's color property (the text color, not the background color).


For Example:


```css
 
  border: 1px solid black;

```


![Border Width](http://i.imgur.com/Hs7JoyP.jpg)

![Border Style](http://i.imgur.com/jYi7mrB.png)


### Border Radius ( `border-radius` ) ![CSS3](http://i.imgur.com/kcw73gq.png) 

- The `border-radius` `CSS` property allows Web authors to define how rounded border corners are. The curve of each corner is defined using one or two radii, defining its shape: circle or ellipse.

<div align="center"><img src="http://i.imgur.com/4DDNOOF.png" align="center" alt="Border Radius Anatomy" title="Border Radius" /></div>


#### Value

- `length`
    - Denotes the size of the circle radius or the semi-major and semi-minor axes of the ellipsis. It can be expressed in any unit allowed by the CSS <length> data types. Negative values are invalid.
- `percentage`
    - Denotes the size of the circle radius, or the semi-major and semi-minor axes of the ellipsis, using percentage values. Percentages for the horizontal axis refer to the width of the box, percentages for the vertical axis refer to the height of the box. Negative values are invalid. 

For Example:

```css
	border-radius: 1em/5em;

	/* is equivalent to */

	border-top-left-radius:     1em 5em;
	border-top-right-radius:    1em 5em;
	border-bottom-right-radius: 1em 5em;
	border-bottom-left-radius:  1em 5em;

	border-radius: 4px 3px 6px / 2px 4px;

	/* is equivalent to: */

	border-top-left-radius:     4px 2px;
	border-top-right-radius:    3px 4px;
	border-bottom-right-radius: 6px 2px;
	border-bottom-left-radius:  3px 4px;
```

<div align="center"><img src="http://i.imgur.com/R1X81c8.png" align="center" alt="Border Radius Anatomy" title="Border Radius Anatomy" /></div>


### Resize ( `resize` ) ![CSS3](http://i.imgur.com/kcw73gq.png)

- The resize CSS property lets you control the resizability of an element.


#### Values

- `none`
    - The element offers no user-controllable method for resizing the element.
- `both`
    - The element displays a mechanism for allowing the user to resize the element, which may be resized both horizontally and vertically.
- `horizontal`
    - The element displays a mechanism for allowing the user to resize the element, which may only be resized horizontally.
- `vertical`
    - The element displays a mechanism for allowing the user to resize the element, which may only be resized vertically.


For Example:

```css
	textarea.example {
	  resize: none; /* disables resizability */
	}

```


### Box Sizing ( `box-sizing` ) ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `box-sizing` property is used to alter the default CSS box model used to calculate widths and heights of elements. It is possible to use this property to emulate the behavior of browsers that do not correctly support the CSS box model specification.


#### Values

- `content-box`
    - This is the default style as specified by the CSS standard. The width and height properties are measured including only the content, but not the padding, border or margin. Note: Padding, border & margin will be outside of the box.

> e.g. IF `.box {width: 350px}` THEN you apply `{border: 10px solid black;}` RESULT `{rendered in the browser} .box {width: 370px;}`

- `border-box`
    - The width and height properties include the padding and border, but not the margin. This is the box model used by Internet Explorer when the document is in Quirks mode. Note that padding and border will be inside of the box e.g.  `.box {width: 350px; border: 10px solid black;}` lead to a box rendered in the browser of width: 350px. The content box can't be negative and is floored to 0 making it impossible to use border-box to make the element disappear. 



### Outline ( `outline` )

- The CSS outline property is a shorthand property for setting one or more of the individual outline properties outline-style, outline-width and outline-color in a single declaration. In most cases the use of this shortcut is preferable and more convenient.

- Outlines differ from borders in the following ways:
	- Outlines do not take up space, they are drawn above the content.
    - Outlines may be non-rectangular. They are rectangular in Gecko/Firefox. But e.g. Opera draws a non-rectangular shape around a construct like this:


<div align="center"><img src="http://i.imgur.com/Vmnu6dp.jpg" align="center" alt="Outline Anatomy" title="Outline Anatomy" /></div>



#### Values

- Outline Width ( `outline-width` )
    - The `outline-width` `CSS` property is used to set the width of the outline of an element. An outline is a line that is drawn around elements, outside the border edge, to make the element stand out:
- Outline Style ( `outline-style` )
    - The `outline-style` CSS property is used to set the style of the outline of an element. An outline is a line that is drawn around elements, outside the border edge, to make the element stand out.
- Outline Color ( `outline-color` )
   

```css
	/* Keyword values */
	outline-style: auto;
	outline-style: none;
	outline-style: dotted;
	outline-style: dashed;
	outline-style: solid;
	outline-style: double;
	outline-style: groove;
	outline-style: ridge;
	outline-style: inset;
	outline-style: outset;

	/* Global values */
	outline-style: inherit;
	outline-style: initial;
	outline-style: unset;
```

<div align="center"><img src="http://i.imgur.com/Xuylv2h.jpg" align="center" alt="Outline" /></div>



----
Go back to `CSS` [Table of Content](css.md)