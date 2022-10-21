[Referencing Document](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model)

# Everything is Boxes
+ In CSS everything is a box, text, button, div, span, etc is a box
+ ![box model][Boxmodel.png]
+ When set Height and width without any additional rules. We are setting the content of the DOM.
+ If we would like to set the diension of the box from the border, we use `box-sizing: border-box;` declaration for our CSS
## Padding
+ Occurs inside the background and goes around the content of the model

## Border
+ Goes around the Padding
+ We can control all margins of an element at once using the property, or each side individually(see the margin section below) as weel as the color. We can also mix the position and the below properties together as well
+ [`border-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-width)
- [`border-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-style)
- [`border-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-color)

## Margin
+ Goes around 2 Items and space them from each other
+ The Margin of each Item is overlap and the distance is the larges margin
+ We can control all margins of an element at once using the property, or each side individually
	- [`margin-top`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-top)
	- [`margin-right`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-right)
	- [`margin-bottom`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-bottom)
	- [`margin-left`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-left)

