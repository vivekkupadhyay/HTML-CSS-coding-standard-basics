## Types of Uses

When we create `CSS` declarations, we will need to decide where to place it. The type of stylesheet we create is characterized by the location we choose to place it.\

We can place our stylesheet in the document using these three ways:

### Internal/Embedded stylesheeet

- Internal stylesheeet are placed inside the `<head>` section of a particular web page via the style tag.
- These stylesheeet can be used only for the web page in which they are embedded. Therefore, you would need to create these styles over and over again for each web page you wish to style.
- Advanced Use of Internal stylesheeet unless you need to override an External stylesheeet. Internal stylesheeet are also called **Embedded** stylesheeet.

For example:

```html
	<!DOCTYPE html>
	<html>
	<head>
		<style type="text/css">
		   p { 
		   	text-decoration: underline; 
		   	color: orange; 
		   }
		   strong { 
		   	color: red 
		   }
		</style>
	</head>
	 <body>
		<p>
	  	 <strong>C</strong>ascading
	  	 <strong>S</strong>tyle
	  	 <strong>S</strong>heets
		</p>
	 </body>
	</html>

```

### Inline stylesheeet

- Inline stylesheeet cannot be resused at all. 
- Inline stylesheeet are placed directly inside an `HTML` element in the code.

> Inline stylesheeet do not have a **selector**. Why not? The reason is because an inline style is embedded directly inside the `HTML` element it styles. Therefore, there's no need for a selector. 

- Inline stylesheeet defeat the purpose of using `CSS` and negates most, if not all of `CSS`'s advantages, like the separation of content from presentation. Therefore, the use of Inline stylesheeet should be kept to **an absolute minimum**.

For example:

```css
	<p style="text-decoration: underline; color: orange; ">
		 <strong style="color: red">C</strong>ascading
		 <strong style="color: red">S</strong>tyle
		 <strong style="color: red">S</strong>heets
	</p>
```

### External stylesheet

- For the most part, we will want to place the majority of our stylesheet rules on an External stylesheet. 
- This will allow us to **reuse** the styles as many times as we would like simply by linking the External stylesheet to other web pages. 
- It also means we only have to create the stylesheet one time!

> An External stylesheet is a separate page (file) which is then linked to the web page. Therefore, the styles are External to, or outside of, the Web Page.

```html
	<!DOCTYPE html>
	<html>
		<head>
		  <link media="all" rel="stylesheet" type="text/css" href="path-to-file/filename.css" />
		</head>
	....
```
 where `filename.css` includes:

 ```css
	p { 
		text-decoration: underline; 
		color: orange; 
	}
	strong { 
		color: red 
	}
```

from all the above stylesheets we will get the same result:

![stylesheet result](http://i.imgur.com/CypoXXK.jpg)



----
Go back to `CSS` [Table of Content](css.md)