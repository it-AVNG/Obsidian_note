here are some CSS properties that use frequently

### Color and background-color

`color`set element color while `background-color` set the back ground of the element, accept HSL RGB HEX color values as well as words such as `red` or `transparent` [](https://www.w3schools.com/cssref/css_colors_legal.asp)[https://www.w3schools.com/cssref/css_colors_legal.asp](https://www.w3schools.com/cssref/css_colors_legal.asp)

### Typography Basics and Text-align

`font-family` can be a single value or a CSV that determine what font an element uses. Each font will fall into one or two categories either a “font family name” like `"Times New Roman"`(we use quotes due to the whitespace between words) or a “generic family name” like `sans-serif`  (generic family names never use quotes).

It’s best practice to include a list of values for this property, starting with the font you want to be used most and ending with a generic font family as a fallback, e.g. `font-family: "Times New Roman", sans-serif;`

`font-size` will, as the property name suggests, set the size of the font. When giving a value to this property, the value should not contain any whitespace, e.g. `font-size: 22px`  has no space between “22” and “px”.

`font-weight` affects the boldness of text, assuming the font supports the specified weight. This value can be a keyword, e.g. `font-weight: bold` , or a number between 1 and 1000, e.g. `font-weight: 700`  (the equivalent of `bold` ). Usually, the numeric values will be in increments of 100 up to 900, though this will depend on the font.

`text-align` will align text horizontally within an element, and you can use the common keywords you may have come across in word processors as the value for this property, e.g. `text-align: center`

example:
```css
.p1 {  font-family: "Times New Roman", Times, serif;}  
  
.p2 {  font-family: Arial, Helvetica, sans-serif;}  
  
.p3 {  font-family: "Lucida Console", "Courier New", monospace;}
```

### Image height and width

It is best to leave one property as ‘auto’ while adjusting the other to mitigate setting problems while loading

```css
img {
  height: auto;
  width: 500px;
}
```

### Cascade of CSS

The cascade is what determines which rules actually get applied to our HTML.

-   Specificity
    
    A CSS declaration that is more specific will take precedence over less specific ones.
    
    The ranking for each type as follow
    
    1.  ID selectors (most specific)
    2.  Class selector
    3.  Type selector
    4.  The one that has more selectors

Selectors does not adding to the specificity
![Selectors][css_properties.png]
-   Inheritance
    
    a certain CSS properties that applied to an element is always inherited by that element’s descendants like typography, most properties aren’t.
    
-   Rule Order
    
    Which element was the last defined rule, win the specification order
    

### Adding CSS to HTML

-   External CSS
    
    creating a separate file for CSS and linking it inside HTML opening and closing `head` tag with a self closing `link` element
    
    ```html
    <head>
    	<link rel="stylesheet" href="styles.css">
    </head>
    ```
    
    the URL inside `href` is realtive to the element inside of the HTML file
    
    then in our CSS styles.css file, we add selectors followed by a pair of opening and closing curl braces
    
    1.  it keeps our HTML and CSS separated, which results in the HTML file being smaller and making things look cleaner.
    2.  We only need to edit the CSS in _one_ place, which is especially handy for websites with many pages that all share similar styles
-   Internal CSS
    
    Adding CSS with the HTML file itself
    
    ```html
    <head>
      <style>
        div {
          color: white;
          background-color: black;
        }
    
        p {
          color: red;
        }
      </style>
    </head>
    <body>...</body>
    ```
    
    Useful for adding unique styles to a single page of a website
    
-   Inline CSS
    
    add styles directly to the HTML element
    
    ```html
    <body>
      <div style="color: white; background-color: black;">...</div>
    </body>
    ```
    
    The first thing to note is that we don’t actually use any selectors here, since the styles are being added directly to the opening `<div>`tag itself. Next, we have the `style=`attribute, with its value within the pair of quotation marks being the declarations.
    
    If you need to add a _unique_ style for a _single_ element, this method can work just fine
    
    Any inline CSS will override the other two methods, which can cause unexpected results. (While we won’t dive into it here, this can actually be taken advantage of).