## Animations in CSS3  ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `animation` `CSS3` property is a shorthand property for `animation-name`, `animation-duration`, `animation-timing-function`, `animation-delay`, `animation-iteration-count`, `animation-direction`, `animation-fill-mode` and `animation-play-state`.

- A description of which properties are animatable is available; it's worth noting that this description is also valid for `CSS3` transitions.


For Example:

```css
/* @keyframes name | duration | timing-function | delay | 
   iteration-count | direction | fill-mode | play-state */
  animation: slidein 3s ease-in 1s 2 reverse both paused;

/* @keyframes name | duration | timing-function | delay */
  animation: slidein 3s linear 1s;

/* @keyframes name | duration */
  animation: slidein 3s;

```

### `animation-delay` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `animation-delay` `CSS3` property specifies when the animation should start. This lets the animation sequence begin some time after it's applied to an element.

- A value of 0s, which is the default value of the property, indicates that the animation should begin as soon as it's applied. Otherwise, the value specifies an offset from the moment the animation is applied to the element; animation will begin that amount of time after being applied.

- Specifying a negative value for the animation delay causes the animation to begin executing immediately. However, it will appear to have begun executing partway through its cycle. For example, if you specify -1s as the animation delay time, the animation will begin immediately but will start 1 second into the animation sequence.

- If you specify a negative value for the animation delay, but the starting value is implicit, the starting value is taken from the moment the animation is applied to the element.

- It is often convenient to use the shorthand property animation to set all animation properties at once.


For Example:

```css
	animation-delay: 3s;
	animation-delay: 2s, 4ms;
```

### `animation-direction` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `animation-direction` `CSS3` property indicates whether the animation should play in reverse on alternate cycles.

- It is often convenient to use the shorthand property animation to set all animation properties at once.

#### Values

- `normal`
    - The animation should play forward each cycle. In other words, each time the animation cycles, the animation will reset to the beginning state and start over again. This is the default animation direction setting.
- `reverse`
    - The animation plays backward each cycle. Each time the animation cycles, the animation resets to the end state and start over again.
- `alternate`
    - The animation should reverse direction each cycle. When playing in reverse, the animation steps are performed backward. In addition, timing functions are also reversed; for example, an ease-in animation is replaced with an ease-out animation when played in reverse. The count to determine if it is an even or an odd iteration starts at one.
- `alternate-reverse`
    - The animation plays backward on the first play-through, then forward on the next, then continues to alternate. The count to determinate if it is an even or an odd iteration starts at one. 

For Example:

```css
	animation-direction: normal;
	animation-direction: reverse;
	animation-direction: alternate;
	animation-direction: alternate-reverse;
	animation-direction: normal, reverse;
	animation-direction: alternate, reverse, normal;
```

### `animation-duration` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `animation-duration` `CSS3` property specifies the length of time that an animation should take to complete one cycle.

- A value of 0s, which is the default value, indicates that no animation should occur.

- It is often convenient to use the shorthand property animation to set all animation properties at once.

For Example:

```css
	animation-duration: 6s;
	animation-duration: 120ms;
	animation-duration: 1s, 15s;
	animation-duration: 10s, 30s, 230ms;
```

### `animation-fill-mode`  ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `animation-fill-mode` `CSS3` property specifies how a CSS animation should apply styles to its target before and after it is executing.


#### Values

- `none`
    - The animation will not apply any styles to the target before or after it is executing.
- `forwards`
    - The target will retain the computed values set by the last `keyframe` encountered during execution. The last keyframe encountered depends on the value of `animation-direction` and `animation-iteration-count`: 

