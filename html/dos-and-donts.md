## `HTML` Do's and Don'ts

There's no such thing as `WYSIWYG` (What You See Is What You Get) in `HTML`. Every browser interprets `HTML` in a slightly different or outdated fashion. Many users of `HTML` assistants or editors are stunned when they find out their web pages appear different or even garbled when viewed by a different browser.

But we should follow what rules say, and whenever we try to cross lines we should keep that in mind that, how it will render on browser whether it mozilla, chrome, safari or world-famous and nightmare for developers Internet Explorer!


Lets have a look at what should we follow:

#### Always Declare a `doctype`

- The `doctype` declaration should be the first thing in our HTML documents.

- The `doctype` goes before the opening `HTML` tag at the top of the page and tells the browser whether the page contains `HTML`, `XHTML`, or a mix of both, so that it can correctly interpret the markup.

**Don't**

```
<html>
  <head> ... </head>
  <body> ... </body>
</html>
```

> Also don't use legacy or obsolete `doctype` OR `XML Declaration`

**Don't**

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">

OR

<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<!DOCTYPE html>
```

**what it should be**

```
<!DOCTYPE html>
<html>
  <head> ... </head>
  <body> ... </body>
</html>
```

#### Always Declare a `title` and use it A LOT

- The `title` tag helps make a web page more meaningful and *search-engine* friendly. For example, the text inside the `title` tag appears in `Google`’s search engine results page, as well as in the user’s web browser bar and tabs.

- Not only just `<title>` but as an **attribute** it is more effective, use it a lot and almost everywhere viz highly recommended by `W3C` our `SEO` guys.


**what it should be**

```
<!DOCTYPE html>
<html>
  <head>
  	<title>Duck Duck Go</title>	
  </head>
  <body> ... </body>
</html>
```
```
	<a href="" title="Home Page">Home</a>

	<h1><a href="" title="Company Name">Company Name</a></h1>

	<img src="path-to-file/imgname.jpg" title="Image Name" alt="Image Name" />
```

> Same goes for `alt` attribute as shown in the example below, as it has same reputations `title`.


#### NEVER use inline `CSS`

- Using `CSS` inline is really very BAD PRACTICE, always try to avoid it.
- It specially happen when we're debugging the code, and instead of editing stylesheet we go for the easier way and write it inline.


**Don't**

```html
	<div class="main-heading" style="margin-bottom:15px; color: #f9a933">Inline mode activated</div>
```

**what it should be**

```html
	.section-name .main-heading {
		margin-bottom:15px;
		color: #f9a933;
	}
```

#### Always link all your `CSS` within `head` tag

-  Actually we can place our stylesheets anywhere. However its recommended that it should be placed within the document `head` tag. 

> The primary benefit is that your pages will seemingly load faster.

**what it should be**

```html
<!DOCTYPE html>
<html>
  <head>
  	<title>Duck Duck Go</title>	
  	<!-- Bootstrap CSS -->
	<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css" media="all" type="text/css" />
  </head>
  <body> ... </body>
</html>
```


#### Always link all your `javascript` at the bottom

-  Its as same as `CSS`, and to successfully load our webpage faster, we should place them at the bottom(in the end of the document).

- When browser loading a script, it can't continue on until the entire file has been loaded. Thus, the user will have to wait longer before noticing any progress.

> If we have JS files whose only purpose is to add functionality -- for example, after a button is clicked -- go ahead and place those files at the bottom, just before the closing body tag. This is absolutely a best practice.


**what it should be**

```html
<!DOCTYPE html>
<html>
  <head>
  	<title>Duck Duck Go</title>	
  	<!-- Bootstrap CSS -->
	<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css" media="all" type="text/css" />
  </head>
  <body>

  	<!-- jQuery Library --> 
	<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js" type="text/javascript"></script> 
	<!-- Bootstrap jQuery/JS Library --> 
	<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js" type="text/javascript"></script>
  </body>
