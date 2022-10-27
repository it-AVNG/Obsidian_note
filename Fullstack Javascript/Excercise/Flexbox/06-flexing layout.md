### Hints

-   You may want to search something like `CSS remove list bullets`. We've done this for you in previous examples, but not here. Yay learning.
-   Finding out how to style links in CSS might help you get rid of that pesky underline decoration...
-   We've added `height: 100vh` to the `body`... this makes the body exactly the same height as the viewport. To stick the footer to the bottom you will need to use flex and change the direction to column.

### Self Check

-   The header is at the top of the page, the footer is at the bottom, and they stay in place if you resize your screen.
-   The header and footer have padding.
-   The links in the header and footer are pushed to either side.
-   There is space between the links in the header and footer.
-   The footer has a light gray background (`#eeeeee`).
-   The logo, input and buttons are centered in the screen.
-   The buttons have an appropriate amount of padding.
-   There is space between the logo, input and buttons.

my solution:

```css
/* arranging the body with the same margin and height */
body{
    height: 100vh; /*set height referencing vieport*/
    margin: 0;
    overflow: auto; /*set overflow content to hidden but I like auto*/
    font-family: Roboto, sans-serif;
    display: flex;
    flex-direction: column;

    justify-content: space-between;
 
}
.content{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    margin: 16px;
}
 /* image unchange width */
img{
    width: 600px;;
    flex-shrink: 0;
}

.buttons{
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 5px;

}
button{
    font-family: Roboto, sans-serif;
    border: none;
    border-radius: 4px;/*set the rounded end*/
    background: #eee;
    flex-shrink:0;
    padding: 8px;

    font-weight: 500;
}

.input{
    display: flex;
    justify-content: center;
    align-items: center;
}
input{
    border: 1px solid #ddd;
    border-radius: 16px;
    padding: 8px 24px;
    width: 400px;
    margin-bottom: 16px;
    flex-shrink: 0;

}

ul{
    
    list-style-type: none;
    
}

a{
    text-decoration: none;
    color: gray;
    font-weight: 300;
}

.header{
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    
}

.footer{
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    background-color: lightgrey;
}

.left-links{
   
    display: flex;
    justify-content: space-around;
    align-items: center;
    gap: 16px;
    padding:0px 20px;
}

.right-links{
   
    display: flex;
    justify-content: space-around;
    align-items: center;
    gap:16px;
    padding:0px 20px;
}
```

System solution:

```css
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

body {
  height: 100vh;
  margin: 0;
  overflow: hidden;
  font-family: Roboto, sans-serif;
}

img {
  width: 600px;
}

button {
  font-family: Roboto, sans-serif;
  border: none;
  border-radius: 8px;
  background: #eee;
}

input {
  border: 1px solid #ddd;
  border-radius: 16px;
  padding: 8px 24px;
  width: 400px;
  margin-bottom: 16px;
}

/* SOLUTION */

body {
  display: flex;
  flex-direction: column;
}

button {
  padding: 8px 16px;
}

.content {
  flex: 1;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

a {
  color: #666;
  text-decoration: none;
}

.header,
.footer {
  display: flex;
  justify-content: space-between;
  padding: 16px;
}

.footer {
  background: #eee;
}

ul {
  display: flex;
  list-style: none;
  margin: 0;
  padding: 0;
  gap: 16px
}
```
