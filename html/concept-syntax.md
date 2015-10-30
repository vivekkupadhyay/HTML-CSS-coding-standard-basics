## Concept & Syntax

An `HTML` document is a plain text **document** structured with **elements**, where an **element** is a part of a **web-page** 
that may contain a data item or a chunk of text or an image, or perhaps nothing. A typical **element** includes an 
**opening tag**, **attributes**, content, and a **closing tag**. **Elements** are surrounded by matching opening and closing **tags**. 
Each **tag** begins and ends with angle brackets `< >`. There are a few empty or **self-closing tags** that cannot enclose any text, for instance `<img>`. You can extend `HTML` **tags** with **attributes**, which provide additional information affecting how the browser interprets the element.

### Tags

`HTML` attaches special meaning to anything that starts with the less-than sign `<` and ends with the greater-than sign `>`. Such markup 
is called a **tag**. Make sure to close the **tag**, as some **tags** are closed by default, whereas others might produce unexpected errors 
if you forget the end **tag**. 

- `HTML` **tags** follow a simple but strict syntax:
    - Opening angle bracket `<`
    - **Tag** Name
    - **Attributes** (optional). First a space, then the **attribute** name, an equal sign `=`, and a **value** enclosed in double quotes `""`.
    - Closing angle bracket `>`

<div align="center"><img src="http://i.imgur.com/y8X4Luo.png" align="center" alt="HTML Tag Anatomy" /></div>
  


### Document-wide Tags

There exist three `**Document-wide Tags**:

1. `<html>`
   - The `<html>` **element** (or `HTML` root **element**) represents the root of an HTML **document** (since it is the first element of 
   any `HTML` **document**). All other **elements** must be descendants of this **element**.
   
2. `<head>`
   - The `<head>` **element** provides general information (metadata) about the **document**, including its `title` and `links` to or 
   definitions of `scripts` and `style sheets`.

3. `<body>`
   - The `<body>` **element** represents the content of an `HTML` **document**. There can be only one `<body>` **element** in a **document**.

### Text Formative Tags

In the end of the day `HTML` **document** is all about **content** i.e. text and each of them has different meaning, using `HTML` **tags** we can easily format it, give them **emphasization** as per their need.

For example:

> a heading should be bold enough to stand-out in a page like:

```
   <h2>Now you see me</h2>
```

Followings are some **text-formative tags**:

#### Heading Tags

- These **tags** are used for emphasizing headings in any `HTML` **document**.
- It ranges from `<h1>` to `<h6>`.
- `<h1>` defines the most important heading(should be main headings) followed by h2 headings, then the less important h3 i.e. `<h6>` defines the least important heading.
- Use `HTML` heading **tags** for headings only. Don't use headings to make text **BIG** or **bold**.
- Search engines use heading **tags** to index the structure and content of **web-pages**. 

For example:

```html
	<h1>I am heading 1</h1>
	<h2>I am heading 2</h2>
	<h3>I am heading 3</h3>
	<h4>I am heading 4</h4>
	<h5>I am heading 5</h5>
	<h6>I am heading 6</h6>
```

It will render on your browser as:


![Heading Tag Anatomy](http://i.imgur.com/aSPJbxL.jpg)


#### Paragraph Tags
- These **tags** are used to create **paragraphs**, which are usually separated by line breaks `<br />` OR `<br >`.
- We can use **Line Break Tags** to create separation as you can see below.

For example:

```
	<p>Mankind was born on Earth<br /> it was never meant to die here</p>
```

It will render on your browser as:


![Paragraph Tag Anatomy](http://i.imgur.com/2ER2D8t.jpg)


#### Pre-formatted Tag

- It defines pre-formatted text i.e.the text inside a `<pre>` element is displayed in a `fixed-width font` (usually **Courier**), and it preserves both spaces and line breaks.

For example:

```
	<pre>Do not go gentle into that good night,
		 Old age should burn and rave at close of day;
		 Rage, rage against the dying of the light.</pre>
```
It will render on your browser as:


![Pre Tag Anatomy](http://i.imgur.com/hihbyoU.png)


#### Bold/Strong and Italic/Emphasize Formatting
- On the **web-page** we easily use `<b>` OR `<strong>` **tag** to make text **Bold**.
- And for Italic/Emphasize formatting we use `<i>` or `<em>`

For example:

```
	<p>I am going normal to <strong>bold very easily</strong>.</p>
	<p>I am going normal to <i>italic very easily</i>.</p>
```
It will render on your browser as:


![Bold/Strong and Italic/Emphasize Anatomy](http://i.imgur.com/A8anrrL.jpg)


#### Some other formative Tags

For example:

```
	<p>I am a <small>Small</small> text.</p>
	<p>I am a <mark>Marked</mark> text</p>
	<p>My Android OS is <del>6.0</del> 5.1.</p>
	<p>He has scored <ins>5 goals</ins> in 9 minutes.</p>
	<p>I am a <sub>subscripted</sub> text.</p>
	<p>I am a <sup>superscripted</sup> text.</p>
