## Media

### ` @media `

- The `@media` `CSS` at-rule associates a set of nested statements, in a `CSS` block that is delimited by curly braces, with a condition defined by a media query.

- The `@media` at-rule may be used not only at the top level of a `CSS`, but also inside any `CSS` conditional-group at-rule.

For Example:

```css

@media <media-query-list> {
  <group-rule-body>
}

```

#### Media types


> Firefox currently only implements the print and screen media types.  The FullerScreen extension enables support for the projection media type.

- `all`
    - Suitable for all devices.
- `print`
    - Intended for paged material and for documents viewed on screen in print preview mode. Please consult the section on paged media, and the media section of the Getting Started tutorial for information about formatting issues that are specific to paged media.
- `screen`
    - Intended primarily for color computer screens.
- `speech`
    - Intended for speech synthesizers. Note: CSS2 had a similar media type called 'aural' for this purpose. See the appendix on aural style sheets for details. 

<div align="center"><img src="http://i.imgur.com/E2FV4HX.png" align="center" alt="media Anatomy" /></div>


Below are some basic `media-queries`:


```css

	/* Mobile First Method  */

	/* Custom, iPhone Retina */ 
	@media only screen and (min-width : 320px) {
	    
	}

	/* Extra Small Devices, Phones */ 
	@media only screen and (min-width : 480px) {

	}

	/* Small Devices, Tablets */
	@media only screen and (min-width : 768px) {

	}

	/* Medium Devices, Desktops */
	@media only screen and (min-width : 992px) {

	}

	/* Large Devices, Wide Screens */
	@media only screen and (min-width : 1200px) {

	}



	/* Non-Mobile First Method */

	/* Large Devices, Wide Screens */
	@media only screen and (max-width : 1200px) {

	}

	/* Medium Devices, Desktops */
	@media only screen and (max-width : 992px) {

	}

	/* Small Devices, Tablets */
	@media only screen and (max-width : 768px) {

	}

	/* Extra Small Devices, Phones */ 
	@media only screen and (max-width : 480px) {

	}

	/* Custom, iPhone Retina */ 
	@media only screen and (max-width : 320px) {
	    
	}

```		


----
Go back to `CSS` [Table of Content](css.md)