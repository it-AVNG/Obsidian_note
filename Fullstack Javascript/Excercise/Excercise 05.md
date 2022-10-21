# Descendant Combinator

Understanding how combinators work can become a lot easier when you start playing around with them and see what exactly is affected by them versus what isn't.

To apply styles to elements that are descendants of another element, while leaving elements that *aren't* descendants of that element unstyled.

You can use either type or class selectors for this exercise; use whichever you may feel you want to practice with more. The HTML file is set up (so no need to edit anything in it) such that any combination of selectors will work, so if you're feeling adventurous you can even try combining a type *and* class selector for the descendant combinator.

The properties you need to add are:
* Only the `p` elements that are descendants of the `div` element should have a yellow background, red text, a font size of 20px, and center aligned.

### Self Check

- Do the elements that contain the text "This should be styled" have the correct styles applied?

- Do the elements that contain the text "This should be unstyled" have no styles applied?

```html
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta http-equiv="X-UA-Compatible" content="IE=edge">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Descendant Combinator</title>

<link rel="stylesheet" href="style.css">

</head>

<body>

<div class="container">

<p class="text">This should be styled.</p>

</div>

<p class="text">This should be unstyled.</p>

<p class="text">This should be unstyled.</p>

<div class="container">

<p class="text">This should be styled.</p>

<p class="text">This should be styled.</p>

</div>

</body>

</html>
```