```

It will render on your browser as:


![Some other formative Tags](http://i.imgur.com/Xu3P760.jpg)



### Lists/Tabular Formative Tags

To display text in a list form we use **Listing Tags** as:

#### Un-ordered Listing
- The `HTML` **unordered list element** `<ul>` represents an **unordered list** of items, namely a collection of items that do not have a numerical ordering, and their order in the list is meaningless.
- Each **unordered list** starts with the `<ul>` and consists list(s) which starts with the `<li>`.

For example:

```
  <ul>
	<li>HTML</li>
	<li>CSS</li>
	<li>Javascript</li>
	<li>jQuery</li>
  </ul> 
```

It will render on your browser as:


![Un-ordered Listing Anatomy](http://i.imgur.com/OSAmuz0.jpg)


#### Ordered Listing
- The `HTML` **ordered list element** `<ol>` represents an **ordered list** of items. Typically, ordered-list items are displayed with a preceding numbering, which can be of any form, like numerals, letters or Romans numerals or even simple bullets.
- Each **ordered list** starts with the `<ol>` and consists list(s) which starts with the `<li>`.

For example:

```
  <ol>
	<li>HTML</li>
	<li>CSS</li>
	<li>Javascript</li>
	<li>jQuery</li>
  </ol> 
```

It will render on your browser as:


![Ordered Listing Anatomy](http://i.imgur.com/KHf3gAj.jpg)


#### Tabular Tags

- To manage tabular structure we use `<table>` tag in `HTML`, it manages the content in a tabular form throughout the web-page.
- It has following anatomy:

```
	<table border="1" cellspacing="2" cellpadding="10">
		<thead>
			<tr>
				<th>Language</th>
				<th>Inventor</th>
				<th>Year</th>
			</tr>
		</thead>
		<tfoot>
			<tr>
				<td>Javascript</td>
				<td>Brendan Eich,</td>
				<td>1995</td>
			</tr>
		</tfoot> 
		<tbody>
			<tr>
				<td>HTML</td>
				<td>Tim Berners-Lee</td>
				<td>1993</td>
			</tr>
			<tr>
				<td>CSS</td>
				<td>Håkon Wium Lie </td>
				<td>1996</td>
			</tr>
		</tbody>
	</table>	
```

It will render on your browser as:


![Tabular Anatomy](http://i.imgur.com/GMnpnEZ.jpg)

Studying the above `code` we learn that:

- Every **table** starts with a `<table>` **tag**
- `<thead>` defines a set of `<tr>` defining the `<th>` of the `<table>`
- `<tr>` defines a **row** of cells in a `<table>`
- `<th>` defines a **cell** i.e. a **header** for a group of **cells** of a `<table>`
- `<td>` defines a **cells** of a `<table>` that contains data
- `<tbody>` defines one or more `<tr>` element `data-rows` to be the **body** of its parent `<table>`
- `<tfoot>` defines a set of `<tr>` summarizing the columns of the `<table>`.

> position of `<tfoot>` does not affect the layout OR structure of `<table>` on browser.


#### Links/Images Tags

- Nowadays every **web-page** has **links**(hyperlinks) and **images** and we can use them using following `HTML` **tags**:

##### Link Tag

- The `HTML` **Anchor Element** `<a>` defines a **hyperlink** to a location on the same page or any other page on the Web. It can also be used (in an obsolete way) to create an anchor point—a destination for hyperlinks within the content of a page, so that links aren't limited to connecting simply to the top of a page.

For example:

```
	<p>
		<a href="https://developer.mozilla.org">Shared knowledge for the Open Web Search</a>
    </p>
```

> Don't panic seeing `href=""`, it is an `attribute` of `<a>` and we will discuss about it further so be patience. 


It will render on your browser as:


![Shared knowledge for the Open Web Search](http://i.imgur.com/sshQSKD.jpg)


##### Image Tag

- The `HTML` **Image Element** `<img>` represents an image in the document.

For example:

```
    <img src="http://git.singsys.com/assets/logo-ca207549507c811d027110077cf86e90.svg" alt="Git Lab" />
```
will render as:

![Git Lab](http://git.singsys.com/assets/logo-ca207549507c811d027110077cf86e90.svg)


### Interactive HTML Tags

- To interact with the **web-page** we use these tags, it can be anything list of contries, asking for your email, submitting the form etc, some important **tags** are as follows:


#### input tag

- The `HTML` `<input>` element is used to create **interactive controls** for **web-based forms** in order to accept data from the user. How an `<input>` works varies considerably depending on the value of its type `attribute`.

- Behaviour of `<input>` tag is depend upon its `type=""` **attribute** as:

##### input type="text"

- A single-line text field

> Plesae not that **line-breaks** are automatically removed from the input value.

Syntax:

```
	<input type="text" name="FirstName" placeholder="FirstName" title="FirstName"  />
