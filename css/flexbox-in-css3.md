## Flexbox in CSS3 ![CSS3](http://i.imgur.com/kcw73gq.png)

The `CSS3` `Flexible Box`, or `flexbox`, is a layout mode providing for the arrangement of elements on a page such that the elements behave predictably when the page layout must accommodate different screen sizes and different display devices. For many applications, the flexible box model provides an improvement over the block model in that it does not use floats, nor do the flex container's margins collapse with the margins of its contents.

Many designers will find the flexbox model easier to use. Child elements in a flexbox can be laid out in any direction and can have flexible dimensions to adapt to the display space. Positioning child elements is thus much easier, and complex layouts can be achieved more simply and with cleaner code, as the display order of the elements is independent of their order in the source code. This independence intentionally affects only the visual rendering, leaving speech order and navigation based on the source order.


### Flexible boxes vocabulary

While a discussion of flexible boxes is liberated from terms like horizontal/inline axis and vertical/block axis, it requires a new terminology to properly describe the model. Consider the following diagram when reviewing the vocabulary items below. It shows a flex container that has a flex-direction of row, meaning that the flex items follow each other horizontally across the main axis according to the established writing mode, the direction in which the element's text flows, in this case left-to-right.


 
- `Flex container`
    - The parent element in which flex items are contained. A flex container is defined using the flex or inline-flex values of the display property.
- `Flex item`

    - Each child of a flex container becomes a flex item. Text directly contained in a flex container is wrapped in an anonymous flex item.
- `Axes`

    - Every flexible box layout follows two axes. The main axis is the axis along which the flex items follow each other. The cross axis is the axis perpendicular to the main axis.

        - The flex-direction property establishes the main axis.
        - The justify-content property defines how flex items are laid out along the main axis on the current line.
        - The align-items property defines the default for how flex items are laid out along the cross axis on the current line.
        - The align-self property defines how a single flex item is aligned on the cross axis, and overrides the default established by align-items.

- `Directions`

    - The main start/main end and cross start/cross end sides of the flex container describe the origin and terminus of the flow of flex items. They follow the main axis and cross axis of the flex container in the vector established by the writing-mode (left-to-right, right-to-left, etc.).

        - The order property assigns elements to ordinal groups and determines which elements appear first.
        - The flex-flow property shorthands the flex-direction and flex-wrap properties to lay out the flex items.

- `Lines`

    - Flex items can be laid out on either a single line or on several lines according to the flex-wrap property, which controls the direction of the cross axis and the direction in which new lines are stacked.
- `Dimensions`

    - The flex items' agnostic equivalents of height and width are main size and cross size, which respectively follow the main axis and cross axis of the flex container.

        - The min-height and min-width properties initial value is 0.
        - The flex property shorthands the flex-grow, flex-shrink, and flex-basis properties to establish the flexibility of the flex items.



### `flex` ![CSS3](http://i.imgur.com/kcw73gq.png)


- The `flex` `CSS3` property is a shorthand property specifying the ability of a flex item to alter its dimensions to fill available space. Flex items can be stretched to use available space proportional to their flex grow factor or their flex shrink factor to prevent overflow.


#### `flex-grow` 


- The `flex-grow` `CSS3` property specifies the flex grow factor of a flex item. 
- It specifies what amount of space inside the flex container the item should take up.  
- Defines the flex-grow of the flex item. Negative values are considered invalid. Defaults to 1 when omitted.

For Example:

```css
	flex-grow: 3;

	/* Global values */
	flex-grow: inherit;
	flex-grow: initial;
	flex-grow: unset;
```


#### `flex-shrink` 


-  The `flex-shrink` `CSS3` property specifies the flex shrink factor of a flex item.
- Defines the flex-shrink of the flex item. Negative values are considered invalid. Defaults to 1 when omitted.

For Example:

```css
	flex-shrink: 2;

	/* Global values */
	flex-shrink: inherit;
	flex-shrink: initial;
	flex-shrink: unset;
```    

#### `flex-basis` 


-  The `flex-basis` `CSS3` property specifies the flex basis which is the initial main size of a flex item. This property determines the size of the content-box unless specified otherwise using box-sizing.
- Defines the flex-basis of the flex item. Any value valid for width and height properties are accepted. A preferred size of 0 must have a unit to avoid being interpreted as a flexibility. Defaults to 0% when omitted.

