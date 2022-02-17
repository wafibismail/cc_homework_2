## 3.1. Solution: Comments Do Not Make Up for Bad Code + Explaining Yourself In Code

```javascript
let hypotaneous;

{
    let trig2_opposite = height - boxHeight;
    let trig2_adjacent = this.boxwidth;
    let trig2_x = Math.atan(trig2_opposite / trig2_adjacent);

    let trig1_opposite = boxWidth;
    let trig1_x = Math.PI/2 - trig2_x;
    let trig1_hypotaneous = trig1_opposite /  Math.sin(trig1_x);

    hypotaneous = trig1_hypotaneous;
}