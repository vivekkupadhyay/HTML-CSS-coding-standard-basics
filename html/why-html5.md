## Why should we use HTML5

`HTML5` was **finalized**, and **published**, on **28 October 2014** by the `World Wide Web Consortium` (W3C). So if you're still not using it, then you should better :runner: because you're missing A Lot!!

Lets markdown some useful features of `HTML5` to start using it right now, OR right after you get done reading this:

1. Accessibility, `HTML5` makes creating accessible sites easier for two main reasons: 
    - Semantics
       - The new (some currently available) HTML headings like `<header>`, `<footer>`, `<nav>`, `<section>`, `<aside>`, etc. allow screen readers to easily access content.
    - ARIA 
       - It is a `World Wide Web Consortium` specification i.e. mainly used to assign specific **roles** to **elements** in an `HTML` **document**

2. Video and Audio Support
    - Lets just forget about Flash Player and other third party media players, make your videos and audio truly accessible with the new HTML5 <video> and <audio> tags.
	- As well said in **Naruto** *if there's friend there will be foe*, there exist number of **evil browsers** who does not or merely support `HTML5`.
	- But since we are coders, all we need to do is to add a little bit more code to get them working correctly.

	```	html
	<video poster="videopreview.jpg" controls>
	 <source src="videopreview.m4v" type="video/mp4" />
	 <source src="videopreview.ogg" type="video/ogg" />
	 <embed src="/to/my/video/player"></embed>
	</video>
	```

3. doctype
	- Aren't you guys tired of cutting and pasting some long unreadable line of code? 
	- Don't you want no more dirty head tags filled with doctype attributes?
	- Don't you want to simply and easily type it out and live happily forever?
	- If your answer is *yes* then you're good to go with `HTML5` as its **doctype** is like:

	```html
	<!DOCTYPE html>
	```

	> yes, that's it, and really great thing about it though, beyond the simplicity, is that it works in every browser clear back to the dreaded IE6.


4. Cleaner Code
   - If you are so keen about your **code** and always make sure that it is neat, elegant and clean,  easier to read, then `HTML5` is the best for you. 
   - `HTML5` allows you to write clear and descriptive code, semantic code that allows you to easily separate meaning from style and content. Consider this typical and simple header code with navigation:

	```html
	<header>
	 <h1>Header Text</h1>
	 <nav>
	  <ul>
	   <li><a href="#">Link</a></li>
	   <li><a href="#">Link</a></li>
	   <li><a href="#">Link</a></li>
	  </ul>
	 </nav>
	</header>
    ```

5. Game Development
	- In `HTML5` you can develop :video_game: using `<canvas>` tag. `HTML5` provides a great, mobile friendly way to develop fun, interactive games.

6. Legacy/Cross Browser Support
	- Fortunately all **modern & popular browsers** support `HTML5` (Chrome, Firefox, Safari, IE9+ and Opera) and the `HTML5` **doctype** was created so that all browsers, even the really old and annoying ones IE6 can use it.
	- But just because old browsers recognize the **doctype** that doesn’t mean they can use all the new `HTML5` tags and **goodies**.
	- Programmatically, `HTML5` is being built to make things easier and more cross browser friendly so in those older IE browsers that don’t like the new tags we can just simply add a Javascript shiv that will allow them to use the new elements:

	```html
	<!--[if lt IE 9]>
	 <script src="http://html5shiv.googlecode.com/svn/trunk/html5.js"></script>
	<![endif]-->
	```

6. Mobile
	- "This site must be mobile-friendly", nowadays every site-owner says that since Mobile devices are taking over the world. Every users will be using their mobile browsers to view your web site or application. 
	- `HTML5` is the most **mobile ready tool** for developing mobile sites and apps. 
	- With Adobe announcing `the death of mobile Flash`, you will now count on `HTML5` to do your mobile web application development.
    - And you what is the good news? **Mobile browsers** have fully adopted `HTML5`!
   


Apart from all the above features, we should start using `HTML5` today as: **it’s the future**. `HTML5` is not going anywhere and as more and more elements get adopted more and more companies will start to develop in `HTML5`. 

`HTML5` is essentially just `HTML`, don't be :fearful: it won't bite you. It’s not something you really need to figure out or relearn. So if you’re developing in `HTML` then you are already developing in `HTML5` so why not take full advantage of it. 


----
Go back to `HTML` [Table of Content](html.md)