<table>
  <thead>
   <tr>
    <th scope="col"><code>animation-direction</code></th>
    <th scope="col"><code>animation-iteration-count</code></th>
    <th scope="col">last keyframe encountered</th>
   </tr>
  </thead>
  <tbody>
   <tr>
    <td><code>normal</code></td>
    <td>even or odd</td>
    <td><code>100%</code> or <code>to</code></td>
   </tr>
   <tr>
    <td><code>reverse</code></td>
    <td>even or odd</td>
    <td><code>0%</code> or <code>from</code></td>
   </tr>
   <tr>
    <td><code>alternate</code></td>
    <td>even</td>
    <td><code>0%</code> or <code>from</code></td>
   </tr>
   <tr>
    <td><code>alternate</code></td>
    <td>odd</td>
    <td><code>100%</code> or <code>to</code></td>
   </tr>
   <tr>
    <td><code>alternate-reverse</code></td>
    <td>even</td>
    <td><code>100%</code> or <code>to</code></td>
   </tr>
   <tr>
    <td><code>alternate-reverse</code></td>
    <td>odd</td>
    <td><code>0%</code> or <code>from</code></td>
   </tr>
  </tbody>
 </table>


- `backwards`
    - The animation will apply the values defined in the first relevant keyframe as soon as it is applied to the target, and retain this during the `animation-delay` period. The first relevant keyframe depends of the value of `animation-direction`:

<table >
  <thead>
   <tr>
    <th scope="col"><code>animation-direction</code></th>
    <th scope="col">first relevant keyframe</th>
   </tr>
  </thead>
  <tbody>
   <tr>
    <td><code>normal</code> or <code>alternate</code></td>
    <td><code>0%</code> or <code>from</code></td>
   </tr>
   <tr>
    <td><code>reverse</code> or <code>alternate-reverse</code></td>
    <td><code>100%</code> or <code>to</code></td>
   </tr>
  </tbody>
 </table>


- `both`
   - The animation will follow the rules for both forwards and backwards, thus extending the animation properties in both directions.


For Example:

```csscss
animation-fill-mode: none;
animation-fill-mode: forwards;
animation-fill-mode: backwards;
animation-fill-mode: both;

/* Several values may be given, separated by commas. */
/* Each applies for each animation in animation-name. */
animation-fill-mode: none, backwards;
animation-fill-mode: both, forwards, none;
```

Try this at your end and observer how it renders in your browser:

> You can see the effect of animation-fill-mode in the following example. For animations that run for an infinite time, you might want them to end on the last state rather than the first.

```csscss
<p>Move your mouse over the grey box</p>
<div class="demo">
  <div class="grows">This just grows</div>
  <div class="growsandstays">This grows and stays big</div>
</div>

.demo {
  border-top: 100px solid #ccc;
  height: 300px;
  font-family: sans-serif;
}
@keyframes grow {
    0% { font-size: 0 }
    100% { font-size: 40px }
}
@-webkit-keyframes grow {
    0% { font-size: 0 }
    100% { font-size: 40px }
}
.demo:hover .grows {
    animation-name: grow;
    animation-duration: 3s;
    -webkit-animation-name: grow;
    -webkit-animation-duration: 3s;
}
.demo:hover .growsandstays {
    animation-name: grow;
    animation-duration: 3s;
    animation-fill-mode: forwards;
    -webkit-animation-name: grow;
    -webkit-animation-duration: 3s;
    -webkit-animation-fill-mode: forwards;
}
```

### `animation-iteration-count`  ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `animation-iteration-count` `CSS3` property defines the number of times an `animation` cycle should be played before stopping.

- It is often convenient to use the shorthand property animation to set all animation properties at once.

#### Values

- `infinite`
    = The animation will repeat forever.
- `number`
    = The number of times the animation should repeat; this is 1 by default. Negative values are invalid. You may specify non-integer values to play part of an animation cycle (for example 0.5 will play half of the animation cycle). 


For Example:

```css
	animation-iteration-count: infinite;
	animation-iteration-count: 3;
	animation-iteration-count: 2.3;
	animation-iteration-count: 2, 0, infinite;
```

### `animation-name`  ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `animation-name` `CSS3` property specifies a list of animations that should be applied to the selected element. Each name indicates a @keyframes at-rule that defines the property values for the animation sequence.

- It is often convenient to use the shorthand property animation to set all animation properties at once.


For Example:

```css
	animation-name: none;
	animation-name: test_05;
	animation-name: -specific;
	animation-name: sliding-vertically;

	animation-name: test1;
	animation-name: test1, animation4;
	animation-name: none, -moz-specific, sliding;

	animation-name: initial
	animation-name: inherit
	animation-name: unset
```

