<!-- What's in iOS --> 

1. Components of iOS
  - Core OS: hardware - iPhone runs a version of UNIX  
  - Core Services: Object oriented services on top of Core OS 
  - Media: Multimedia 
  - Cocoa Touch: Object Oriented API for building user interfaces  

2. XCode

  - The "use core data" option that is listed when creating a new project is referring to implementation of databases 
  - for a list of shortcut keys, click on Xcode at top right of screen > Preferences > Key Bindings 
  - Assets: media files 
  - Modules: UIKit, other Apple Modules that come with Swift 
  - When calling a function, remember the first argument/parameter is the variable name, the second has to include the keyword/name of the argument 
    Ex: self.pradaDress(dressButton, dressCost: 2000)
  - To connect multiple buttons, use the drag and select method 


3. MVC
  - Model - the model is what controls the data; it manipulates the data and prepares the data to be served up to the View Controller; the model deals with WHAT your application does 
  - View 
    - think of the View as your Controller's minions :) 
    - the View includes things that the Controller is going to use to put things on screen 
    - this includes buttons, labels, text or images 
  - Controller - this is what goes on behind the scenes
    - the Controller is HOW your model is presented to the user, and includes the UI logic 
    - the code that controls what should happen when the user taps a button 
    - also includes the code that controls what should happend when you have a piece of data to display on screen 
  - Communication Between Model, View and Controller 
    - Controllers can always talk directly TO their Model 
    - Controllers know everything about the Model, it can send any message it wants to the Model 
    - Controllers are in complete control of the Model 
    - Controllers can always talk directly TO the View 
    - The connection between the Controller and the View is via IBOutlet(s)
    - The Model and View NEVER speak to each other, because the Model is UI independent. Since the View is completely UI dependent, there's no need for communication between the Model and View
    - There is limited communication FROM the View to the Controller 
    - The communication FROM the View TO the Controller is blind and structured: 
        - blind: since the objects in the View don't know what class they are talking to 
        - structured: since there is no knowledge of the objects on either end, they have to communicate in a well defined/pre-defined way  
    

