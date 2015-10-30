## Using HTML5 Elements in Non-HTML5 Browsers

Practically `<sections>` and `<header>` elements should work in most *non-HTML5 browsers*. Though unsupported, they don't need a special *DOM interface* and they only need a specific `CSS` styling as unknown elements are styled as `display:inline` by default:

```css
section, article, aside, footer, header, nav, hgroup {
  display:block;
}
```

Of course the web developer can style them differently, but keep in mind that in a non-HTML5 browser, the default styling is different from what is expected for such elements. Also note that the `<time>` element has not been included, because the default styling for it in a non-HTML5 browser is the same as the one in an HTML5-compatible one.

This method has its limitation though, as some browsers do not allow styling of unsupported elements. That is the case of the Internet Explorer (version 8 and earlier), which need a specific script to allow this:

```html
<!--[if lt IE 9]>
  <script>
    document.createElement("header" );
    document.createElement("footer" );
    document.createElement("section"); 
    document.createElement("aside"  );
    document.createElement("nav"    );
    document.createElement("article"); 
    document.createElement("hgroup" ); 
    document.createElement("time"   );
  </script>
<![endif]-->
```

This *script* means that, in the case of Internet Explorer (8 and earlier), **scripting should be enabled in order to display HTML5** sectioning and headings elements properly. If not, they won't be displayed, which may be problematic as these elements are likely defining the structure of the whole page. That's why an explicit `<noscript>` element should be added for this case:

```html
<noscript>
   <strong>Warning !</strong>
   Because your browser does not support HTML5, some elements are simulated using JScript.
   Unfortunately your browser has disabled scripting. Please enable it in order to display this page.
</noscript>
```

This leads to the following code to allow the support of the `HTML5 <sections>` and `<header>` elements in non-HTML5 browsers, even for Internet Explorer (8 and older), with a proper fallback for the case where this latter browser is configured not to use scripting:

```html
<!--[if lt IE 9]>
  <script>
    document.createElement("header" );
    document.createElement("footer" );
    document.createElement("section"); 
    document.createElement("aside"  );
    document.createElement("nav"    );
    document.createElement("article"); 
    document.createElement("hgroup" ); 
    document.createElement("time"   );
  </script>
  <noscript>
     <strong>Warning !</strong>
     Because your browser does not support HTML5, some elements are created using JavaScript.
     Unfortunately your browser has disabled scripting. Please enable it in order to display this page.
  </noscript>
<![endif]-->
```


----
Go back to `HTML` [Table of Content](html.md)