## Comments and doctype

`HTML` has a mechanism for embedding **comments** that are not displayed when the page is rendered in a browser. This is useful for explaining a section of markup, leaving notes for other people who might work on the page<br />
viz quite useful for us too. 

- `HTML` **comments** are enclosed in symbols as follows:

```html
  <!-- This is comment text -->
```

Besides **tags**, text content, and entities, an `HTML` document must contain a **doctype** declaration as the first line.

- The **doctype** declaration is not an `HTML` tag, but rather tells the browser which version of `HTML` the page is written in.
- The doctype has a long and intricate history, but for now all you need to know is that this doctype tells 
the browser to interpret the HTML and CSS code according to W3C standards and not try to pretend that 
it is Internet Explorer from the 90s.
- In `HTML 4.01`, **doctype** referred to a **DTD** (Document Type Definition).

> There were three different doctype declarations in `HTML 4.01`:
   - strict
   - transitional
   - frameset

- strict (contained all HTML elements and attributes, but NOT presentational or deprecated elements)
   
   ```html
    <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
   ```
- transitional (contained all HTML elements and attributes, INCLUDING presentational and deprecated elements)
   
   ```html
    <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
   ```
- frameset.

  ```html
    <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Frameset//EN" "http://www.w3.org/TR/html4/frameset.dtd"> 
  ```

> In `HTML5`, there is only one declaration and is written like this:

```html
<!DOCTYPE html>
```

----
Go back to `HTML` [Table of Content](html.md)