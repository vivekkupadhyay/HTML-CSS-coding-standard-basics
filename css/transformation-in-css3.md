## Transform in CSS3 ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `CSS3` `transform` property lets you modify the coordinate space of the `CSS3` visual formatting model. Using it, elements can be translated, rotated, scaled, and skewed.

- If the property has a value different than none, a stacking context will be created. In that case the object will act as a containing block for position: fixed elements that it contains.


#### Values

- `transform-function`
    One or more of the CSS transform functions to be applied, see below.
- `none`
    Specifies that no transform should be applied. 

### Transform Function ( `transform-function` ) ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `transform-function` `CSS3` data type denotes a function applied to an element's representation in order to modify it. Usually such transform may be expressed by matrices and the resulting images can be determined using matrix multiplication on each point.


#### `matrix()` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `matrix()` `CSS3` function specifies a homogeneous 2D transformation matrix comprised of the specified six values. The constant values of such matrices are implied and not passed as parameters; the other parameters are described in the column-major order.

- matrix(a, b, c, d, tx, ty) is a shorthand for matrix3d(a, b, 0, 0, c, d, 0, 0, 0, 0, 1, 0, tx, ty, 0, 1).

For Example:

```css
	matrix(a, b, c, d, tx, ty)
```


#### `matrix3d()` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `matrix3d()` `CSS3` function describes a 3D transform as a 4x4 homogeneous matrix. The 16 parameters are described in the column-major order.

For Example:

```css
	matrix3d(a1, b1, c1, d1, a2, b2, c2, d2, a3, b3, c3, d3, a4, b4, c4, d4)
```

#### `perspective()` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `perspective()` `CSS3` function defines the distance between the z=0 plane and the user in order to give to the 3D-positioned element some perspective. Each 3D element with z>0 becomes larger; each 3D-element with z<0 becomes smaller. The strength of the effect is determined by the value of this property.


For Example:

```css
	perspective(l)
```

#### `rotate()` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `rotate()` `CSS3` function defines a transformation that moves the element around a fixed point (as specified by the transform-origin property) without deforming it. The amount of movement is defined by the specified angle; if positive, the movement will be clockwise, if negative, it will be counter-clockwise. A rotation by 180° is called point reflection.

