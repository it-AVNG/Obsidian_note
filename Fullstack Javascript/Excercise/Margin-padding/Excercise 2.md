- There is 8px between the edge of the card and its content (the blue sections).
- There is an 8px gap between each of the blue sections inside the card.
- The title of the card uses a 16px font.
- There are 8px between the title text and the edge of the title section.
- The content section has 16px space on the top and bottom, and 8px on either side.
- Everything inside the `.button-container` section is centered, and there is 8px padding.
- The Big Button is centered on its own line.
- The Big Button has 24px space on the sides, and 8px on top and bottom.
```css
body {

background: #eee;

font-family: sans-serif;

}

  

.card {

width: 400px;

background: #fff;

margin: 16px auto;

}

  

.title {

background: #e3f4ff;

}

  

.content {

background: #e3f4ff;

}

  

.button-container {

background: #e3f4ff;

}

  

button {

background: white;

border: 1px solid #eee;

}

  

/* SOLUTION */

  

/* disclaimer: duplicating the selectors here isn't best practice.

In your solution you probably put it right inside the existing selectors,

which _is_ the best practice.

  

We separated it out here to make it extra clear what has changed. */

  

.card {

padding: 8px;

}

  

.title {

margin-top: 0;

margin-bottom: 8px;

font-size: 16px;

padding: 8px;

}

  

.content {

margin-bottom: 8px;

padding: 16px 8px;

}

  

.button-container {

text-align: center;

padding: 8px;

}

  

button {

display: block;

margin: 0 auto;

padding: 8px 24px;

}
```
