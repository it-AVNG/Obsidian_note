for Excercise_03 disered outcome:
![desiredoutcome Excercise 03][Excercise_3.png]
Requirement:
added multiple classes to a single element in order to apply two different rules to it.
give two elements each a unique class name, then add rules for styles that both elements share as well as their own unique styles
* **The first element**: a black background and white text
* **The second element**: a yellow background
* **Both elements**: a font size of 28px and a list of fonts containing `Helvetica` and `Times New Roman`, with `sans-serif` as a fallback.  

### Self Check

- Does each element have a unique class name?
- Did you use the grouping selector for styles that both elements share?
- Did you make separate rules for the styles unique to each element?

## Solution
```html

<!DOCTYPE html>

<html>

<head>

<meta charset="UTF-8">

<meta http-equiv="X-UA-Compatible" content="IE=edge">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<link rel="stylesheet" href="./style.css">

<title>Group Selectors</title>

</head>

<body>

<button class="left">Click Me!</button>

<button class="right">No, Click Me!</button>

  

</body>

  

</html>
```

Stylesheet
```css
.left,
.right{

font-size: 28px;

font-family: "Helvetica","Times New Roman", sans-serif;

font-weight: bold;

}

.left{

background-color: black;

color: white;

}

.right{

background-color: yellow;

}
```