![transform rotate](http://i.imgur.com/0v8Dvhk.png)

For Example:

```css
	rotate(a)
```

#### `rotate3d()` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `rotate3d()` `CSS3` function defines a transformation that moves the element around a fixed axis without deforming it. The amount of movement is defined by the specified angle; if positive, the movement will be clockwise, if negative, it will be counter-clockwise.

- In the 3D space, rotations have three degrees of liberty, describing an axis of rotation. The axis of rotation is defined by an [x, y, z] vector and pass by the origin (as defined by the transform-origin CSS property. If the vector is not normalized, that is the sum of the square of its three coordinates is not 1, it will be normalized internally. A non-normalizable vector, like the null vector, [0, 0, 0], will cause the rotation not to be applied, without invaliding the whole CSS property.


##### Values

- `x`
    - It is a `number` describing the x-coordinate of the vector denoting the axis of rotation.
- `y`
    - It is a `number` describing the y-coordinate of the vector denoting the axis of rotation.
- `z`
    - It is a `number` describing the z-coordinate of the vector denoting the axis of rotation.
- `a`
    - It is an `angle` representing the angle of the rotation. A positive angle denotes a clockwise rotation, a negative angle a counter-clockwise one. 

For Example:

```css
	rotate3d(x, y, z, a)
```

#### `rotateX()` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `rotateX()` `CSS3` function defines a transformation that moves the element around the abscissa without deforming it. The amount of movement is defined by the specified angle; if positive, the movement will be clockwise, if negative, it will be counter-clockwise.

- The axis of rotation passes by the origin, defined by `transform-origin` CSS3 property.

- `rotateX(a)` is a shorthand for `rotate3D(1, 0, 0, a)`.

For Example: 

```css
	rotateX(a)
```


#### `rotateY()` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `rotateY()` `CSS3` function defines a transformation that moves the element around the ordinate without deforming it. The amount of movement is defined by the specified angle; if positive, the movement will be clockwise, if negative, it will be counter-clockwise.

- The axis of rotation passes by the origin, defined by `transform-origin` CSS3 property.

- `rotateY(a)`is a shorthand for `rotate3D(0, 1, 0, a)`.

- In opposition to rotations in the plane, the composition of 3D rotations is usually not commutative; it means that the order in which the rotations are applied is crucial.

For Example:

```css
	rotateY(a)
```

#### `rotateZ()` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `rotateZ()` CSS3 function defines a transformation that moves the element around the z-axis without deforming it. The amount of movement is defined by the specified angle; if positive, the movement will be clockwise, if negative, it will be counter-clockwise.

- The axis of rotation passes by the origin, defined by `transform-origin` CSS3 property.

- `rotateZ(a)`is a shorthand for `rotate3D(0, 0, 1, a)`.

- In opposition to rotations in the plane, the composition of 3D rotations is usually not commutative; it means that the order in which the rotations are applied is crucial.


For Example:

```css
	rotateZ(a)
```


#### `scale()` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `scale()` `CSS3` function modifies the size of the element. It can either augment or decrease its size and as the amount of scaling is defined by a vector, it can do so more in one direction than in another one.

- This transformation is characterized by a vector whose coordinates define how much scaling is done in each direction. If both coordinates of the vector are equal, the scaling is uniform, or isotropic, and the shape of the element is preserved. In that case, the scaling function defines a homothetic transformation.

- When outside the ]-1, 1[ range, the scaling enlarges the element in the direction of the coordinate; when inside the range, it shrinks the element in that direction. When equal to 1 it does nothing and when negative it performs a point reflection and the size modification.

![transform rotate](http://i.imgur.com/QECRUCS.png)


For Example:

```css
	scale(sx) or
	scale(sx, sy)
```


#### `scale3d()` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `scale3d()` CSS3 function modifies the size of an element. Because the amount of scaling is defined by a vector, it can resize different dimensions at different scales.

- This transformation is characterized by a vector whose coordinates define how much scaling is done in each direction. If all three coordinates of the vector are equal, the scaling is uniform, or isotropic, and the shape of the element is preserved. In that case, the scaling function defines a homothetic transformation.

- When outside the [-1, 1] range, the scaling enlarges the element in the direction of the coordinate; when inside the range, it shrinks the element in that direction. When equal to 1 it does nothing and when negative it performs a point reflection and the size modification.


##### Values

- `sx`
    - It is a `number` representing the abscissa of the scaling vector.
- `sy`
    - It is a `number` representing the ordinate of the scaling vector.
- `sz`
    - It is a `number` representing the z-component of the scaling vector. 


For Example:

```css
	scale3d(sx, sy, sz)
```


#### `scaleX()` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `scaleX()` CSS3 function modifies the abscissa of each element point by a constant factor, except if this scale factor is 1, in which case the function is the identity transform. The scaling is not isotropic and the angles of the element are not conserved.

- `scaleX(sx)` is a shorthand for `scale(sx, 1)` or for `cale3d(sx, 1, 1)`.

- `scaleX(-1)` defines an axial symmetry with a vertical axis passing by the origin (as specified by the transform-origin 

![transform scaleX](http://i.imgur.com/7t83DWt.png)

For Example:

```css
	scaleX(s)
```



#### `scaleY()` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `scaleY()` CSS3 function modifies the ordinate of each element point by a constant factor except if this scale factor is 1, in which case the function is the identity transform. The scaling is not isotropic and the angles of the element are not conserved.

- `scaleY(sy)` is a shorthand for scale(1, sy) or for scale3d(1, sy, 1).

- `scaleY(-1)` defines an axial symmetry with a horizontal axis passing by the origin (as specified by the transform-origin property).


![transform scaleY](http://i.imgur.com/NszZpfk.png)

For Example:

```css
	scaleY(s)
```



#### `scaleZ()` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `scaleZ()` CSS3 function modifies the z-coordinate of each element point by a constant factor, except if this scale factor is 1, in which case the function is the identity transform. The scaling is not isotropic and the angles of the element are not conserved.

- `scaleZ(sz)` is a shorthand for scale3d(1, 1, sz).

- `scaleZ(-1)` defines an axial symmetry along the z-axis passing by the origin (as specified by the transform-origin property).

For Example:

```css
	scaleZ(s)
```

#### `skew()` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `skew()` CSS3 function is a shear mapping, or transvection, distorting each point of an element by a certain angle in each direction. It is done by increasing each coordinate by a value proportionate to the specified angle and to the distance to the origin. The more far from the origin, the more away the point is, the greater will be the value added to it.


#### `skewX()` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `skewX()` CSS3 function is a horizontal shear mapping distorting each point of an element by a certain angle in the horizontal direction. It is done by increasing the abscissa coordinate by a value proportionate to the specified angle and to the distance to the origin. The more far from the origin, the more away the point is, the greater will be the value added to it.


#### `skewY()`

- The `skewY()` CSS3 function is a vertical shear mapping distorting each point of an element by a certain angle in the vertical direction. It is done by increasing the ordinate coordinate by a value proportionate to the specified angle and to the distance to the origin. The more far from the origin, the more away the point is, the greater will be the value added to it.


For Example:

```css

	skew(ax)       or
	skew(ax, ay)

	skewX(a)
	skewY(a)

```


#### `translate()` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `translate()` CSS3 function moves the position of the element on the plane. This transformation is characterized by a vector whose coordinates define how much it moves in each direction.


![transform translate](http://i.imgur.com/y7pBFO9.png)


#### `translate3d()` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `translate3d()` CSS3 function moves the position of the element in the 3D space. This transformation is characterized by a 3-dimension vector whose coordinates define how much it moves in each direction.

#### `translateX()` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `translateX()` CSS3 function moves the element horizontally on the plane. This transformation is characterized by a <length> defining how much it moves horizontally.

- `translateX(tx)` is a shortcut for translate(tx, 0).


![transform translateX](http://i.imgur.com/PWfDrbg.png)


#### `translateY()` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `translateY()` CSS3 function moves the element vertically on the plane. This transformation is characterized by a <length> defining how much it moves vertically.

- `translateY(ty)` is a shortcut for translate(0, ty).

![transform translateY](http://i.imgur.com/khEBc5P.png)


#### `translateZ()` ![CSS3](http://i.imgur.com/kcw73gq.png)

- The `translateZ()` CSS3 function moves the element along the z-axis of the 3D space. This transformation is characterized by a <length> defining how much it moves.

- `translateZ(tz)` is a shorthand for translate3d(0, 0, tz).


For Example:

```css
	translate(tx)       or
	translate(tx, ty)

	translate3d(tx, ty, tz)
	translateX(t)
	translateY(t)
	translateZ(t)
```

##### Values

- `tx`
    Is a `length` representing the abscissa of the translating vector.
- `ty`
    Is a `length> representing the ordinate of the translating vector.
- `tz`
    Is a `length` representing the z component of the translating vector. It can't be a `percentage` value; in that case the property containing the transform is considered invalid. 



----
Go back to `CSS` [Table of Content](css.md)