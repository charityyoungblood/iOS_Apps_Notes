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
        - one of the ways the View talks to the Controller is via target - action 
            - The Controller hangs a target on itself, by defining a method with @IBAction
            - When the View wants to talk to the Controller, it calls the method that was defined with @IBAction 
        - another example of when the View talks TO the Controller is if there are other more complex actions, i.e. scrollView or zoom
            - In this case, the View may need to tell the Controller that the user just started "scrolling" or the user is zooming in to a new zoom scale 
            - The Controller would need to be notified of those actions because the Controller may need to "react" to those actions 
        - another example of when the View talks TO the Controller, is when the View asks the Controller if it should allow something to happen (i.e. "should I allow vertical scrolling right now?") - this is accomplished with delegation
          - the View will send messages with words like "should", "did" and "will" - these questions are asked via a delegate 
    - The Controller sets itself as the View's delegate 
          - a delegate is set via protocol 
          - a protocol is a description of a bunch of methods that the other guy promises to implement 
          - "data source" property on the View 
    - The View does NOT own the data it's displaying > to access the data, the View asks the Controller 
    - The Controller's job can be described as interpreting and formatting the Model data for the View
    - The Model NEVER talks directly TO the Controller - because the Controller is the UI logic and the Model is UI independent, so there's no way the model would have anything to say to the Controller 
    - If the Model has data that CHANGES, i.e. the Model is receiving data from a network, the Model sets up a "radio station" (Notification & KVO) Model to let the Controller ACCESS the data it needs, i.e. the Controller "tunes in" to the station
      - all info on the radio station has nothing to do with the UI only with the data 
    - On a large application, there are MULTIPLE MVC's working together to form one application - when multiple MVC's are connected, one MVC can only serve as the View to another MVC
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
            
    