### `animation-play-state`  ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `animation-play-state` `CSS3` property determines whether an animation is running or paused. This can be queried to determine whether or not the animation is currently running. In addition, its value can be set to pause and resume playback of an animation.

- Resuming a paused animation will start the animation from where it left off at the time it was paused, rather than starting over from the beginning of the animation sequence.


#### Values

- `running`
   - The animation is currently playing.
- `paused`
   - The animation is currently paused.

For Example:

```css
	/* Single animation */
	animation-play-state: running;
	animation-play-state: paused;

	/* Multiple animations */
	animation-play-state: paused, running, running;

	/* Global values */
	animation-play-state: inherited;
	animation-play-state: initial;
	animation-play-state: unset;
```

### `animation-timing-function`  ![CSS3](http://i.imgur.com/kcw73gq.png).

- The `animation-timing-function` `CSS3` property specifies how a CSS animation should progress over the duration of each cycle. The possible values are one or several `timing-function`.

- For keyframed animations, the timing function applies between keyframes rather than over the entire animation. In other words, the timing function is applied at the start of the keyframe and at the end of the keyframe.

- An animation timing function defined within a keyframe block applies to that keyframe; otherwise. If no timing function is specified for the keyframe, the timing function specified for the overall animation is used.

- It is often convenient to use the shorthand property animation to set all animation properties at once.

For Example:

```css
	/* Keyword values */
	animation-timing-function: ease;
	animation-timing-function: ease-in;
	animation-timing-function: ease-out;
	animation-timing-function: ease-in-out;
	animation-timing-function: linear;
	animation-timing-function: step-start;
	animation-timing-function: step-end;

	/* Function values */
	animation-timing-function: cubic-bezier(0.1, 0.7, 1.0, 0.1);
	animation-timing-function: steps(4, end);

	/* Multiple animations */
	animation-timing-function: ease, step-start, cubic-bezier(0.1, 0.7, 1.0, 0.1);

	/* Global values */
	animation-timing-function: inherited;
	animation-timing-function: initial;
	animation-timing-function: unset;
```



Try this at your end and observer how it renders in your browser:

```css
.polling_message {
  color: white;
  float: left;
  margin-right: 2%;            
}

.view_port {
  background-color: black;
  height: 25px;
  width: 100%;
  overflow: hidden;
}

.cylon_eye {
  background-color: red;
  background-image: -webkit-linear-gradient(    left, rgba( 0,0,0,0.9 ) 25%, rgba( 0,0,0,0.1 ) 50%, rgba( 0,0,0,0.9 ) 75%);
  background-image:    -moz-linear-gradient(    left, rgba( 0,0,0,0.9 ) 25%, rgba( 0,0,0,0.1 ) 50%, rgba( 0,0,0,0.9 ) 75%);
  background-image:      -o-linear-gradient(    left, rgba( 0,0,0,0.9 ) 25%, rgba( 0,0,0,0.1 ) 50%, rgba( 0,0,0,0.9 ) 75%);
  background-image:         linear-gradient(to right, rgba( 0,0,0,0.9 ) 25%, rgba( 0,0,0,0.1 ) 50%, rgba( 0,0,0,0.9 ) 75%);
  color: white;
  height: 100%;
  width: 20%;

  -webkit-animation: move_eye 4s linear 0s infinite alternate;
     -moz-animation: move_eye 4s linear 0s infinite alternate;
       -o-animation: move_eye 4s linear 0s infinite alternate;
          animation: move_eye 4s linear 0s infinite alternate;
}

@-webkit-keyframes move_eye { from { margin-left:-20%; } to { margin-left:100%; }  }
   @-moz-keyframes move_eye { from { margin-left:-20%; } to { margin-left:100%; }  }
     @-o-keyframes move_eye { from { margin-left:-20%; } to { margin-left:100%; }  }
        @keyframes move_eye { from { margin-left:-20%; } to { margin-left:100%; }  }
```



----
Go back to `CSS` [Table of Content](css.md)