Hopefully, you have studied or currently studying [**`HTML`**](html), and one thing that keep bothering you is that:

> how to manage texts on the page so that they can have diffrent `font-size` or `color` ?

Practically, a **web-page** consists of three layers: 
1. Content Layer - [**`HTML`**](html)
2. Presentation Layer - [**`CSS`**](css)
    - It defines how the content will appear to a **user** who accesses the **web-page**. 
3. Behavior Layer - [**`javascript`**](javascript)

Now the question is: 
### What is CSS?
[**`CSS`**](css) (Cascading StyleSheets) is a *declarative language* that controls how **web-pages** will behave in the browser.

 - The browser applies [**`CSS`**](css) style declarations to selected elements to display them properly. 
 - A style declaration contains the properties, with their values, that determine how a **web-page** behaves.
 - A [**`CSS`**](css) rule is a set of properties associated with a `selector`.
 
 
Here is a little example that makes every `HTML` paragraph **white** against a **black background**:

```css
    /* The selector "p" indicate that all paragraphs in the document will be affected by that rule */
    p {
        /* The "color" property defines the text color, in this case yellow. */
        color: white; 
        
        /* The "background-color" property defines the background color, in this case black. */
        background-color: black
    }
```

and here's how it will render on browser:

![Paragraph styling](http://i.imgur.com/AKvA4fZ.jpg)



----
Go back to `CSS` [Table of Content](css.md)