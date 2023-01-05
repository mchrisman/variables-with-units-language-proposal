#  A truly modest language feature request: *primitive number variables* with units

This seems like it should be so easy to add to most c-style languages, and so useful, that I don't get why it hasn't been done.

```
unit horizontal_pixels int;
unit vertical_pixels int;

var horizontal_pixels x,dx;
var vertical_pixels y,dy;

x += dx;
y += dx;   // fails without explicit cast
```
Or with declared conversion ratios:
```
unit inches:double;
unit meters:39.37 inches;

var inches ceiling_height;
var meters roof_height = (meters)10;

// fails without cast
let ceiling_height = roof_height/2; 

// converts
let ceiling_height = (inches)roof_height/2;

// assigns without conversion
let ceiling_height = (double)roof_height/2;
```
