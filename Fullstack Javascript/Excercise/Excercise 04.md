important to understand how chaining different selectors works than how to actually add the attributes.
We have two images for you to style, each with two class names, where one of the class names is shared. The goal here is to chain the selectors for both elements, so that each have a unique style applied, despite using a shared class selector.

The properties you need to add to each element are:

* Make the element with both the `avatar` and `proportioned` classes 300 pixels wide, then give it a height so that it retains its original square proportions (don't hardcode in a pixel value for the height!).

* Make the element with both the `avatar` and `distorted` classes 200 pixels wide, then make its height twice as big as its width (here you should hardcode in a pixel value).

```html
<!DOCTYPE html>

<html lang="en">
	<head>
		<meta charset="UTF-8">
		<meta name="viewport" width="device-width, initial-scale=1.0" >
		<link rel="stylesheet" href="./style.css">
		<title>Chaining Selectors</title>
	</head>
	
	<body>
<!-- Use the classes BELOW this line -->
		<div>
			<img class="avatar proportioned" src="pexels-katho-mutodo-8434791.jpg" alt="Woman with glasses">
			<img class="avatar distorted" src="pexels-andrea-piacquadio-3777931.jpg" alt="Man with surprised expression">
		</div>
<!-- Use the classes ABOVE this line -->
		<div>
			<img class="original proportioned" src="./pexels-katho-mutodo-8434791.jpg" alt="Woman with glasses">
			<img class="original distorted" src="./pexels-andrea-piacquadio-3777931.jpg" alt="Man with surprised expression">
		</div>
	</body>
</html>

```

```css
.avatar.proportioned {

	width: 300px;
	height: auto;

}

.avatar.distorted{

	width: 200px;
	height: 400px;

}
```