This refer to the HTML element to which CSS rule apply; they are what is actually being “selected” for each rule.

### Universal Selector

The universal selector will select elements of any type, hence the name “universal”, syntax is at below. in the example below, every element would have the `color: purple` style apply to it

```css
*{
	color: purple;
}
```

### Type selectors

A type selector or element selector will select all elements of given element type, syntax is the name of the element

```css
div{
color: white;
}
```

The above example means all the element called `div` will be in white

### Class Selectors

Class selectors will select all elements with the given class, which is just an attribute you place on an HTML element

```html
<!-- index.html -->
<div class="alert-text"> please agree. </div>
```

```css
/* styles.css */
.alert-text {
	color: read;
}
```

the syntax for class selectors: a period immediately followed by the case-sensitive value of the class attribute.

class attributes is not unique; elements can have multiple class syntax as follow `class="class-1 class-2"` a space is use as seperator so hyphen is use instead of space for class names

### ID selectors

the same as class selector but element can only have **one** ID. Use ID _sparingly_

```css
#title {
background-color: red;
}
```

### Grouping Selectors

What if we have two or more groups of elements share some their style declaration? We can group them using comma-separated list

```css
.read,
.unread {
color: white;
background-color: black;
}

.read{
/* unique declaration for read style */
}

.unread{
/* unique declaration for unread style */
} 
```

### Chaining selectors

Anotherway to use selectors is to chain them as a list without seperation.

```html
<div>
	<div class="subsection header">Latest Posts</div>
	<p class="subsection preview">This is where a preview for a post</p>
</div>
```

_subsection_ class have a unique styles but what if we only want to apply a separate rule to the element that also has header as a second class? Well we chain them all in CSS

```css
.subsection.header{

color: red;
}
```

What `.subsection.header` does is it selectd any elements has both `subsection` and `header` classes, there is no space in a chain. Syntax for chaining class and ID as follow `.class#ID` you can’t chain more than one type selector since an element can’t be two different types at once.

### Descendant Combinator

A descendant combinator, represents by a single space between selectors. A descendant combinator will only cause elements that match the last selector to be selected IF they also have an ancestor that matches previous selector.

```html
<div class="ancestor"> <!-- A -->
	<div class="contents"> <!-- B -->
    <div class="contents"> <!-- C -->
    </div>
  </div>
</div>

<div class="contents"></div> <!-- D -->
```

```css
/* styles.css */

.ancestor .contents {
  /* some declarations */
}
```

The example shows that only the class `.contents` has the parents(nested in) called `.ancestor` would be selected