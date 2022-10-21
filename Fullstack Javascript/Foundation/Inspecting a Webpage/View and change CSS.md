# Viewing an element's CSS
+ In CSS, a unit called `em` means referencing to the current font size. If the font size is at 11px, 1em=11px

# Add a css declaration to an element 
+ After inspect an element, in the styles pane, we add into `element.syles` our modification
+ The modification will shows as inline styles CSS in HTML file

# Add a CSS class to an element
+ In the Styles pane, `.cls` help us adding a class to our node without need to jump to HTML to do so

# Add a pseudostate to a class
+ Use the `.hov` to add a pseudostate to a class to see the change as if the state has been activated
+ Use HTML method (right click>Force State> :hover) as alternative

# change the dimensions of an element
+ Box model intteractive diagram in the Style pane to change the width, height, padding, margin, or border length
![box model ][Boxmodel.png]
+ With rulers we cna measure our elements dimensions accurately. Ruler can be access via typing `show ruler on hover` in command menu
+ Search for nodes by select the elements tab and ctrl-F

# Edit element using HTML mode
+ Right click on the element and select edit in HTML, hit enter and type the replacement, after wards, use Ctrl-ENTER to log in the change
+ To hide a node, press H (for inspecting purposes)

# Access nodes in the Console

DevTools provides a few shortcuts for accessing DOM nodes from the Console, or getting JavaScript references to them.

# Reference the currently-selected node with $0

When you inspect a node, the `== $0` text next to the node means that you can reference this node in the Console with the variable `$0`.
+ Type `$0` and press the Enter key. The result of the expression shows that `$0` evaluates to `<li>The Left Hand of Darkness</li>` 

# Store as global variable

If you need to refer back to a node many times, store it as a global variable.
+ Right-click elements in the DOM Tree and select **Store as global variable**. it will be store as `temp`

# Copy JS path
Copy the JavaScript path to a node when you need reference it in an automate test by right click on the DOM>copy>copy JS path

# Using CSS overview to inspect the overall information of the website
In the CSS overview, after capture the webpage, we can Identify  improvement points
