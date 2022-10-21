When a class is defined by CSS, the selecter style definition that comes after, overwirte the seting of the previouse rules. Because CSS reads from top to botttom. What is written at the bottom will over write the top.


When 2 type of Selectors point to one element, the one that has more specificity will be chosen.

`Id` is more specifica that classes. CSS take ALL selectors and it specificity then comapare them. 

CSS paradigm of specificity as follow, from left to right, decreading specificity.
> [inline style],[ID],[Classes],[Elements]

For example, the below index. html has the folowing set
```html
<h1 id="header-id" class="header">Header</h1>
```
The element `h1` has 1 ID, 1 class , 0 property element. In CSS we write
```css
.header{
color:red;
}

h1{
color:blue;
}
```

the color `red` will be chosen since header has higher specificity.

Every selectors for elements like `div, h1, p` will has lower specification than classes and IDs.

In case of same specificity, CSS will add to the paradigm for any additional specificity it can find then select the higher one to apply.

Ancestry and inheritent doesn't have contribution to specificity.
We can add `!important` overwrite every thing comes before. Don't do this in general, unless you want to have a quick fix.

