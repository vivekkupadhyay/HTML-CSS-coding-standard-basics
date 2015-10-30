## Transitions in CSS3 ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `transition` `CSS3` property is a shorthand property for `transition-property`, `transition-duration`, `transition-timing-function`, and `transition-delay`. 
- It enables you to define the transition between two states of an element. Different states may be defined using pseudo-classes like `:hover` or `:active` or dynamically set using `JavaScript`.


> Note that order is important within the items in this property: the first value that can be parsed as a time is assigned to the `transition-duration`, and the second value that can be parsed as a time is assigned to `transition-delay`.


For Example:

```css
	/* Apply to 1 property */
	/* property name | duration */
	transition: margin-left 4s;

	/* property name | duration | delay */
	transition: margin-left 4s 1s;

	/* property name | duration | timing function | delay */
	transition: margin-left 4s ease-in-out 1s;

	/* Apply to 2 properties */
	transition: margin-left 4s, color 1s;

	/* Apply to all changed properties */
	transition: all 0.5s ease-out;

	/* Global values */
	transition: inherit;
	transition: initial;
	transition: unset;
```


### `transition-delay` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `transition-delay` `CSS3` property specifies the amount of time to wait between a change being requested to a property that is to be transitioned and the start of the transition effect.

- A value of 0s, or 0ms, indicates that the property will begin to animate its transition immediately when the value changes; positive values will delay the start of the transition effect for the corresponding number of seconds. Negative values cause the transition to begin immediately, but to cause the transition to seem to begin partway through the animation effect.

- You may specify multiple delays; each delay will be applied to the corresponding property as specified by the transition-property property, which acts as a master list. If there are fewer delays specified than in the master list, missing values are set to the initial value (0s). If there are more delays, the list is simply truncated to the right size. In both case the CSS declaration stays valid.


#### Values

- `time`
	- It is a `time` denoting the amount of time to wait between a property's value changing and the start of the animation effect.


For Example:

```css
	/* time values */
	transition-delay: 3s;
	transition-delay: 2s, 4ms;

	/* Global values */
	transition-delay: inherit;
	transition-delay: initial;
	transition-delay: unset;

```

### `transition-duration` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `transition-duration` `CSS3` property specifies the number of seconds or milliseconds a transition animation should take to complete. By default, the value is 0s, meaning that no animation will occur.

- You may specify multiple durations; each duration will be applied to the corresponding property as specified by the transition-property property, which acts as a master list. If there are fewer durations specified than in the master list, the user agent repeat the list of durations. If there are more durations, the list is simply truncated to the right size. In both case the CSS declaration stays valid

#### Values

- `time`
	- It is a `time` denoting the amount of time the transition from the old value of a property to the new value should take. A time of 0s indicates that no transition will happen, that is the switch between the two states will be instantaneous. A negative value for the time renders the declaration invalid.

For Example:

```css
	/* time values */
	transition-duration: 6s;
	transition-duration: 120ms;
	transition-duration: 1s, 15s;
	transition-duration: 10s, 30s, 230ms;

	/* Global values */
	transition-duration: inherit;
	transition-duration: initial;
	transition-duration: unset;
```


### `transition-property` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `transition-property` `CSS3` property is used to specify the names of CSS properties to which a transition effect should be applied.


#### Values

- none
	- No properties will transition.
- all
	- All properties that can have an animated transition will do so.
- IDENT
	- A string identifying the property to which a transition effect should be applied when its value changes. This identifier is composed by case-insensitive letters a to z, numbers 0 to 9, an underscore (_) or a dash(-). The first non-dash character must be a letter (that is: no number at the beginning of it, even preceded by a dash). Also, two dashes are forbidden at the beginning of the identifier.

For Example:

```css
	/* Keyword values */
	transition-property: none;
	transition-property: all;
	transition-property: test_05;
	transition-property: -specific;
	transition-property: sliding-vertically;

	transition-property: test1;
	transition-property: test1, animation4;
	transition-property: all, height, all;
	transition-property: all, -moz-specific, sliding;

	/* Global values */
	transition-property: inherit;
	transition-property: initial;
	transition-property: unset;
```


### `transition-timing-function` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `transition-timing-function` `CSS3` property is used to describe how the intermediate values of the CSS properties being affected by a transition effect are calculated. This in essence lets you establish an acceleration curve, so that the speed of the transition can vary over its duration.

- This acceleration curve is defined using one `timing-function` for each property to be transitioned. 

- You may specify multiple timing functions; each one will be applied to the corresponding property as specified by the transition-property property, which acts as a master list. If there are fewer functions specified than in the master list, missing values are set to the initial value (ease). If there are more timing functions, the list is simply truncated to the right size. In both case the CSS declaration stays valid.


#### Values

- `timing-function`
   - Each `timing-function` represents the timing function to link to the corresponding property to transition, as defined in transition-property.


- The timing functions have the following definitions:

- `ease`
	- The ease function is equivalent to cubic-bezier(0.25, 0.1, 0.25, 1).
- `linear`
	- The linear function is equivalent to cubic-bezier(0, 0, 1, 1).
- `ease-in`
	- The ease-in function is equivalent to cubic-bezier(0.42, 0, 1, 1).
- `ease-out`
	- The ease-out function is equivalent to cubic-bezier(0, 0, 0.58, 1).
- `ease-in-out`
	- The ease-in-out function is equivalent to cubic-bezier(0.42, 0, 0.58, 1).
- `step-start`
	- The step-start function is equivalent to steps(1, start).
- `step-end`
	- The step-end function is equivalent to steps(1, end).
- `steps`
	- Specifies a stepping function, described above, taking two parameters. The first parameter specifies the number of intervals in the function. It must be a positive integer (greater than 0). The second parameter, which is optional, is either the value start or end, and specifies the point at which the change of values occur within the interval. If the second parameter is omitted, it is given the value end.
- `cubic-bezier`
	- Specifies a cubic-bezier curve. The four values specify points P1 and P2 of the curve as (x1, y1, x2, y2). Both x values must be in the range [0, 1] or the definition is invalid. The y values can exceed this range.


For Example:

```css
	/* Keyword values */
	transition-timing-function: ease;
	transition-timing-function: ease-in;
	transition-timing-function: ease-out;
	transition-timing-function: ease-in-out;
	transition-timing-function: linear;
	transition-timing-function: step-start;
	transition-timing-function: step-end;

	/* Function values */
	transition-timing-function: steps(4, end);
	transition-timing-function: cubic-bezier(0.1, 0.7, 1.0, 0.1);

	/* Multiple timing functions */
	transition-timing-function: ease, step-start, cubic-bezier(0.1, 0.7, 1.0, 0.1);

	/* Global values */
	transition-timing-function: inherit;
	transition-timing-function: initial;
	transition-timing-function: unset;
```

----
Go back to `CSS` [Table of Content](css.md)