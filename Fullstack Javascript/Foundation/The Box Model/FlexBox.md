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

A flex container is 