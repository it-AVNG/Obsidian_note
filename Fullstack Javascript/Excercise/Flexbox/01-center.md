All you need to do is center the red div inside the blue container.

### Self Check

- Is the red div centered?

- Did you _only_ use flexbox to center it?

```html
<!DOCTYPE html>

<html lang="en">

<head>

<meta charset="UTF-8">

<meta http-equiv="X-UA-Compatible" content="IE=edge">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>CENTER THIS DIV</title>

<link rel="stylesheet" href="style.css">

</head>

<body>

<div class="container">

<div class="box">center this div</div>

</div>

</body>

</html>
```

CSS result

```css
.container {

display: flex;

background: dodgerblue;

border: 4px solid midnightblue;

width: 400px;

height: 300px;

align-items: center;

justify-content: center;

}

  

.box {

background: palevioletred;

font-weight: bold;

text-align: center;

border: 6px solid maroon;

width: 80px;

height: 80px;

/* margin: auto; optional solution*/

}
``` 
