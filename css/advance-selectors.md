## Advance Selectors

At this stage we have learned `CSS` **selectors** the based on  `id`, `class`, and `pseudo elements/classes`, but its not enough we can do much more and can have enormous level of flexibility.

### ` * `

- The star ( `*` ) symbol will target every single element on the page. Many developers will use this trick to zero out the `margins` and `padding`. While this is certainly fine for quick tests, I'd advise you to never use this in production code. It adds too much weight on the browser, and is unnecessary.

For Example:

```css
	* {
	 margin: 0;
	 padding: 0;
	}

```


### ` #<id-name> `

- Prefixing the hash ( `#` ) symbol to a selector allows us to target by id. This is easily the most common usage, however be cautious when using id selectors.

> Ask yourself: **do I absolutely need to apply an id to this element in order to target it**?

- `id` selectors are rigid and don't allow for reuse. If possible, first try to use a tag name, one of the new [<kbd>`HTML5`</kbd>](html/intro-to-html5.md) elements, or even a pseudo-class.

For Example:

```css
	#header {
	   width: 960px;
	   margin: auto;
	}

```

### ` .<class-name> `

- This is a `class` selector. The difference between `id`s and `class`es is that, with the latter, you can target multiple elements. Use `class`es when you want your styling to apply to a group of elements. Alternatively, use `id`s to find a needle-in-a-haystack, and style only that specific element.

For Example:

```css
	.header {
	   width: 960px;
	   margin: auto;
	}

```

### ` tag1<space>tag2 ` OR ` .<class-name><space>.<class-name> `

- The next most comment selector is the `descendant` selector. When you need to be more specific with your selectors, you use these. For example, what if, rather than targeting all anchor tags, you only need to target the anchors which are within an unordered list? This is specifically when you'd use a descendant selector. 

> If your selector looks like `ul li ul li a span.menu-text`, you're doing it wrong. Always ask yourself if it's absolutely necessary to apply all of that weight.


For Example:

```css
	ul li {
	   padding: 0px;
	   margin: 0px;
	}

	.header .nav {
		color: #f00000;
	}

```

### ` tag1 + tag2 ` OR ` .<class-name> + .<class-name> `

- This is referred to as an adjacent selector. It will select only the element that is immediately preceded by the former element. In this case, only the first paragraph after each ul will have red text.

For Example:

```css
	h2 + h3 {
		color: red;
	}

```

### ` tag1 > tag2 ` OR ` .<class-name> > .<class-name> `

- The difference between the standard `ul li` and `ul > li` is that the latter will only select direct children.


For Example:

```css
	ul > li {
  		border: 1px solid black;
	}
```

- A selector of `ul > li` will only target the `li`s which are direct children of the `ul`.

- For this reason, there are performance benefits in using the child combinator. In fact, it's recommended particularly when working with `JavaScript-based CSS` selector engines.


### ` tag1 ~ tag2 ` OR ` .<class-name> ~ .<class-name> `

- This sibling combinator is similar to `ul ~ p`, however, it's less strict. While an adjacent selector `ul + p` will only select the first element that is immediately preceded by the former selector, this one is more generalized. It will select, referring to our example above, any p elements, as long as they follow a ul. 

For Example:

```css
	ul ~ p {
   		color: red;
	}
```

### ` tag[title] `

- Referred to as an attributes selector, in our example above, this will only select the anchor tags that have a title attribute. Anchor tags which do not will not receive this particular styling.

```css
	a[title] {
	   color: green;
	}
```

### ` a[href="name"] `


> Note that we're wrapping the value in quotes. Remember to also do this when using a JavaScript CSS selector engine. When possible, always use CSS3 selectors over unofficial methods.


For Example:

```css
	a[href="http://stackoverflow.com"] {
	  color: #F48024;
	}
```

- The snippet above will style all anchor tags which link to `http://stackoverflow.com`. All other anchor tags will remain unaffected.


### ` a[href*="namestring"] `


For Example:

```css
	a[href*="stackoverflow"] {
	  color: #F48024;
	}
```

- There we go; that's what we need. The star ` * ` designates that the proceeding value must appear somewhere in the attribute's value. That way, this covers stackoverflow.com, www.stackoverflow.com, and even stackoverflow.com.

- Keep in mind that this is a broad statement. What if the anchor tag linked to some non-Envato site with the string tuts in the url? When you need to be more specific, use ^ and $, to reference the beginning and end of a string, respectively.


### ` a[href^="http"] `

- Ever wonder how some websites are able to display a little icon next to the links which are external? I'm sure you've seen these before; they're nice reminders that the link will direct you to an entirely different website.

> We're not searching for `http://` that's unnecessary, and doesn't account for the urls that begin with `https://`.


For Example:

```css
	a[href^="http"] {
	   background: url(path/to/external/icon.png) no-repeat;
	   padding-left: 10px;
	}
```

### ` a[href$=".jpg"] `

- Again, we use a regular expressions symbol ` $ ` to refer to the end of a string. In this case, we're searching for all anchors which link to an image -- or at least a url that ends with **.jpg**. Keep in mind that this certainly won't work for **gif**s and **png**s.

For Example:

```css
	a[href$=".jpg"] {
	   color: red;
	}
```

###  ` tag[data-*="name"] ` OR `class[data-*="name"] `

For Example:

````css	
	a[data-filetype="image"] {
	   color: red;
	}
	
	a[href$=".jpg"],
	a[href$=".jpeg"],
	a[href$=".png"],
	a[href$=".gif"] {
	   color: red;
	}
```

- Another possible solution is to use custom attributes. What if we added our own `data-filetype`attribute to each anchor that links to an image?

For Example:

```css	
	<a href="path/to/image.jpg" data-filetype="image"> Image Link </a>

	a[data-filetype="image"] {
	   color: red;
	}

```

### ` tag[foo~="bar"] ` OR ` class[foo~="bar"] `

```css

	a[data-info~="external"] {
	   color: red;
	}
	 
	a[data-info~="image"] {
	   border: 1px solid black;
	}
```

- Here's a special, as not too many people know about this trick. The tilda ` ~ `  symbol allows us to target an attribute which has a spaced-separated list of values.

- Going along with our custom attribute from number fifteen, above, we could create a data-info attribute, which can receive a space-separated list of anything we need to make note of. In this case, we'll make note of external links and links to images -- just for the example.

	
```css
	<a href="path/to/image.jpg" data-info="external image"> Click Me, Fool </a>

	
	/* Target data-info attr that contains the value "external" */
	a[data-info~="external"] {
	   color: red;
	}
 
	/* And which contain the value "image" */
	a[data-info~="image"] {
	  border: 1px solid black;
	}

```

----
Go back to `CSS` [Table of Content](css.md)