## Content

- The `content` `CSS` property is used with the `::before` and `::after` pseudo-elements to generate content in an element. Objects inserted using the content property are anonymous replaced elements.


#### Values

- none
    - The pseudo-element is not generated.
- normal
    - Computes to none for the :before and :after pseudo-elements.
- `string`
    - Text content.
- `uri` or `url()`
    - The value is a URI that designates an external resource (such as an image). If the resource or image can't be displayed, it is either ignored or some placeholder shows up.
- `counter`
    - Counters may be specified with two different functions: 'counter()' or 'counters()'. The former has two forms: 'counter(name)' or 'counter(name, style)'. The generated text is the value of the innermost counter of the given name in scope at this pseudo-element; it is formatted in the indicated style ('decimal' by default). The latter function also has two forms: 'counters(name, string)' or 'counters(name, string, style)'. The generated text is the value of all counters with the given name in scope at this pseudo-element, from outermost to innermost separated by the specified string. The counters are rendered in the indicated style ('decimal' by default). See the section on automatic counters and numbering for more information. The name must not be 'none', 'inherit' or 'initial'. Such a name causes the declaration to be ignored.
- attr(X)
    - Returns the value of the element's attribute X as a string. If there is no attribute X, an empty string is returned. The case-sensitivity of attribute names depends on the document language.
- open-quote | close-quote
    - These values are replaced by the appropriate string from the quotes property.
- no-open-quote | no-close-quote
    - Introduces no content, but increments (decrements) the level of nesting for quotes. 


For Example:

```

	/* Keywords that cannot be combined with other values */
	content: normal;
	content: none;

	/* string value, non-latin characters must be encoded */
	/* e.g. \00A0 for &nbsp; */
	content: 'prefix';

	/* uri value */
	content: url(http://www.example.com/test.html);

	/* counter values */
	content: chapter_counter;

	/* attr() value linked to the HTML attribute value */
	content: attr(value string);

	/* Language- and position-dependant keywords */
	content: open-quote;
	content: close-quote;
	content: no-open-quote;
	content: no-close-quote;

	/* Except for normal and none, several values */
	/* can be used simultaneously */
	content: open-quote chapter_counter;

	/* Global values */
	content: inherit;
	content: initial;
	content: unset;

	q {
	    color: #00008B;
	    font-style: italic;
	}

	q::before   { content: open-quote }
	q::after    { content: close-quote }

```


----
Go back to `CSS` [Table of Content](css.md)