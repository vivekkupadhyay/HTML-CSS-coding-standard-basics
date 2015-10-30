## Margin & Padding

In `CSS` we can use `margin` and `padding` properties to manage our `HTML` elmenents postion and elements inside them.


### Margin ( `margin` )

- The `margin` `CSS` property sets the margin for all four sides. 
- It is a shorthand to avoid setting each side separately with the other margin properties: 
	- margin-top
	- margin-right
	- margin-bottom
	- margin-left

#### Values

- `length`
    - Specifies a fixed width. *Negative Values are allowed*.
- `percentage`
    - A `percentage` relative to the width of the containing block. *Negative values are allowed*.
- auto
    - auto is replaced by some suitable value, e.g. it can be used for centering of blocks.
    div { width:50%;  margin:0 auto; } centers the div container horizontally.

> One single value applies to all four sides.
> Two values apply first to top and bottom, the second one to left and right.
> Three values apply first to top, second to left and right and third to bottom.
> Four values apply to top, right, bottom and left in that order (clockwise).

For Example:

```css
	/* Apply to all four sides */
	margin: 1em;

	/* vertical | horizontal */
	margin: 5% auto;

	/* top | horizontal | bottom */
	margin: 1em auto 2em; 

	/* top | right | bottom | left */
	margin: 2px 1em 0 auto;

	margin: 5%;                /* all sides 5% margin */

	margin: 10px;              /* all sides 10px margin */

	margin: 1.6em 20px;        /* top and bottom 1.6em, left and right 20px margin */

	margin: 10px 3% 1em;       /* top 10px, left and right 3%, bottom 1em margin */

	margin: 10px 3px 30px 5px; /* top 10px, right 3px, bottom 30px, left 5px margin */

	margin: 1em auto;          /* 1em margin on top and bottom, box is horizontally centered */

	margin: auto;              /* box is horizontally centered, 0 margin on top and bottom */

	/* horizontal centering with */ 
	margin: 0 auto;

	/* Global values */
	margin: inherit;
	margin: initial;
	margin: unset;

```



### Padding ( `padding` )

- The `padding` property sets the padding space on all sides of an element. 
- The `padding` area is the space between the content of the element and its border. *Negative values are not allowed*.
- The padding property is a shorthand to avoid setting each side separately:
	- padding-top
	- padding-right
	- padding-bottom
	- padding-left


#### Values


- `length 
    - Specifies a non-negative fixed width. See <length> for details.
- `percentage 
    - With respect to the width of the containing block.

> One single value applies to all 4 sides
> Two values apply to 1. top and bottom and 2. to the left and right side
> Three values apply to 1. top, 2. right and left and 3. to the bottom side
> Four values apply to 1. top, 2. right, 3. bottom and 4. to the left side

For Example:

```css
	/* Apply to all four sides */
	padding: 1em;

	/* vertical | horizontal */
	padding: 5% 10%;

	/* top | horizontal | bottom */
	padding: 1em 2em 2em; 

	/* top | right | bottom | left */
	padding: 2px 1em 0 1em;

	/* Global values */
	padding: inherit;
	padding: initial;
	padding: unset;

	padding: 5%;                /* on all sides 5% padding */

	padding: 10px;              /* on all sides 10px padding */

	padding: 10px 20px;         /*  top and bottom 10px padding  */
	                             /*  left and right 20px padding  */

	padding: 10px 3% 20px;      /*  top 10px padding          */
	                             /*  left and right 3% padding */
	                             /*  bottom 20px padding       */

	padding: 1em 3px 30px 5px;  /*  top    1em  padding  */
	                             /*  right  3px  padding  */
	                             /*  bottom 30px padding  */
	                             /*  left   5px  padding  */

```


----
Go back to `CSS` [Table of Content](css.md)