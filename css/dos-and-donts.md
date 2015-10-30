## `CSS` Do's and Don'ts

We all should follow what rules say, and whenever we try to cross lines we should keep that in mind that, how it will render on browser whether it mozilla, chrome, safari or world-famous and nightmare for developers Internet Explorer!


Lets have a look at what should we follow:

#### hold one's horses while declaring Universal Rules

- When we define something universally, always be very very careful, otherwise you will end up spoiling everything one day or another.

- Try making a specific rule instead of universal category!

#### Don't qualify `ID` rules with `tag` name or `class`

- If a rule has an `ID` selector as its key selector, don't add the tag name to the rule. Since `ID`s are unique, adding a tag name would slow down the matching process needlessly.

```css
	/* BAD */
    	button#backButton {…}
	/* BAD */
    	.menu-left#newMenuIcon {…}
	/* GOOD */
    	#backButton {…}
	/* GOOD */
    	#newMenuIcon {…} 

   /* very very BAD */
	<div id="block">
   		<div id="btn"></div>
   		<div id="btn"></div>
	</div>

	/* How we should do it: */

	<div id="block">
	   <div class="btn"></div>
	   <div class="btn"></div>
	</div>

```

#### Don't qualify `class` rules with `tag` names

- The previous concept also applies here. Though classes can be used many times on the same page, they are still more unique than a tag.

- One convention you can use is to include the tag name in the class name.  However, this may cost some flexibility; if design changes are made to the tag, the class names must be changed as well.

```css
	/* BAD */
    	treecell.indented {…}
	/* GOOD */
    	.treecell-indented {…}
	/* BEST */
    	.hierarchy-deep {…} 
```


#### NEVER use inline `CSS`

- Using `CSS` inline is really very BAD PRACTICE, always try to avoid it.
- It specially happen when we're debugging the code, and instead of editing stylesheet we go for the easier way and write it inline.


**Don't**

```html
	<div class="main-heading" style="margin-bottom:15px; color: #f9a933">Inline mode activated</div>
```

**what it should be**

```css
	.section-name .main-heading {
		margin-bottom:15px;
		color: #f9a933;
	}
```

#### Use the most specific category possible

- The single biggest cause of slowdown is too many rules in the tag category. By adding classes to our elements, we can further subdivide these rules into Class Categories, which eliminates time spent trying to match rules for a given tag.

```css
	/* BAD */
   	    treeitem[mailfolder="true"] > treerow > treecell {…}
	/* GOOD */
    	.treecell-mailfolder {…} 
```

#### Avoid the descendant selector

- The descendant selector is the most expensive selector in `CSS`. It is dreadfully expensive, especially if the selector is in the tag or Universal Category.

- Frequently, what is really desired is the child selector.  For instance, the performances are so bad, that descendant selectors are banned in Firefox' User Interface CSS, without a specific justification.

- Avoid using the child selector with tag category rules. This will dramatically lengthen the match time (especially if the rule is likely to be matched) for all occurrences of that element.

```css
/* BAD */
   	 treehead > treerow > treecell {…}
/* GOOD */
     .treecell-header {…} 
```