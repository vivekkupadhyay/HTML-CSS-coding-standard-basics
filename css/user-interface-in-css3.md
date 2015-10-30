## User Interface in CSS3 ![CSS3](http://i.imgur.com/kcw73gq.png)

`CSS3` `User Interface` is a module of `CSS3` that allows to define set of rules that will only apply based on capabilities of the processor or the document the style sheet is being applied to.

- Below are some very popular `User Interface` in `CSS3`

### `@document`  ![CSS3](http://i.imgur.com/kcw73gq.png)
 - The `@document` rule is a `CSS3` at-rule that restricts the style rules contained within it based on the URL of the document. It is designed primarily for user style sheets. 
 - A @document rule can specify one or more matching functions. If any of the functions apply to a URL, the rule will take effect on that URL.
 - The main use case is for user-defined stylesheets, though this at-rule can be used on author-defined stylesheets too.
    
    - The functions available are:
		- `url()`, which matches an exact URL
		- `url-prefix()`, which matches if the document URL starts with the value provided
		- `domain()`, which matches if the document URL is on the domain provided (or a subdomain of it)
		- `regexp()`, which matches if the document URL is matched by the regular expression provided. The expression must match the entire URL.


For Example:

```css
	@document url(http://www.w3.org/),
	               url-prefix(http://www.w3.org/Style/),
	               domain(mozilla.org),
	               regexp("https:.*")
	{
	  /* CSS rules here apply to:
	     + The page "http://www.w3.org/".
	     + Any page whose URL begins with "http://www.w3.org/Style/"
	     + Any page whose URL's host is "mozilla.org" or ends with
	       ".mozilla.org"
	     + Any page whose URL starts with "https:" */

	  /* make the above-mentioned pages really ugly */
	  body { color: purple; background: yellow; }
	}
```


### `@supports` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `@supports` `CSS3` at-rule associates a set of nested statements, in a CSS block, that is delimited by curly braces, with a condition consisting of testing of CSS declarations, that is property-value pairs, combined with arbitrary conjunctions, disjunctions, and negations of them. Such a condition is called a supports condition.

- `@supports` gives CSS the ability to perform a feature query.

- The `@supports` at-rule may be used not only at the top level of a CSS, but also inside any CSS conditional-group at-rule and can be accessed via the CSS object model interface CSSSupportsRule.


#### Declaration syntax

- The simplest expression is a `CSS3` declaration, that is a CSS property name followed by a value, separated by a colon. The following expression

```css
	( transform-origin: 5% 5% )
	/* returns true if the transform-origin 
	   implements a syntax considering 5% 5% as valid. */
```

- A CSS declaration is always surrounded by parentheses.

- The `not` operator 
	- The not operator can precede any expression to create a new expression, resulting in the negation of the original expression.

```css
	not ( transform-origin: 10em 10em 10em )
    /* returns true if transform-origin doesn't implement 
       a syntax considering 10em 10em 10em as valid. */
    
    /* Like any operator, the not operator can be 
       applied to a declaration of any complexity. 
       The following examples are all valid expressions: */
	not ( not ( transform-origin: 2px ) )
    (display: flexbox) and ( not (display: inline-grid) )
```

> There is no need to enclose the not operator between two parenthesis when at the top level. But to combine it with other operators, like and and or, the parenthesis are required.


- The `and` operator

- From two expressions, the and operator creates a new expression consisting in the conjunction of the two original ones, that is the resulting expression is true only if both of the original expressions also resolve to true. In this example, the complete expression resolves to true if and only if the two expressions are simultaneously true:

```css
	(display: table-cell) and (display: list-item)

	/* Several conjunctions can be juxtaposed without the need of more parenthesis: */
    (display: table-cell) and (display: list-item) and (display:run-in)
	/* is equivalent to: */
	(display: table-cell) and ((display: list-item) and (display:run-in))
	
```


- The `or` operator

- From two expressions, the or operator creates a new expression consisting in the disjunction of the two original ones, that is the resulting expression is true if one, or both, of the original expressions also resolves to true. In this example, the complete expression resolves to true if at least one of the two expressions is true:

```css
	( transform-style: preserve ) or ( -moz-transform-style: preserve )
	Several disjunctions can be juxtaposed without the need of more parenthesis:

	( transform-style: preserve ) or ( -moz-transform-style: preserve ) or 
	( -o-transform-style: preserve ) or ( -webkit-transform-style: preserve  )
	is equivalent to:

	( transform-style: preserve-3d ) or (( -moz-transform-style: preserve-3d ) or 
	(( -o-transform-style: preserve-3d ) or ( -webkit-transform-style: preserve-3d  )))
```

For Examples:

- Testing for the support of a given CSS property

```css
@supports (animation-name: test) {
    … /* specific CSS applied when animations are supported unprefixed */
    @keyframes { /* @supports being a CSS conditional group at-rule, it can includes other relevent at-rules */
      …
    }
}
```

- Testing for the support of a given CSS property or a prefixed version

```css
@supports ( (perspective: 10px) or (-moz-perspective: 10px) or (-webkit-perspective: 10px) or
            (-ms-perspective: 10px) or (-o-perspective: 10px) ) {
    … /* specific CSS applied when 3D transforms, eventually prefixed, are supported */
}
```

- Testing for the non-support of a specific CSS property

```css
@supports not ((text-align-last:justify) or (-moz-text-align-last:justify) ){
    … /* specific CSS applied to simulate text-align-last:justify */
}
```

### `@media` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `@media` `CSS3` at-rule associates a set of nested statements, in a CSS block that is delimited by curly braces, with a condition defined by a media query. The @media at-rule may be used not only at the top level of a CSS, but also inside any CSS conditional-group at-rule.

- The `@media` at-rule can be accessed via the CSS object model interface CSSMediaRule.

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

For Example:

```css
	@media print {
		body { font-size: 10pt }
	}
	@media screen {
		body { font-size: 13px }
	}
	@media screen, print {
		body { line-height: 1.2 }
	}
```

<div align="center"><img src="http://i.imgur.com/q3Ack6g.png" align="center" alt="media tag Anatomy" title="media tag Anatomy" /></div>



----
Go back to `CSS` [Table of Content](css.md)