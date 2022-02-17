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
```
## Good Comments

### Legal Comments

```javascript
/*Copyright (c) 2022 Wafi B

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

...*/
```

<!--### Informative Comments-->
### Explanation of Intent

```c
//Warning: Endless loop
//Intended to simulate memory usage in running apps
int i = 0, n;
while(1){
    n = array[i];
    i = (i+1) % (sizeof(array)/sizeof(int));
}
```

### TODO Comments

```html
<!--
    TODO - the next line will no longer be used in deployment.
    It is to be removed as soon as <a planned feature implementation> has been implemented
-->
<div id='deprecated-feature-container-0'></div>
```

### Amplification

```javascript
router.get('/:id', function(req, res, next) {
    var idArray = req.params['id'].split(',');
    //The request parameters must not be directly read as an array
    //It would lead to it being read as a string of characters instead
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
    /*To compensate for browser top bars potentially blocking the view on some phones, top margin is enlarged*/
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