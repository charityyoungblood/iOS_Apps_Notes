1. When creating functions, you have to declare data types in Swift 

  // create a function that takes in parameters: weight, height - return BMI
  // BMI is calculated as mass(kg)/(height(m)) * height(m) - height squared

    func calculateBMI(height: Int, weight: Int) -> Int {
    let bmi = weight/(height * height)
    return bmi
        }

    calculateBMI(height: 4, weight: 73)
    
2. In order for function to run, you have to enter all information including return value data type, and explicity use return keyword 

    Ex: //create a function that prints out all of the Fibonacci numbers, in sequence, until the user input is reached

    func fibonacci(userInput: Int) -> Int {
    var fibonnaciStart = 0
    var fibonnaciNext = fibonnaciStart + 1
    return fibonnaciStart + fibonnaciNext
      }

    fibonacci(userInput: 5)
    
3. Tags in Storyboards - tags are useful when you are grouping data (i.e. buttons)

    - tag is a property that you can "call" on the button object
    
4. To add a file in Swift, select folder > right click > select "new file" > make sure group is the correct folder, target should be the current project 

5. Methods vs Functions
  - when a method is created "inside" of a class (class body) it is called a "method" (i.e. if it's within the curly braces/body of a class it's considered a method)
  - when a method is created "outside" of a class (outside of the class body) it is called a function 
  
6. In Swift Objects have:
 - Properties - set or initialize the properties
 - actions - what should happen in respond to events 
 - events - how should the object act in certain events (onStart, shake, etc) 
 
8. Properties vs Variables/Constants
  - when constants or variables are created inside of a class, they are called properties 
  - when constants or variables are created outside of a class, they are referred to as constants and variables

9. GPS/Location Services 
  - when setting latitude and longitude variables, XCode may request those values as "Strings"
  - to change to String, add String keyword, and place code within parentheses: 
     Ex.  let latitude = String(accurateLocation.coordinate.latitude)

10. What is Delegation? 
  - allows the built in Apple classes (i.e. CoreLocation) to access properties and send data to our ViewController, or designated delegate classes
  - the delegation pattern is similar to if your ViewController was raising it's hand saying "Hi, I'll be the delegate! I'll handle the data that comes through the locationManager"
  
11. Swift Dictionaries 
  - modeled by real-life dictionaries, where you have a word and an associated meaning 
  - in Programming, we use dictionaries to associate a key with its value, so that any value can be identified as long as you know the key 
      Ex. var fashion = ["Zac Posen" : "Fashion Designer"]
  - ** Remember, when you create a dictionary, you can put in any number of key-value pairs - as long as they have the SAME data type 
      Ex. Dictionary data types of [String : String] 
      or Dictionary [String : Int] 
      ** the data entered has to match the data types ** 
  - In Swift, you can explicity state the data types in your dictionary, or let Swift infer
      Ex. var bridalFashion = ["Berta" : "Bridal Fashion Designer"]
        or var bridalFashion : [String : String] = ["Berta" : "Bridal Fashion Designer"]
  - Dictionaries have to have unique keys, but can have the same value
      Ex. var fashionDesigners = ["Zac Posen" : "Fashion Designer", "Noon by Noor" : "Fashion Designer"]
  _ ** Remember, to access the values by key, use the variable name and bracket notation of the key name
      Ex. var fashionDesigners : [String : String] = ["Zac Posen" : "Fashion Designer", "Noon by Noor" : "Fashion Designer"]
      access value by using variable name[key] >> fashionDesigners["Zac Posen"] >> will return "Fashion Designer"
      
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  