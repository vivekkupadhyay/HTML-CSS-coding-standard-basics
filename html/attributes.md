## Attributes

First of all thank you all for your patience as we have used few `HTML` **tags** along with thier **attributes** such as:

```html
  <img src="path/mylogo.png" alt="Xavier Foundations" />
```

So now its time: 

- An **attribute** is used to define the **characteristics** and sometimes **begaviour** of an `HTML` element and is placed inside the **element**'s opening tag `<`. 
- All **attributes** are made up of two parts:
	- a **name**
	- and a **value**

- The **name** is the property you want to set for that `HTML` tag. <br />In the above example, the **image** `<img>` element in the example carries an **attribute** whose name is `alt`, which you can use to indicate the **alternate text** OR **small description** of that `<img>`.

- The **value** is what you want the **value of the property** to be set and always put within **quotations** `" "`. <br />In case of above example **Xavier Foundations** is the value of `alt` **attribute**.

> **Attribute names** and **attribute values** are **case-insensitive**. 
> However, the `World Wide Web Consortium` (W3C) recommends **lowercase attributes/attribute values**.


### List of Attributes

- So the point is **elements** in `HTML` have **attributes**, and these are **additional values** that **configure** the **elements** or adjust their behavior in various ways to meet the criteria the users want.
- Here's a **table** of some **attributes**:



