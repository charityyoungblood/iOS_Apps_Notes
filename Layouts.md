<!-- Auto Layout - how to make your app look beautiful on every screen size --> 

There are two ways to make sure your app will display the same on any screen size 

  1. Programmatically 
    - In the override func viewDidLoad() or func viewDidLoad() 
      - use UIView class
      
          Ex: override func viewDidLoad() {
              let square = UIView(frame: CGRect(x: 0, y: 0, width: 50, height: 50))
            }
    
  
  
  
  2. Using Auto Layout 