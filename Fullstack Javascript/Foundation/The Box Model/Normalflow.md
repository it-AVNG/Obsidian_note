Normal flow refer to the model that website element lay themselves out if no specifification is provided. 
Normal flow helps documents to be readable even on a very limitted device

## How elements laid out by default
+ THe process begins as boxes of indivifual elements are laid out in box model.
+ ==A block level element content fills the available inline space of the parent element containing it and grows along the block dimension to accommodate its content==
+ Size of `inline element` is the size of its content, we have to convert it using `display` property if we want to manipulate inline element dimension.
+ By default, block level element laid out in *block flow direction* dictate by *writing mode* specified by the html (by default is horizontal-tb) [writing mode](obsidian://open?vault=Fullstack%20Javascript&file=Foundation%2FThe%20Box%20Model%2FWriting%20mode)
+ Each element will appear in a new line, sperated by the margin that has been specified
+ Inline element doesnt appear on a new line, they will sits on the same line as the adjacent text as long as there are space.
+ 
