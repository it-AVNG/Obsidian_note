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
.flex-cointainer{
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