<table>
   <thead>
	 <tr>
		<th width="20%">Attribute Name</th>
		<th width="30%">Elements</th>
		<th width="50%">Description</th>
	 </tr>
   </thead>
   <tbody>
	 <tr>
		<td><code>manifest</code></td>
		<td><code>&lt;html&gt;</code></td>
		<td>Specifies the URL of the document's cache manifest.</td>
	 </tr>
	 <tr>
		<td><code>http-equiv</code></td>
		<td><code>&lt;meta&gt;</code></td>
		<td>Declares the character encoding of the page or script.</td>
	 </tr>
	 <tr>
		<td><code>content</code></td>
		<td><code>&lt;meta&gt;</code></td>
		<td>Declares the character encoding of the page or script.</td>
	 </tr>
	 <tr>
		<td><code>charset</code></td>
		<td><code>&lt;meta&gt;</code>, <code>&lt;script&gt;</code></td>
		<td>Declares the character encoding of the page or script.</td>
	 </tr>
	 <tr>
		<td><code>name</code></td>
		<td><code>&lt;meta&gt;</code>, <code>&lt;button&gt;</code>, <code>&lt;form&gt;</code>, <code>&lt;iframe&gt;</code>, <code>&lt;input&gt;</code>, <code>&lt;select&gt;</code>, <code>&lt;textarea&gt;</code></td>
		<td>Name of the element. For example used by the server to identify the fields in form submits.</td>
	 </tr>
	 <tr>
		<td><code>media</code></td>
		<td><code>&lt;a&gt;</code>, <code>&lt;area&gt;</code>, <code>&lt;link&gt;</code>, <code>&lt;source&gt;</code>, <code>&lt;style&gt;</code></td>
		<td>Specifies a hint of the media for which the linked resource was designed.</td>
	 </tr>
	 <tr>
		<td><code>form</code></td>
		<td><code>&lt;button&gt;</code>, <code>&lt;input&gt;</code>, <code>&lt;label&gt;</code>, <code>&lt;select&gt;</code>, <code>&lt;textarea&gt;</code></td>
		<td>Indicates the form that is the owner of the element.</td>
	 </tr>
	 <tr>
		<td><code>rel</code></td>
		<td><code>&lt;a&gt;</code>, <code>&lt;area&gt;</code></a>, <code>&lt;link&gt;</code></td>
		<td>Specifies the relationship of the target object to the link object.</td>
	 </tr>
	  <tr>
		<td><code>href</code></td>
		<td><code>&lt;a&gt;</code>, <code>&lt;area&gt;</code></a>, <code>&lt;base&gt;</code>, <code>&lt;link&gt;</code></td>
		<td>The URL of the embeddable content.</td>
	 </tr>
	  <tr>
		<td><code>hidden</code></td>
		<td>Also known as <code>Global Attribute</code></td>
		<td>Prevents rendering of given element, while keeping child elements, e.g. script elements, active.</td>
	 </tr>
	 <tr>
		<td><code>disabled</code></td>
		<td><code>&lt;button&gt;</code>, <code>&lt;input&gt;</code>, <code>&lt;label&gt;</code>, <code>&lt;select&gt;</code>, <code>&lt;textarea&gt;</code></td>
		<td>Indicates whether the user can interact with the element.</td>
	 </tr>
	  <tr>
		<td><code>src</code></td>
		<td><code>&lt;audio&gt;</code>, <code>&lt;embed&gt;</code></a>, <code>&lt;iframe&gt;</code>, <code>&lt;img&gt;</code>, <code>&lt;input&gt;</code>, <code>&lt;script&gt;</code>, <code>&lt;source&gt;</code>, <code>&lt;track&gt;</code>, <code>&lt;video&gt;</code></td>
		<td>The URL of the embeddable content.</td>
	 </tr>
	 <tr>
		<td><code>type</code></td>
		<td><code>&lt;button&gt;</code>, <code>&lt;input&gt;</code></a>, <code>&lt;embed&gt;</code>, <code>&lt;style&gt;</code>, <code>&lt;script&gt;</code>, <code>&lt;link&gt;</code></td>
		<td>Defines the type of the element.</td>
	 </tr>
	  <tr>
		<td><code>bgcolor</code></td>
		<td><code>&lt;body&gt;</code>, <code>&lt;table&gt;</code>, <code>&lt;tbody&gt;</code>, <code>&lt;tfoot&gt;</code>, <code>&lt;td&gt;</code>, <code>&lt;th&gt;</code>, <code>&lt;tr&gt;</code></td>
		<td>Background color of the element.</td>
	 </tr>
	  <tr>
		<td><code>accept</code></td>
		<td><code>&lt;form&gt;</code>, <code>&lt;input&gt;</code></td>
		<td>List of types the server accepts, typically a file type.</td>
	 </tr>
	 <tr>
		<td><code>multiple</code></td>
		<td><code>&lt;input&gt;</code>, <code>&lt;select&gt;</code></td>
		<td>Indicates whether multiple values can be entered in an input of the type email or file.</td>
	 </tr>
	 <tr>
		<td><code>data-*</code></td>
		<td>Also known as <code>Global Attribute</code></td>
		<td>Lets you attach custom attributes to an HTML element.</td>
	 </tr>
	 <tr>
		<td><code>action</code></td>
		<td><code>&lt;form&gt;</code></td>
		<td>The URI of a program that processes the information submitted via the form.</td>
	 </tr>
	 <tr>
		<td><code>align</code></td>
		<td><code>&lt;iframe&gt;</code>, <code>&lt;img&gt;</code>, <code>&lt;table&gt;</code>, <code>&lt;tbody&gt;</code>, <code>&lt;td&gt;</code>, <code>&lt;tfoot&gt;</code>, <code>&lt;th&gt;</code>, <code>&lt;thead&gt;</code>, <code>&lt;tr&gt;</code></td>
		<td>Specifies the horizontal alignment of the element.</td>
	 </tr>
	 <tr>
		<td><code>alt</code></td>
		<td><code>&lt;img&gt;</code>, <code>&lt;input&gt;</code></td>
		<td>Alternative text in case an image can't be displayed.</td>
	 </tr>
	 <tr>
		<td><code>border</code></td>
		<td><code>&lt;table&gt;</code>, <code>&lt;img&gt;</code></td>
		<td>The border width.</td>
	 </tr>
	 <tr>
		<td><code>checked</code></td>
		<td><code>&lt;input&gt;</code></td>
		<td>Indicates whether the element should be checked on page load.</td>
	 </tr>
	 <tr>
		<td><code>class</code></td>
		<td>Also known as <code>Global Attribute</code>. It is a space-separated list of the classes of the element. <code>class</code> allows <code>CSS</code> and <code>JavaScript</code> to **select** and <strong>access</strong> specific elements via the <code>class</code> <strong>selectors</strong>.</td>
		<td>Often used with <code>CSS</code> to style elements with common properties.</td>
	 </tr>
	 <tr>
		<td><code>id</code></td>
		<td>Also known as <code>Global Attribute</code>. It has only single value for any perticular element on any web-page. <code>class</code> allows <code>CSS</code> and <code>JavaScript</code> to **select** and <strong>access</strong> specific elements via the <code>class</code> <strong>selectors</strong>.</td>
		<td>Often used with <code>CSS</code> to style elements with common properties.</td>
	 </tr>
	 <tr>
		<td><code>title</code></td>
		<td>Also known as <code>Global Attribute<code>.</td>
		<td>Text to be displayed in a tooltip when hovering over the element.</td>
	 </tr>
	 <tr>
		<td><code>method</code></td>
		<td><code>form<code></td>
		<td>Defines which <code>HTTP</code> method to use when submitting the form. Can be GET (default) or POST.</td>
	 </tr>
	 <tr>
		<td><code>checked</code></td>
		<td><code>&lt;input&gt;</code></td>
		<td>Indicates whether the element should be checked on page load.</td>
	 </tr>
	  <tr>
		<td><code>value</code></td>
		<td><code>&lt;button&gt;</code>, <code>&lt;input&gt;</code>, <code>&lt;option&gt;</code></td>
		<td>Indicates whether the element should be checked on page load.</td>
	 </tr>
	 <tr>
		<td><code>selected</code></td>
		<td><code>&lt;option&gt;</code></td>
		<td>Defines a value which will be selected on page load.</td>
	 </tr>
	  <tr>
		<td><code>readonly</code></td>
		<td><code>&lt;input&gt;</code>, <code>&lt;textarea&gt;</code></td>
		<td>Indicates whether the element can be edited.</td>
	 </tr>
	  <tr>
		<td><code>rowspan</code></td>
		<td><code>&lt;td&gt;</code>, <code>&lt;th&gt;</code></td>
		<td>Defines the number of rows a table cell should span over.</td>
	 </tr>
	  <tr>
		<td><code>colspan</code></td>
		<td><code>&lt;td&gt;</code>, <code>&lt;th&gt;</code></td>
		<td>The colspan attribute defines the number of columns a cell should span.</td>
	 </tr>
	  <tr>
		<td><code>required</code></td>
		<td><code>&lt;input&gt;</code>, <code>&lt;select&gt;</code>, <code>&lt;textarea&gt;</code></td>
		<td>Indicates whether this element is required to fill out or not.</td>
	 </tr>
   </tbody>
</table>


----
Go back to `HTML` [Table of Content](html.md)