</html>
```

#### Use code commenting and white spaces around it

- Code commenting is MUST, we should strictly follow it.
- While sectioning our `HTML` we should comment it, its not only help you but other who will or might be working on your code in future.



**Don't**

```html

	<!--site wrapper-->
    <div class="site-wrapper"> 
		<!--header section-->
		<header class="header-wrapper">
		...
```

**what it should be**

```html
	<!-- site wrapper -->
    <div class="site-wrapper"> 
		<!-- header section -->
		<header class="header-wrapper">
		...
```

#### Never forget to close tags

- Closing your tag is MUST, nowadays if you forget to close or tags OR you can misplaced them our *modern browsers* will neglect it and render in correctly on the browser.

**what it should be**

```html
	<nav>
		<ul>
			<li><a href="" title="">test</a></li>
			<li><a href="" title="">test</a></li>
		</ul>
	</nav>
```

#### Carefully use heading tags `<h1>` - `<h6>`

- Every heading tag has its special meaning for the browser, for the search engine and for the www.
- Don't just use them for **bold**, we have `<strong>` for that.

> The six heading elements, `H1` through `H6`, denote section headings. Although the order and occurrence of headings is not constrained by the HTML DTD, documents should not skip levels (for example, from `H1` to `H3`), as converting such documents to other representations is often problematic. `W3C`

```html
<h1>This is the topmost heading</h1>
<h2>This is a sub-heading underneath the topmost heading.</h2>
<h3>This is a sub-heading underneath the h2 heading.</h3>
```

#### Use tags effectively

- Always use what is necessary or effective:

For example:

- for *ordered list* we MUST use `<ol>` not `<ul>` not `<div>` or any other tag and vice-versa for *un-ordered*
- for navigation we MUST use `<ul>` and for good practice(best in case):

```html
	<nav>
		<ul>
			<li><a href="" title="">test</a></li>
			<li><a href="" title="">test</a></li>
		</ul>
	</nav>
```

#### MUST Minify and Unify CSS

- A simple website usually has one main `CSS` file and possibly a few more for things like `reset-css` and `browser-specific` fixes.

> Dont worry about these if you're using *Bootstrap*.

- By minifying (take out unneeded characters such as spaces, newlines, and tabs) all your code and try to unify files that can be combined into one file, we can improve load time for our website.

- A problem with this approach is that you have to "unminify" (because it’s hard to read unformatted code) and then redo the minification process every time you need to update your code. So it’s better to do this *at the end of your production cycle*.

> Online tools to minify and optimize `CSS` can be found on this list of CSS optimizers.

1. [CSSOptimiser](http://cssoptimiser.com)
2. [CleanCSS](http://www.danstools.com/?lang=en)
3. [CSSCompressor](http://www.cssdrive.com/index.php/main/csscompressor)
4. [CSSOptimiser-mabblog](http://mabblog.com/cssoptimizer/compress.html)
5. [FlumpCakes](http://flumpcakes.co.uk/css/optimiser)


#### Minify, Unify and Move Down JavaScript

- Like `CSS` try to minify and unify your JavaScript libraries to reduce the number of HTTP requests that need to be made in order to generate one of your web pages.

- But unlike `CSS`, there is one really bad thing about external JavaScript files: browsers do not allow parallel downloads, which means the browser cannot download anything while it’s downloading JavaScript, resulting in making the page feel like it’s loading slowly.


#### Avoid `div` use `section` and `main`

- Instead of unnecessary `div` we should opt for `header`, `footer` and `section` viz not only a good practice but alos highly recommended.


**Don't**

```html
	<!--site wrapper-->
    <div class="site-wrapper"> 
		<!--header section-->
		<div class="header-wrapper">
		...
```

**what it should be**

```html
	<!-- site wrapper -->
    <main> 
		<!-- header section -->
		<header class="header-wrapper">
		...

	OR
	
	<section class="services-section">
		...	
