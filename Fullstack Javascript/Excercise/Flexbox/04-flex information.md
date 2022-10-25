### Self Check

- All items are centered on the page (horizontally, not vertically).
- The title is centered on the page.
- There is 32px between the title and the 'items.'
- There is 52px between each item.
- The items are arranged horizontally on the page.
- The items are only 200px wide and the text wraps.
- The item text is centered.


solution:

```html

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Information</title>
    <link rel="stylesheet" href="style.css">
  </head>
  <body>
   
      <div class="title">Information!</div>
    

    <div id="content"> 

      <div class="item one">
        <img src="./images/barberry.png" alt="barberry">
        <div class="text">This is a type of plant. We love this one.</div>
      </div>

      <div class="item two">
        <img src="./images/chilli.png" alt="chili">
        <div class="text">This is another type of plant. Isn't it nice?</div>
      </div>
      
      <div class="item three">      
        <img src="./images/pepper.png" alt="pepper">
        <div class="text">We have so many plants. Yay plants.</div>
      </div>

      <div class="item four">
        <img src="./images/saffron.png" alt="saffron">
        <div class="text">I'm running out of things to say about plants.</div>
      </div>

    </div>
    <!-- disregard this section, it's here to give attribution to the creator of these icons -->
    <div class="footer">
      <div>Icons made by <a href="https://www.flaticon.com/authors/icongeek26" title="Icongeek26">Icongeek26</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div>
    </div>
  </body>
</html>
```


```css
body {
  font-family: 'Courier New', Courier, monospace;
  text-align: center;
}

img {
  width: 100px;
  height: 100px;

}

#content{
  display: flex;
  justify-content: center;
  gap: 52px;
}

.title {
  font-size: 36px;
  font-weight: 900;
  margin-bottom: 32px;
}

.item{
  max-width:200px;
}
/* do not edit this footer */
.footer {
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  height: 52px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #eee;
}
```