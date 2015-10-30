## Markup
It is an act of inserting additional text into a document viz not usually visible to the reader, and is not part of the content, but enhances the document in some way, such as capturing document 
structure or adding hypertext capability. And for this it uses the additional text, also known as **tags**.

> A set of **tag**s designed for the **processing**, **definition** and **presentation** of text, assigned to elements of a text to indicate their relation to the rest of the text or dictate how they should be displayed.

### HTML Markup
 **HTML** tags are used to markup the structure of a document, and embed basic formatting information so that the browser can use to decide how to display the document. 
 
 > **HTML** has two types of markup: **tags** and **character entities**. 

- **Tags** are constructed of brackets between which the tag is placed.

```html
   <h1> The closer you look, the less you'll see </h1>
```
- **Character Entities** are used to include international characters as well as characters usually included in tags as markup. Entities start with an ampersand(&), followed by the entity name and end with a semicolon(;).

```html
    &amp;
```

### Components/Elements Markup
The very basic markup of an element/component is as:

```html
   <img src="now-you-see-me.jpg" alt="Now You See Me" />
```   


- `<img>` is Image tag (**tags** are also referred as **elements**).
- `src` and `alt` are attributes of the Image tag.
- **="Now You See Me"** is a value being assigned to the attribute.
- `/>` closes OR ends the Image tag.

**Tags** can have **elements**, which are only allowed between them.

> If you inspect your current webpage you can probably check that all the `HTML` **tags** are between `<html>` ... `</html>`.


----
Go back to `HTML` [Table of Content](html.md)