## Background

- The `background` `CSS` property is a shorthand for setting the individual background values in a single place in the style sheet. 
- It can be used to set the values for one or more of: 
	- `background-color`  
	- `background-image` 
	- `background-position` 
	- `background-repeat`
	- `background-size`
	- `background-attachment`

```css
/* Using a background-color */
background: green;

/* Using a bg-image and repeat-style */
background: url("test.jpg") repeat-y;

/* A single image, centered and scaled */
background: no-repeat center/80% url("../img/image.png");
```

all the above explained below:


### Background Attachment ( `background-attachment` )

- If a `background-image` is specified, the `background-attachment` `CSS` property determines whether that image's position is fixed within the viewport, or scrolls along with its containing block.


#### Values

- `fixed`
    - This keyword means that the background is fixed with regard to the viewport. Even if an element has a scrolling mechanism, a ‘fixed’ background doesn't move with the element.
- `local`
    - This keyword means that the background is fixed with regard to the element's contents: if the element has a scrolling mechanism, the background scrolls with the element's contents, and the background painting area and background positioning area are relative to the scrollable area of the element rather than to the border framing them.
- `scroll`
    - This keyword means that the background is fixed with regard to the element itself and does not scroll with its contents. (It is effectively attached to the element's border.)



### Background Color ( `background-color` )

- The `background-color` `CSS` property sets the background color of an element, either through a color value or the keyword transparent.


#### Values

- `color`
    - It is a CSS `color` that describes the uniform color of the background.
    - Even if one or several background-image are defined, this color can be affect the rendering, by transparency if the images aren't opaque. In CSS, transparent is a color. 


### Background Image ( `background-image` )

- The `CSS` `background-image` property sets one or several background images for an element. The images are drawn on stacking context layers on top of each other. The first layer specified is drawn as if it is closest to the user.

- The borders of the element are then drawn on top of them, and the background-color is drawn beneath them. How the images are drawn relative to the box and its borders is defined by the background-clip and background-origin CSS properties.

- If a specified image cannot be drawn (for example, when the file denoted by the specified URI cannot be loaded), browsers handle it as they would a none value.


#### Values

- `none`
    - It is a keyword denoting the absence of images.
- `image`
    - It is an `image` denoting the image to display. There can be several of them, separated by commas, as multiple backgrounds are supported. 


### Background Position ( `background-position` )

- The `background-position` `CSS` property sets the initial position, relative to the `background position` layer defined by background-origin for each defined background image.


#### Values

- `position
    - It is a `position`, that is one to four values representing a 2D position regarding the edges of the element's box. Relative or absolute offsets can be given. Note that the position can be set outside of the element's box. Default values are:
		-  top;
		-  bottom;
		-  left;
		-  right;
		-  center;.
		-  25% 75%
		-  0px 0px;



### Background Repeat ( `background-repeat` )

- The `background-repeat` `CSS` property defines how background images are repeated. A background image can be repeated along the horizontal axis, the vertical axis, both axes, or not repeated at all.

- By default, the repeated images are clipped to the size of the element, but they can be scaled to fit (using round) or evenly distributed from end to end (using space).


#### Values

- `repeat-style`
   - The one-value syntax is a shorthand for the full two-value syntax:

<table width="100%">
  <tbody>
   <tr>
    <td width="20%"><code>repeat</code></td>
    <td>The image is repeated as much as needed to cover the whole background image painting area. The last image will be clipped if it doesn't fit.</td>
   </tr>
   <tr>
    <td><code>space</code></td>
    <td>The image is repeated as much as possible without clipping. The first and last images are pinned to either side of the element, and whitespace is distributed evenly between the images. The <a href="/en-US/docs/Web/CSS/background-position" title="The background-position CSS property sets the initial position, relative to the background position layer defined by background-origin for each defined background image."><code>background-position</code></a> property is ignored unless only one image can be displayed without clipping. The only case where clipping happens using <code>space</code> is when there isn't enough room to display one image.</td>
   </tr>
   <tr>
    <td><code>round</code></td>
    <td>As the allowed space increases in size, the repeated images will stretch (leaving no gaps) until there is room for another one to be added. When the next image is added, all of the current ones compress to allow room. Example: An image with an original width of 260px, repeated three times, might stretch until each repetition is 300px wide, and then another image will be added. They will then compress to 225px.</td>
   </tr>
   <tr>
    <td><code>no-repeat</code></td>
    <td>The image is not repeated (and hence the background image painting area will not necessarily be entirely covered). The position of the non-repeated background image is defined by the <a href="/en-US/docs/Web/CSS/background-position" title="The background-position CSS property sets the initial position, relative to the background position layer defined by background-origin for each defined background image."><code>background-position</code></a> CSS property.</td>
   </tr>
  </tbody>
 </table>




###  Background Size ( `background-size` ) ![CSS3](http://i.imgur.com/kcw73gq.png)

 - The `background-size` `CSS` property specifies the size of the background images. 
 - The size of the image can be fully constrained or only partially in order to preserve its intrinsic ratio.

####  Values

- `length
    - A `length` value that scales the background image to the specified length in the corresponding dimension. Negative lengths are not allowed.

- `percentage
    - A `percentage` value that scales the background image in the corresponding dimension to the specified percentage of the background positioning area, which is determined by the value of background-origin. The background positioning area is, by default, the area containing the content of the box and its padding; the area may also be changed to just the content or to the area containing borders, padding, and content. If the background's attachment is fixed, the background positioning area is instead the entire area of the browser window, not including the area covered by scrollbars if they are present. Negative percentages are not allowed.

- `auto`
    - A keyword that scales the background image in the corresponding direction such that its intrinsic proportion is maintained.

- `contain`
    - A keyword that scales the image as large as possible and maintains image aspect ratio (image doesn't get squished). Image is letterboxed within the container. When the image and container have different dimensions, the empty areas (either top/bottom of left/right) are filled with the background-color.  The image is automatically centered unless over-ridden by another property such as background-position.

- `cover`
    - A keyword that is the inverse of contain. Scales the image as large as possible and maintains image aspect ratio (image doesn't get squished). The image "covers" the entire width or height of the container. When the image and container have different dimensions, the image is clipped either left/right or top/bottom. 


For Example:

```css
	/* writing all properties separately */
	div {     
		background-color: #f00000; 
    	background-position: center top;
    	background-attachment: scroll;
    	background-repeat: no-repeat;
    	background-size: cover;
    	background-image: url(path-to-file/filename.jpg);
    }

    /* Keeping all the properties at once/using shorthand */
    div {
    	background: url(path-to-file/filename.jpg) no-repeat cover center top #f00000;
    }
```

  
----
Go back to `CSS` [Table of Content](css.md)