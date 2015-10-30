## Getting Started with CSS Frameworks(aka FrontEnd Frameworks)

- A **framework** is a standardized set of concepts, practices and criteria for dealing with a common type of problem, which can be used as a reference to help us approach and resolve new problems of a similar nature.

- In the world of *web design*, to give a more straightforward definition, a framework is defined as a package made up of a structure of files and folders of standardized code (`HTML`, `CSS`, `JS` documents etc.) which can be used to support the development of websites, as a basis to start building a site.

- Most websites share a very similar (not to say identical) structure. The aim of frameworks is to provide a common structure so that developers don’t have to redo it from scratch and can reuse the code provided. In this way, frameworks allow us to cut out much of the work and save a lot of time.

> To summarize: **there’s no need to reinvent the wheel**.

> The aim of frameworks is to provide a common structure so that developers don’t have to redo it from scratch and can reuse the code provided


### Front-end Frameworks (or CSS Frameworks)

- Frontend frameworks usually consist of a package made up of a structure of files and folders of standardized code (`HTML`, `CSS`, `JS` documents etc.)

    - CSS source code to create a grid: this allows the developer to position the different elements that make up the site design in a simple and versatile fashion.
    - Typography style definitions for `HTML` elements.
    - Solutions for cases of browser incompatibility so the site displays correctly in all browsers.
    - Creation of standard `CSS` classes which can be used to style advanced components of the user interface

<div align="center"><img src="http://i.imgur.com/tTKzeru.png" align="center" alt="Responsive Design" title="Responsive Design" /></div>


Here we only discuss about *complete frontend frameworks* and by the word *complete* we mean,
	- with configurable features like *styled-typography*, *sets of forms*, *buttons*, *icons* and other reusable components built to provide *navigation*, *alerts*, *popovers*, and more, *images frames*, *HTML templates*, *custom settings*, etc.

And when we hear all this, the very first name that came into our mind is **Bootstrap**.

### Bootstrap

- Sleek, intuitive, and powerful front-end framework for faster and easier web development. Built at `Twitter` by `@mdo` and `@fat`, Bootstrap utilizes `LESS CSS`, is compiled via Node, and is managed through GitHub to help nerds do awesome stuff on the web.

- Its main features are:
	- Preprocessors
		- Bootstrap ships with vanilla CSS, but its source code utilizes the two most popular CSS preprocessors, Less and Sass. Quickly get started with precompiled CSS or build on the source.
	- One framework, every device.
		- Bootstrap easily and efficiently scales your websites and applications with a single code base, from phones to tablets to desktops with CSS media queries.
	- Full of features
		- With Bootstrap, you get extensive and beautiful documentation for common HTML elements, dozens of custom HTML and CSS components, and awesome jQuery plugins.

- [Getting Started with Bootstrap](http://getbootstrap.com/getting-started) is not a *Rocket Science* so don't be afraid of using it.


#### Basic template

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!-- The above 3 meta tags *must* come first in the head; any other head content must come *after* these tags -->
    <title>Bootstrap</title>

    <!-- Bootstrap -->
	<link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/css/bootstrap.min.css" rel="stylesheet" type="text/css" media="all" />

    <!-- HTML5 shim and Respond.js for IE8 support of HTML5 elements and media queries -->
    <!-- WARNING: Respond.js doesn't work if you view the page via file:// -->
    <!--[if lt IE 9]>
      <script src="https://oss.maxcdn.com/html5shiv/3.7.2/html5shiv.min.js"></script>
      <script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"></script>
    <![endif]-->
  </head>
  <body>
    <h1>Hello, world!</h1>

    <!-- jQuery (necessary for Bootstrap's JavaScript plugins) -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js" type="text/javascript"></script>
    <!-- Include all compiled plugins (below), or include individual files as needed -->
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.5/js/bootstrap.min.js" type="text/javascript"></script>
  </body>
</html>
```




----
Go back to `CSS` [Table of Content](css.md)