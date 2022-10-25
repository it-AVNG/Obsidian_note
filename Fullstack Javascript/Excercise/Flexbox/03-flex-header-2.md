edit the HTML a little bit. Often with flexbox you need to add containers around things to make them go where you need them to go. In this case, you probably want to separate the items that go on the left and right of the header.

This is also the first example where you'll be nesting flex containers inside each other.
this one needs to be flexible in the middle, with items pushed to the left and right.

### Self Check
- Everything is centered vertically inside the header.
- There is 8px space between everything and the edge of the header.
- Items are arranged horizontally as seen in the outcome image.
- There is 16px between each item on both sides of the header.
- flex is used to arrange everything.

raw html
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flex Header 2</title>
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
    <div class="header">
      <div class="right-links">
        <div class="logo">
        LOGO
        </div>
        <ul class="links">
        <li><a href="https://www.google.com">link-one</a></li>
        <li><a href="https://www.google.com">link-two</a></li>
        <li><a href="https://www.google.com">link-three</a></li>
        </ul>
      </div>
      <div class="left-links">
        <button class="notifications">
        1 new notification
        </button>
        <div class="profile-image"></div>
      </div>
    </div>
  </body>
</html>
```

CSS

```css

/* this is some magical font-importing.  
you'll learn about it later. */
@import url('https://fonts.googleapis.com/css2?family=Besley:ital,wght@0,400;1,900&display=swap');

body {
  margin: 0;
  background: #eee;
  font-family: Besley, serif;
}

.header {
  
  /* original code */
  background: white;
  border-bottom: 1px solid #ddd;
  box-shadow: 0 0 8px rgba(0,0,0,.1);
  /* turn on flexing and center all the divs */
  display: flex;
  justify-content: space-between;
  align-items: center;

}
/* grouping the right and left links */
.right-links,
.left-links{
  display: flex;
  justify-content: flex-start;
  align-items: center;
  
}


.profile-image {
  
  background: rebeccapurple;
  box-shadow: inset 2px 2px 4px rgba(0,0,0,.5);
  border-radius: 50%;
  width: 48px;
  height: 48px;
  /*add margin from the edge and other elements*/
  margin: 8px 16px;
}

.logo {
  color: rebeccapurple;
  font-size: 32px;
  font-weight: 900;
  font-style: italic;
  /* insert logo magrin */
  margin: 8px 16px;
}

button {
  border: none;
  border-radius: 8px;
  background: rebeccapurple;
  color: white;
  padding: 8px 24px;
}

a {
  /* this removes the line under our links */
  text-decoration: none;
  color: rebeccapurple;
}

ul {
  list-style-type: none;
  /*I add this*/
  display: flex;
  padding:0; 
  gap:16px; 
  
}


```

