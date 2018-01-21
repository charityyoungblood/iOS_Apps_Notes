<!-- Terms -->

1. IBOutlet - changes the appearance of the UI element (i.e. image)
2. IBAction - this notifies the code when the UI element is interacted with 
3. ImageView - (label) can only change the appearance of this element - only has outlets
4. Button - you can change both the appearance and notify the code when it is pressed/tapped - buttons have both outlets and actions

<!-- Most Common Errors with IBAction and IBOutlet --> 

**When you have misspelled a variable name - you cannot click on the variable name inside the center pane** 
 Error message for misspelled variable would be similar to: "terminating app due to uncaught exception 'NSUnknownKeyException'" 
 
 - The first thing you have to do, is break the connection between the imageView 
  - select image > right click > you'll see a pop up window with variable name on top
  - under referencing outlets > click on the connection to break it
  - now when you look at outlets, there should be one less than before 
  - then click on image, hold control and drag to ViewController code 
  
  <!-- Test Your Code -->
  
  - as you are coding - rememeber to run your program and test if the app is doing what you think it's doing
  (i.e. add a print statement)