##### Values

- `width`
    - Defined as a number followed by a absolute unit such as px, mm or pt, or a percentage of the parent flex container main size property. Negative values are invalid.
- `content`
    - Indicates automatic sizing, based on the flex item’s content.    

For Example:

```css
	/* Specify <'width'> */
	flex-basis: 10em;      
	flex-basis: 3px;
	flex-basis: auto;

	/* Intrinsic sizing keywords */
	flex-basis: fill;
	flex-basis: max-content;
	flex-basis: min-content;
	flex-basis: fit-content;

	/* Automatically size based on the flex item’s content */
	flex-basis: content;

	/* Global values */
	flex-basis: inherit;
	flex-basis: initial;
	flex-basis: unset;
```

#### `flex-direction` 


-  The `flex-direction` `CSS3` property specifies how flex items are placed in the flex container defining the main axis and the direction (normal or reversed).

> The value `row` and `row-reverse` are affected by the directionality of the flex container. If its dir attribute is ltr, row represents the horizontal axis oriented from the left to the right, and row-reverse from the right to the left; if the dir attribute is rtl, row represents the axis oriented from the right to the left, and row-reverse from the left to the right.

##### Values

- `row`
    - The `flex container`'s main-axis is defined to be the same as the text direction. The main-start and main-end points are the same as the content direction.
- `row-reverse`
    - Behaves the same as row but the main-start and main-end points are permuted.
- `column`
    - The flex container's main-axis is the same as the block-axis. The main-start and main-end points are the same as the before and after points of the writing-mode.
- `column-reverse`
    - Behaves the same as column but the main-start and main-end are permuted. 

For Example:

```css
	/* The direction text is laid out in a line */
	flex-direction: row;

	/* Like <row>, but reversed */
	flex-direction: row-reverse;

	/* The direction in which lines of text are stacked */
	flex-direction: column;

	/* Like <column>, but reversed */
	flex-direction: column-reverse;

	/* Global values */
	flex-direction: inherit;
	flex-direction: initial;
	flex-direction: unset;
```

#### `flex-flow` 


- The `flex-flow` `CSS3` property is a shorthand property for flex-direction and flex-wrap individual properties.

For Example:

```css
	/* flex-flow: flex-direction */
	flex-flow: row;
	flex-flow: row-reverse;
	flex-flow: column;
	flex-flow: column-reverse;

	/* flex-flow: flex-wrap */
	flex-flow: nowrap;
	flex-flow: wrap;
	flex-flow: wrap-reverse;

	/* flex-flow: flex-direction and flex-wrap */
	flex-flow: row nowrap;
	flex-flow: column wrap;
	flex-flow: column-reverse wrap-reverse;

	/* Global values */
	flex-flow: inherit;
	flex-flow: initial;
	flex-flow: unset;
```

#### `flex-wrap` 




-  The `CSS3` `flex-wrap` property specifies whether flex items are forced into a single line or can be wrapped onto multiple lines. If wrapping is allowed, this property also enables you to control the direction in which lines are stacked.


##### Values

- `nowrap`
    - The flex items are laid out in a single line which may cause the flex container to overflow. The cross-start is either equivalent to start or before depending flex-direction value.
- `wrap`
    - The flex items break into multiple lines. The cross-start is either equivalent to start or before depending flex-direction value and the cross-end is the opposite of the specified cross-start.
- `wrap-reverse`
    - Behaves the same as wrap but cross-start and cross-end are permuted. 

For Example: 

```css
	flex-wrap: nowrap;
	flex-wrap: wrap;
	flex-wrap: wrap-reverse;

	/* Global values */
	flex-wrap: inherit;
	flex-wrap: initial;
	flex-wrap: unset;
```



















For Example:

```
	#flex-container {
		display: -webkit-flex;
		display: flex;
		-webkit-flex-direction: row;
		flex-direction: row;
	}

	#flex-container > .flex-item {
		-webkit-flex: auto;
		flex: auto;
	}

	#flex-container > .raw-item {
		width: 5rem;
	}

	<div id="flex-container">
	    <div class="flex-item" id="flex">Flex box (click to toggle raw box)</div>
	    <div class="raw-item" id="raw">Raw box</div>
	</div>
```



----
Go back to `CSS` [Table of Content](css.md)