```

> Same as `type=""` , `name, placeholder and title` also are **attributes** of `<input>` and we will discuss about it further so be patience


##### input type="password"

- A single-line text field whose value is **obscured**.


Syntax:

```
	<input type="password" name="Password" title="password"  />
```

##### input type="radio"

- we must use the `value=""` **attribute** to define the **value** submitted by this item. 
- use the `checked` **attribute** to indicate whether this item is **selected by default**. 
- **only one radio button** in a group can be selected at a time.


Syntax:

```
	<input type="radio" name="yes" value="yes" checked /> Yes
	    <br>
	<input type="radio" name="no" value="no" /> No
```

##### input type="checkbox"

- we must use the `value=""` **attribute** to define the **value** submitted by this item. 
- use the `checked` **attribute** to indicate whether this item is **selected**. 


Syntax:

```
	<input type="checkbox" name="HTML" value="HTML" checked /> HTML
	   <br>
	<input type="checkbox" name="CSS" value="CSS" /> CSS
```

##### input type="file"

- `type="file"` **attribute** let user select a file.

Syntax:

```
	 <input type="file" name="fileUpload" title="fileUpload" />
```



#### select tag

- The `HTML` `<select>` **element** represents a control that presents a **menu of options**. 
- The options within the menu are represented by `<option>` **elements**, which can be grouped by `<optgroup>` **elements**. 
- An `<option>` can also be **pre-selected** for the user.


Syntax:

```
	<select name="Language">
		<option value="HTML">HTML</option>
		<option value="CSS">CSS</option>
		<option value="Javascript">Javascript</option>
		<option value="jQuery">jQuery</option>
	</select>
```

#### textarea tag

- The `HTML` `<textarea>` **element** represents a **multi-line plain-text** editing control.

Syntax:

```
	<textarea name="message" rows="10" cols="30">The cat was playing in the garden.</textarea>
```

#### button tag

- The `HTML` `<button>` **element** represents a **clickable** button.
- Behaviour of `<button>` tag is depend upon its `type=""` **attribute**.
- An `<input>` can be a **button** also using `type="buttton"` **attribute**

##### submit button

- `<input type="submit" />` OR `<button type="submit"></button>` used for submitting/posting all the entered values in **form-elements** to the server.

Syntax:

```
	<input type="submit" name="Submit" value="Submit" title="Submit" />
	<button type="submit" name="Submit" value="Submit" title="Submit">Submit</button>
```

> Please note that syntax of both `<input>` and `<button>` is slighlty diffrent. However they render same on the browser without any diffrence.


##### reset button

- `<input type="reset" />` OR `<button type="reset"></button>` used for resetting/clearing all the **form-elements** within a `<form>`.

Syntax:

```
	<input type="reset" name="reset" value="Reset" title="Reset" />
	<button type="reset" name="reset" value="Reset" title="Reset">Reset</button>
```

#### form tag

- The `HTML` `<form>` **element** represents a **document** section that contains **interactive controls** to submit information to a **web server**.
- these **interactive controls** are known as **form-elements** such as:
	- `<input>`
	- `<select>`
	- `<textarea>`
	- `<button>`
- a simple layout of a `<form>` can be as:

```
	<form>
            <div class="form-group">
                <label for="Name">Name</label>
                <input type="email" class="form-control" id="Name" placeholder="Name">
            </div>
            <div class="form-group">
                <label for="exampleInputEmail1">Email address</label>
                <input type="email" class="form-control" id="exampleInputEmail1" placeholder="Email">
            </div>
            <div class="form-group">
                <label for="exampleInputPassword1">Password</label>
                <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Password">
            </div>
            <div class="form-group">
                <label for="Name">Message</label>
                <textarea class="form-control" rows="3"></textarea>
            </div>
            <div class="form-group">
                <label for="exampleInputFile">File input</label>
                <input type="file" id="exampleInputFile">
            </div>
            <div class="form-group">
                <label class="checkbox-inline">
                    <input type="checkbox" id="inlineCheckbox1" value="option1">HTML</label>
                <label class="checkbox-inline">
                    <input type="checkbox" id="inlineCheckbox2" value="option2">CSS</label>
            </div>
            <div class="form-group">
                <label class="radio-inline">
                    <input type="radio" name="inlineRadioOptions" id="inlineRadio1" value="option1">Teacher</label>
                <label class="radio-inline">
                    <input type="radio" name="inlineRadioOptions" id="inlineRadio2" value="option2">Student</label>
            </div>
            <button type="submit" class="btn btn-default">Submit</button>
    </form>
```

A typical form will look like:

![Sample Form Anatomy](http://i.imgur.com/gd6Zvhn.jpg)


----
Go back to `HTML` [Table of Content](html.md)