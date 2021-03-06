** TO CHANGE THE NAME OF VARIABLES/PROPERTIES: Click on property/variable name > right click while holding "Command" key > Select "rename" > rename variable/property 

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
      Ex. var fashion = ["Zac Posen" : "Fashion Designer"] >> Here "Zac Posen" is the "key" and "Fashion Designer" is the "value" 
      
  - ***REMEMBER, when you create a dictionary, you can put in any number of key-value pairs - as long as they have the SAME data type 
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
      
  - Arrays and Dictionaries are known as "Collection Types" and they help you to organize data 
  - If you have data that is sequential in nature, then you're going to want to organize that data into an Array
  - If you have data that is NOT sequential, then you'll use a Dictionary (key-value pair structure)
  - When structuring a Dictionary, remember the RETURN value will be OPTIONAL - since what we are looking up MAY NOT be in the Dictionary (iOS Stanford: Lecture 2 @52:30)
  
12. What are API's? 
  - Application Programming Interfaces 
  - It is essentially a contract with rules that your app must follow in order to get the data from the website's server 
  - These rules are pre-written and specified on the API's documentation - they include the things you need to provide, so that the API can deliver you
  - You don't HAVE to use an API to get info from a website - you can program your app to look for specific information on a website, instead --- THE PROBLEM - is that if that website decided to change it's appearance, your program may not work - it won't know how to parse/interpret the data from that website 
  - API is a "Request" > "Response" system
  
13. Closure - a function within a function > this is also noted by using the keyword "in" 
  - whenever you are inside of a closure and want to call another function, you always have to declare "self" in front of the function call 
    Ex: self.updateWeatherData(json: weatherJSON)
  
14. Converting data types (Type Conversion)
  - use either dot notation or parenthesis to perform type conversion 
    Ex: fashionDesigner.dress = Str(dressResult)
        fashionDesigner.dress = dressResult.stringValue 
        
15. Read Only - Apple Developer Documentation
  - Whenever you see the { get } at the end of a Swift method, or variable declaration, this means it's "read only" 
  - This means you can't change 
    Ex: var currentTitle: String? { get }
     - you can "get" the current title, but you can't set it using this method 
     
16. String Interpolation
  - In Swift, we use \() for string interpolation
  - instead of #{}, like in Ruby or %s, like in C
  - Ex: let fashionDesigner = "Berta Bridal"
        func bestBrialDesigner(){
          print("The number one bridal designer is \(fashionDesigner)")
        }
        
17. Optionals(?)
  - In Swift, there is a type, like Int or Bool, called Optional
  - This "Optional" type can only have two values:
      - not set: which is expressed with the keyword "nil" > meaning, "this Optional is not set"  - there is no associated value because the value is not set 
      - set: if the Optional is in "set" state, it can have an associated value, which can be of any other type - including Optional, i.e. you can have an "Optional Optional"
  - Optionals have a ? on the end of the type 
      Ex: var currentTitle: String? { get }
  - Optionals have an INITIAL value of "not set" or nil, which can of course be changed in your code/logic when writing your program
      
18. Forced Unwrapping(!)
  - This is done to "force unwrap" an optional value's value 
  - Use this with caution
  - ONLY use this on Optional values, whose value is NOT "not set", i.e. the value is not, or will not be "nil"
  
19. Communication between Classes (Objects)
  - **REMEMBER: the way classes "speak" to each other, is by creating a variable equal to an instance of the class you want to communicate with 
    Ex: var bestDesigner : String = BestDesigner()
    
20. Dictinoary
  - In Swift, a Dictionary is a type
  - It is a GENERIC type > when you declare your Dictionary, you SPECIFY what TYPE the key:value pairs are 
    - Ex: Dictionary syntax: var keyword, data type followed by <key,value> = [code]
          var dresses: Dictionary<String,String> = [
                "mermaid":"type of silhouette", 
                "size":"size of dress"
              ]
  - To access data in a Dictionary, use bracket notation 
    Ex: dresses["mermaid"] would return "type of silhouette"
    
21. Enum 
  - Is a data structure 
  - Has to have discrete values - meaning it can only take integer values
  - Enums are similar to classes, as they can have methods (within the enum declaration)
    Ex: enum DressSizes {
        case FirstSize
        case SecondSize
        case ThirdsSize
        
        func newCoatSize() {
          code 
        }
    }
 
 - Enums can ONLY have COMPUTED PROPERTIES (not stored variables) - as the cases are the "stored" values 
 - Enums CANNOT have inheritance > you cannot have an enum that inherits from another enum 
 - Enums are passed by VALUE  
 
 22. Struct 
  - Is a data structure 
  - It is very much like a class, ALMOST identical 
  - It can have variables, both STORED and COMPUTED PROPERTY
  - Struct CANNOT have inheritance 
  - Struct, like Enum, are passed by VALUE - where as classes are passed by REFERENCE
    - passing something by REFERENCE means that that thing lives in the heap (memory) and when you pass it around to a method, you are essentially passing a "pointer" to it, not the ACTUAL thing
    - passing by VALUE, means you are COPYING it 
  - You do not have to set the variables you initialize in Struct to anything, unlike class 
  
23. Closures 
  - An inline function that captures the state of its environment
  - Explanation at 1:08:57 in iOS Stanford Course - Lesson 2 
  
24. For Loops in Swift 
  - They do not use variable i for a counter and increment 
  - For loop Syntax 
    Ex: for dress in allDresses {
        dress.backgroundColor = white // colorLiteral represented in Swift by name or chart by entering "color" > color Literal
    }
    
  - You can use a For loop in Swift on anything that has a SEQUENCE -- this includes:
    - Arrays 
    - Strings 
    - Countable Range: displayed with starting index .. (for 0 start) or ... (for "including" the last index) until (including or not including) end index 
        Ex: for identifier in 0..< numberOfPairsOfCards {
            let card = Card(identifier: identifier) 
        }  
  
25. "lazy" var 
  - Since you have to initialize a variable before doing any operation on it in Swift, 
  - if you make a "lazy var" - it will not initialize UNTIL someone uses it 
  - lazy var CANNOT have a didSet {} property observer 
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  