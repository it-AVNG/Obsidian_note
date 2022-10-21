### [Assignment](https://www.theodinproject.com/lessons/foundations-block-and-inline#assignment)

1.  The concept of “Normal flow” is implied in the box-model resources, but isn’t laid out very specifically. Read [“Normal Flow” from MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Normal_Flow) to make sure you understand how elements lay themselves out by default.
2.  W3 schools’ [“HTML Block and Inline Elements”](https://www.w3schools.com/html/html_blocks.asp) has a description and a list of all the default block and inline elements.
3.  The Digital Ocean tutorial [“Inline vs Inline-block Display in CSS”](https://www.digitalocean.com/community/tutorials/css-display-inline-vs-inline-block) has a couple of great examples that clarify the difference between `inline` and `inline-block`.
4.  Go to our [CSS exercises repository](https://github.com/TheOdinProject/css-exercises) and do “01-margin-and-padding-1” and “02-margin-and-padding-2” in the `margin-and-padding` directory.

# Block and inline boxes
+ In CSS we have 2 types of boxes - **block Boxes** and **inline boxes**. The Type refers to how the box behaves in terms of page flow and in relation to other boxes.
+ Boxes has **Inner display type** and **Outer display type**
+ `display` type can be set by using [display property](https://developer.mozilla.org/en-US/docs/Web/CSS/display)

## Outter display
+ If a box has an outter display of a `block` then
	+ Box will break into a newlinr
	+ The `width` and `length` will be respected
	+ Padding, margin, border will cause other element to be pushed away from the box
	+ Direction of extension: inward
	+ by default, some HTML such as `<h1>` and `<p>` use block as their outer display type

## Inner display type
Please check the laidout in [normal flow](obsidian://open?vault=Fullstack%20Javascript&file=Foundation%2FThe%20Box%20Model%2FNormalflow)
The elements layout in normal flow and behave as block or inline boxes
Changing the inner display type by `dispaly: flex;` the element will still use outter display type `block` but the inner display type to flex.
>Reminder: \<span>\ element means inline block 

## What is the CSS box model
+ The CSS box model as a whole applies to block boxes and defines how different parts of the bo work toghether 
+ **Parts of a box**:
	+ Content box: Area where content is displayed. Sizing using `inline-size` and `block-size` or `width`and `height`
	+ Padding box: Sits around content as white space; Size it using `padding` and related properties
	+ Border box: warps around the content and padding, Size it using`border`
	+ Margin box: Out most layer, acting as white space between elements, sizing using `margin`

+ **Best practice CSS box model** :
Turn on the alternative model, set `box-sizing: border box`
```css
.box {
  box-sizing: border-box;
  width: 350px;
  inline-size: 350px;
  height: 150px;
  block-size: 150px;
  margin: 10px;
  padding: 25px;
  border: 5px solid black;
}
```

The actuall space taken will be 350px int'the inline direction and 150px in the block direction 

In practice, in css style sheet we set the following is true
```css
html { box-sizing: border-box; } 

*, *:before, *:after { box-sizing: inherit; }

```
