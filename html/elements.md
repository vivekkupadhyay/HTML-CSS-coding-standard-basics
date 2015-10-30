## Elements — (the basic building blocks)

`HTML` consists of a set of **elements**, which define the semantic meaning of their content. **Elements** include two matching **tags** and everything in between. 

For example:
- `<p>` **element** indicates a **paragraph**.
- `<img>` **element** indicates an **image**.

Some elements have very precise meaning, as:<br />

> `<img>` **this is an image**.<br /> 
> `<h1>`  **this is a heading**.<br />
> `<ol>`  **this is an ordered list**.


Most elements may contain other elements, forming a hierarchic structure. Such as:

```html
  <html>
    <body>
      <p> you are in your beginning stage of HTML</p>
    </body>
  </html>
```

As you can see, the `<html>` element surrounds the rest of the document and the `<body>` element surrounds the page content. This structure is often thought of as a tree with branches (in this case, the `<body>` and `<p>` elements) growing from the trunk (`<html>`). This hierarchical structure is called the **DOM** `(document object model)`.

----
Go back to `HTML` [Table of Content](html.md)