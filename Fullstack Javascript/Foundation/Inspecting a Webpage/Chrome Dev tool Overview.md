# Debug CSS
+ Right click inspect to highlight the element in the DOM tree
+ To adjust dev tool **placement** command menu: **crtl-shift-P** and type bottom or top
+ in ***Command menu*** we can type 'undock' to undock the tool
+ in the ***Styles pane*** there are multiple style sheet, each one has declared background color gives us the idea of casscade order prolems 
+ ***Computed pane*** tell us what declaration/properties ar being applied in addition to each the final value of each property. In the drop down of the properties, we can see the cascade order for each particular properties
+ ==**we can only debug one element of CSS at a time*== 
+ Click top left icon or **crtl-shift-C** to select ***hover tool***. hover mouse to highlight elements to inspect
+ DOM tree has a search UI 
	+ Crtl-F for search when we focus on the DOM tree
	+ search by string, CSS selector, or XPath
	>*Note to self: Look up XPath method for XML query search*
+ ***Console***: inspect(element_to_inspect) will hightlight the element in the DOM tree
+ Highlighted element will give a commonly use element information of the element
+ ***Animation tab*** will help us with CSS debugging tool
	+ Open the ***Command Menu*** the type *animations*, the animation will 'listen' to the trigger animation adn we can adjust and change the animation
	+ The animation will also highlighted the elements so we can keep track 
+ **Rendering tab*** can aslo be accessed via the Command menu, we enable paint flashing and we reload a highlighted element while doing the animations means the browser has to paint the element inorder to do the animation --> room for improvement

# Prototyping CSS
+ When we reloading CSS to check code, is tidious. 
+ In the dev tool, when we adjust, the inspectin element will change instantly instead of reloading the page
+ Auto completing by value with dev tool will increase the speed of of typing
+ *Shift-up_arrow* will increment the highlighted value
+ **Pseudo-classes** in the Syles pane, click the `:hov` button to assign a special state like *hover, focus, visited* 
+ Applying and removing classes in the Styles pane and click `.cls` button and typing the classes that we have available in the HTML
+ **Detour: Darktheme** we can change the theme of the DEVtool to dark theme via command menu
+ *Automatic syncing* it is automatic sync with the browser/system setting
+ **Contrast ratio** while inspecting an Element, find the element `color` value declaration, click the small box next to the color declaration to expand and see the Contrast ratio section
+ **Copy Element Styles** after prototyping the element, we can copy the prototyping to our code via right-click>Copy>Copy Styles and return and higlight the element that we would like to change, we paste the copied styles to our clip board. Carefull off what you copy, only do this when you understand enough of the stuff
+ **Screenshots** command menu and type capture screen shot/Fullsize screenshot/area screenshot/Node screenshoot

# Debugging Javascript
+ Common problems checking: Excecuting order and value sets correct
+ Strategy: Logging and debugging with source panel.
+ Shortcut: Contrl+Shift+J to jumps into the Console
+ Open console in Drawer: Escape

+ Basic logging
	+ Basic `console.log(pets)` : Logging the value of an array and print out the value of the array object
	+ `console.log({pets})` : Printout the name of the variable and followed by its value
	+ `console.table(pets)` : print out a table
	+ `console.trace('how is this')` : to get a call stack trace

> Debugging with source panel: 
> + Better suited with tricky bug
> + Keeping track of code execution order
> 	+ Code stepping
> 	+ Call stack
> 	+ code folding

+ Keeping track of value
	+ Values printed inline after a line of code executes
	+ Scope pane will update the output of the code
	+ Run Javascript contextually in the Drawer
	+ live expressions
	+ Log Points (right click and add using the GUI)
	+ storing Log point output as global variables
	+ adding `debugger;` in your script

+ Breakpoinsts
	+ DOM muatation break points
		+ rightclick -> break on attribute adjustment 
	+ event listener break points
		+ Blackboxing frame scripts
	+ [break points guide](https://developer.chrome.com/docs/devtools/)

+ Analysis load performance
	+ Start with Audits panel access via command menu
	+ further analyzing with Coverage tabs, Performance panel, Network panel
	-   **Audits** panel > **Run Audits**
	-   Different **Metrics** to measure different aspects of the load experience
	-   **Opportunities** are the specific suggestions on how to improve
	-   **Diagnostics** also provide helpful points but are more abstract

# What is a DOM
+ D.O.M Document object model is a programming interface that allows us to create, change, or remove elements from the document
+ in HTML document,DOM views an as a tree of nodes. A node represents an HTML element
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>DOM tree structure</title>
  </head>
  <body>
    <h1>DOM tree structure</h1>
	<h2>Learn about the DOM</h2>
  </body>
</html>
```
+ Our root node is our document that has 1 child node that is our `<html>` element.
+ The `<html>` element has 2 children nodes`<head>` and `<body>` 










