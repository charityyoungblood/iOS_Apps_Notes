<!-- Auto Layout - how to make your app look beautiful on every screen size --> 

There are two ways to make sure your app will display the same on any screen size 

  1. Programmatically 
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
  2. Using Auto Layout   