```

#### Avoid unnecessary `CSS` use `HTML` tags

- Instead of writing unnecessary `CSS` we should use `i`, `u`, `b` OR `strong` etc tags.

#### User `br` but effectively 

- Try to avoid using `br`, and specially when it's used for UI purpose.


**Don't**

```html
<p><label>Rule name: <input name="rule-name" type="text"></label><br>
<label>Rule description:<br>
<textarea name="rule-description"></textarea></label></p>
```

**what it should be**

```html
<p><label>Rule name: <input name="rule-name" type="text"></label></p>
<p><label>Rule description:<br>
<textarea name="rule-description"></textarea></label></p>
```

> Also as you can see, `label` is being used for form-controls.


#### Always write your `table` correctly

- We should always write our `table` correctly instead as:

**Don't**

```html
	<table>
	    <tr>
	      <th><strong>Element</strong></th>
	      <th><strong>Empty</strong></th>
	      <th><strong>Tag omission</strong></th>
	    </tr>
	    <tr>
	      <td><strong><code>pre</code></strong></td>
	      <td>No</td>
	      <td>Neither tag is omissible</td>
	    </tr>
	    <tr>
	      <td><strong><code>img</code></strong></td>
	      <td>Yes</td>
	      <td>No end tag</td>
	    </tr>
	</table>
```

**what it should be**

```html
	<table>
	  <thead>
	    <tr>
	      <th>Element</th>
	      <th>Empty</th>
	      <th>Tag omission</th>
	    </tr>
	  </thead>
	  <tbody>
	    <tr>
	      <th><code>pre</code></th>
	      <td>No</td>
	      <td>Neither tag is omissible</td>
	    </tr>
	    <tr>
	      <th><code>img</code></th>
	      <td>Yes</td>
	      <td>No end tag</td>
	    </tr>
	  </tbody>
	</table>
```

#### Always indent your code consistently

- Beautified code is always recommended, formatting or beautifying the code is something we all should follow.
- But unnecessary indenting is avoided.
- A cleanly written and well-indented code base shows your professionalism, as well as your consideration for the other people that might need to work on your code.
- Write properly indented clean markup from the start; it will increase your work’s readability.


**what it should be**

```html
<!DOCTYPE html>
  <html lang="en">
    <head>
        <meta charset="utf-8" />
        <meta http-equiv="X-UA-Compatible" content="IE=edge" />
        <meta name="viewport" content="width=device-width, initial-scale=1" />
        <title>Site Title</title>
        
		<!-- Bootstrap CSS -->
	    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css" media="all" type="text/css" />
    </head>

    <body>
    
    <!-- site wrapper -->
    <main class="site-wrapper"> 
		<!-- header section -->
		<header class="header-wrapper">
		</header>
		
		<!-- middle section -->
		<section class="middle-section">
			
		</section>
					
		<!-- footer section -->
		<footer class="footer-section">
			
	   </footer>	   
    </main>

    <!-- jQuery Library --> 
	<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js" type="text/javascript"></script> 
	<!-- Bootstrap jQuery/JS Library --> 
	<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js" type="text/javascript"></script>

    </body>
    
  </html>

```

#### Used cdn/maxcdn

- `CDN`/`MaxCDN` is one of the largest **Content Delivery Network** provider. They accelerate your site and decrease the server load. 

Following are main reasons why should we use them:

1. Speed
	- Once we started using a CDN on our site, the site got faster.

2. Crash Resistance
	- CDN allows us to distribute the load to multiple servers instead of having 100% traffic to our main server thus making it less likely to crash.

3. Improved User Experience 
	– Since we started using a CDN, we have noticed a decline in bounce rate on our site. Furthermore, we have also seen increased in pageviews and numbers of pages viewed by each user. So clearly a fast site means improved user experience.

4. Improvement in SEO 
	– Google has clearly stated that faster sites tend to rank higher in Search Engines. We have noticed our site ranking higher once we did the optimization on our site.


#### Validate Your Code

- While writing HTML, make a habit to validate frequently; this will save you from issues that are harder to pinpoint (or redo) once your work is completed and lengthier.

- [The `World Wide Web Consortium`(W3C) HTML Validation Service](https://validator.w3.org/)
    - We recommend putting the document type declaration (link is external) (identifying the version of HTML you are writing) in your web pages.
    - If any errors are found in your HTML document, they will be listed by line number with a link to an explanation of the error. Understanding this report can be difficult at times, but stick with it.
