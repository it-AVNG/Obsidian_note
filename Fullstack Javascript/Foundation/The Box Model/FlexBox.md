Positioning element using flexbox
Flexcontainers adn FlexItems
create usefull components and layout that go beyong stacking and centering
***IMPORTANT to remember is that get used to inspecting usong chrome developer tools***

Flex box is away for us to arrange item into rows or columns. They will "flex" according to rules we define.
We turn any container into flexbox by the syntax below:

```css
.flex-container{
	display:flex
}
```

The syntax belows helps sets all the child div inside the container into flexbox.

```css
.flex-cointainer-item{
	flex: 1;
}
```

The flexbox will arrange them self and fill the area and they will have equal width.

## Flex container and flex items:

a flex container is a container of multiple flex items, and position them INSIDE the container.

A flex container is the selectors that has display value turns into `display: flex;` we are telling the browser that everything inside the container is rendered using flexbox instead of default box model

let use the following html example:
```html
<!DOCTYPE html>

<html lang='en'>

<head>

<meta charset='UTF-8'/>

<title>Some Web Page</title>

<link rel='stylesheet' href='styles.css'/>

<meta name="viewport" content="width=device-width, inital-scale=1.0">

</head>

<body>

<div class='menu-container'>

<div class='menu'>

<div class='date'>Aug 14, 2016</div>

<div class='signup'>Sign Up</div>

<div class='login'>Login</div>

</div>

</div>

</body>

</html>

```

### Aligning a flex item, centering a div:
After we have a flex container we align the item using `justify-content: center`
note: other values for justify-content:
	+ center : packs items around the center
	+ flex-start : packs items from the start
	+ flex-end : packs Items from the ends
	+ space-around : distribute Items evenly Items have half-size space on either ends
	+ space-between: distribute Items evenly, first Item is flush with the start, last is flush with the end
	check the [reference](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content) for more items

adding that to our stylesheet

```css
*{

margin: 0;

padding: 0;

box-sizing: border-box;

font-family: Arial, Helvetica, sans-serif;

}

.menu-container {

color: #fff;

background-color: #5995DA; /* Blue */

padding: 20px 0;

display: flex;

justify-content: center;

}

  

.menu {

border: 1px solid #fff; /* For debugging */

width: 800px;

}

```

### Grouping flex Items
When we group flex items together in a `<div>` we basicly creating another web page altogether.

we add a `.links` div acting as containers for the signup and login class
```html
<div class="links">

	<div class='signup'>Sign Up</div>
	<div class='login'>Login</div>

</div>
```

Give it a style and display flexbox 

```css
.links{

border: 1px solid #fff; /* For debugging */

display: flex;

justify-content: flex-end;

}

  

.login{

margin-left: 20px;

}
```

### Cross axis and vertical alignment
`justify-content` helps us align the container and its item in horizontal; for veritical, we use `align-items`.
Check the [reference](https://cssreference.io/property/align-items/) for the properties of the align-items.

### Wrapping flex items
when extra Items does not fit with our alignment horizontaly and vertically, sometime they would ascrewed our screen, thus `flex-warp: warp` to the rescue.
the propert will pump the extra itmes to another row.

### Flex conainer direction:
"Directions" refers to whether a container renders its items horizintally or vertically. All container is default in horizontal direction. 
+ `flex-direction: row;` means direction of the flex is laid out in a line until they reach the ends
+ `flex-firection: column;` means the items are stacked.

The `flex-direction`also offers controlling the order which items appear via row-reverse or column-reverse property.  

### alignment consideration:
When we rotate an flexbox element, we also rotate its alignment. In order to properly center the div, it is a good practice to add `justify-content` and `align-items` properly.

### Adding order to flex items
`order` helps arranging items order in the flex container, the lower the number, the higher the order. 
The default order is the order inwhich they are added in the source file html.

### Flex item alignment
`align-self` helps overwrite value sets be containers for specific Items inside the flex container.
Some value we can adapt to our design:
+ center
+ flex-start (top)
+ flex-end (bottom)
+ strech
+ baseline

### Flexible Items

Flex items are, well, *flexible*. Each Items can have a flexible width, grow, distribution. Let consider a footer as follow

```html
<footer>
	<div class="footer-item footer-oner"></div>
	<div class="footer-item footer-two"></div>
	<div class="footer-item footer-three"></div>
</footer>

```

with css style

```css
.footer-item{
	border: 1px solid white;
	background-color: #D6E9FE;
	height: 200px;
	flex: 1;
}
```

The `flex` is a consituent properties shor hand for
+ flex-grow
+ flex-shrink
+ flex-basis

The `flex: 1` tells the items to stretch to match the width of the `.footer` since they all have the same weight, they will strecht equally

If, one of the item has `flex: 2`, it means they have grow factor equal to twice the grow factor of other element.

`flex` distribute the free space into the element while `justify-content` distribute space between the items.

We can also manipulate the distribution with flex property.
Examples:
```css
.footer-three,

.footer-one{

background-color: #5995da;

flex: initial;

width: 300px;

}
```

### Flex items auto-margins
With margin setting such as `margin-left: auto;` or `margin: auto` the margin will eats and distribute the available margin as specified. 
Setting the `margin` property on a flex child will push the child away from that direction. Set `margin-left` to `auto`, the child will push right. Set `margin-top` to `auto` and the child will push to the bottom.