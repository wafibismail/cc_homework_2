## 4.1. Comments Do Not Make Up for Bad Code + Explaining Yourself In Code

The code below is disorganized
```javascript
/*The hypotaneous, h is derived by the trigonometric formula h = opposite_1/sin(x),
where opposite_1 is the boxWidth, and x is derived from PI/2 - y,
where y is derived from tan-1(opposite_2/adjacent_2),
where opposite_2 is this.height-boxHeight, and adjacent_2 is this.width*/
let hypotaneous = boxWidth/(Math.sin(Math.PI/2 - Math.atan((this.height-boxHeight)/this.width)));
```
and organizing it would be a more appropriate form of clarifying its content rather than putting the explanation in comment form.

## 4.2 Good Comments

### Legal Comments

```javascript
//Not including the required legal comments
```

<!--### Informative Comments-->
### Explanation of Intent & Warning of Consewuences

Without sufficient context one would wonder why a piece of code exists
```c
int i = 0, n;
while(1){
    n = array[i];
    i = (i+1) % (sizeof(array)/sizeof(int));
}
```
In such case adding an explanation via. comment would be appropriate.
In addition, a warning too, of the possibly undesired consequences of running a piece would be of help.

### TODO Comments

Some codes may only be required temporarily
```html
<div id='deprecated-feature-container-0'></div>
```
In such cases, it is best to state it as such.

### Amplification

An explanation on why seemingly inconsequential things are done would be useful. In this case, the need for splitting the request parameters when it may already seem to be readable as an array
```javascript
router.get('/:id', function(req, res, next) {
    var idArray = req.params['id'].split(',');
    var itemsAll = getItems();
    var itemsToBeSent = {};
    for (var i = 0; i < idArray.length; i++){
        itemsToBeSent[idArray[i]] = itemsAll[idArray[i]];
    }
    res.json(itemsToBeSent);
});
```

## 4.3 Bad Comments

### Mumbling

```css
@media screen and (max-width: 640px) {
  .overlay .closebtn {
    font-size: 13vw;
    margin-top: 2vh;
    /*Because blockage, require space*/
  }
}
```

<!--### Redundant Comments-->
<!--### Misleading Comments-->
<!--### Mandated Comments-->
<!--### Noise Comments-->
<!--### Scary Noise-->
<!--### Don't Use a Comment When You Can Use a Function or a Variable>
<!--### Position Markers-->
<!--### Closing Brace Comments>
<!--### Attribution and Bylines>
<!--### Commented-Out Code-->
<!--### HTML Comments>
<!--### Nonlocal Information-->
<!--### Too Much Information-->
<!--### Inobvious Connection-->
<!--### Function Headers-->
<!--### Javadocs in Nonpublic Code-->
<!--### Bibliography-->