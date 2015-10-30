## Position

- The position CSS property chooses alternative rules for positioning elements, designed to be useful for scripted animation effects.

> The top, right, bottom, and left properties specify the position of positioned elements.


```css
	/* Keyword values */
	position: static;
	position: relative;
	position: absolute;
	position: fixed;
	position: sticky;

	/* Global values */
	position: inherit;
	position: initial;
	position: unset;
```

#### Values

- `static`
    - This keyword lets the element use the normal behavior, that is it is laid out in its current position in the flow.  The top, right, bottom, left and z-index properties do not apply.
- `relative`
    - This keyword lays out all elements as though the element were not positioned, and then adjust the element's position, without changing layout (and thus leaving a gap for the element where it would have been had it not been positioned). The effect of position:relative on table-*-group, table-row, table-column, table-cell, and table-caption elements is undefined.
- `absolute`
    - Do not leave space for the element. Instead, position it at a specified position relative to its closest positioned ancestor or to the containing block. Absolutely positioned boxes can have margins, they do not collapse with any other margins.
- `fixed`
    - Do not leave space for the element. Instead, position it at a specified position relative to the screen's viewport and don't move it when scrolled. When printing, position it at that fixed position on every page. This value always create a new stacking context. 

----
Go back to `CSS` [Table of Content](css.md)