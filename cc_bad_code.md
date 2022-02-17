## 3.1. Comments Do Not Make Up for Bad Code + Explaining Yourself In Code

The code below is disorganized
```javascript
/*The hypotaneous, h is derived by the trigonometric formula h = opposite_1/sin(x),
where opposite_1 is the boxWidth, and x is derived from PI/2 - y,
where y is derived from tan-1(opposite_2/adjacent_2),
where opposite_2 is this.height-boxHeight, and adjacent_2 is this.width*/
let hypotaneous = boxWidth/(Math.sin(Math.PI/2 - Math.atan((this.height-boxHeight)/this.width)));
```
and organizing it would be a more appropriate form of clarifying its content rather than putting the explanation in comment form.

