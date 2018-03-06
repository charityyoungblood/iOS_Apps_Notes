<!-- Auto Layout - how to make your app look beautiful on every screen size --> 

There are two ways to make sure your app will display the same on any screen size 

  1. Programmatically 
  
    - Determine the width and the height of the screen
      - x = self.view.frame.width / 2
          // self is the current view controller, current class you are in 
          // view is the background view that covers the entire screen
          // frame is the background view's x, y, width and height values 
          // width 
          // the self.view.frame.width gives us how wide the current screen is and when you divide that by 2, you get the midpoint
      - y = self.view.frame.height / 2
      - width = 100 // example value
      - height = 100 // example value 
      
     ***TO CENTER IMAGE***
     
        let square = UIView(frame: CGRect(x: 0, y: 0, width: 50, height: 50)) // example values
      - x = self.view.frame.width / 2 - square.width / 2
      - y = self.view.frame.height / 2 - square.height / 2 
      
    ** If you only want to change the UIView for a specific screen size (i.e. iPhone 7) follow the steps below***
    
        - In the override func viewDidLoad() or func viewDidLoad() 
        - use UIView class
      
          Ex: override func viewDidLoad() {
              let square = UIView(frame: CGRect(x: 0, y: 0, width: 50, height: 50))
            }
            
        - by default, UIView is transparent - so in order to see it, you'll need to change the background color 
          Ex: override func viewDidLoad() {
             let square = UIView(frame: CGRect(x: 0, y: 0, width: 50, height: 50))
             square.backgroundColor = UIColor.red
             self.view.addSubview(square)
            }
            
    - Remember, when we specify positioning, we are referring to the coordinates of the top left corner of the rectangle or square 
    
  
  2. Using Auto Layout   
    - Pinning - also uses same four properties - x, y, width, height 
    - Aligning 
  
    ** Steps ** 
    
      a. Highlight/select image to be edited 
      
      b. Click on "Add New Contraints button, located on bottom far right of screen, next to where you would enter a search term for UIview or label ( button icon looks like a square between two poles)
      
      c. Deselect "Constrain to margins" - this means, instead of sending constraints to the margin of the screen we want to set it to the edges of the screen 
      
      d. Click on the drop down menu for the number on top > select "View (current distance = some value)"
      
      e. Click on the drop down menu for the number on the bottom > select "View (current distance = some value)"
      
      f. To activate the left and right constraints, click on the bars next to the number on the left and the right 
      
      g. Select "Add 4 constraints" on the bottom to save 
      
  3. Using Labels - labels are "read only" text; they CANNOT be changed by the user 
  
  4. Using Stack View - When you have a set of buttons or "tiles" you want to FIRST, make buttons stick to the edges (no matter the screen size or screen view (landscape or portrait)), SECOND, we want to "group" buttons together - so that when the edges pull the buttons apart, they all share that space
    - Stack View: is a class in iOS; used to group items together (stack) vertically or horizontally 
    - You can place "stacks" on top of "Stacks"
    - To create stack view, > select the items to group > select "imbed in stack" on bottom near the constraints buttons
    - This will show the buttons on top of each other > To add spacing, control drag, to select set of buttons > Command + Option + 4 (for Attributes Inspector) > Select "Spacing" > Use Standard 
    - Under "Distribution" option (above spacing option) > select "Fill Equally"
    
  5. If you get an ERROR while using Stack View > Command + 0 to show Navigator Pane > Control + Option + o (to show Document Outline) > There should be a small yellow circle at top, next to View Controller > Click on yellow circle > XCode will offer hints/help to fix issue 
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
   

