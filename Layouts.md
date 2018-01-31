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