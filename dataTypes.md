<!-- Data Types in Swift --> 

1. Swift is an EXTREMELY strongly TYPED language - in most cases, you want to be VERY specific about what data types you are using 

2. Swift also has STRONG TYPE INFERENCE - in most cases, if it can, it will guess the type for you 

3. Array is a GENERIC CLASS in Swift - this means you can't have the class "array" on it's on listed as a TYPE in Swift 
  - When you create an array, you have to specifiy what type of data is in the array so that Swift can breathe easy 
  - Since arrays are so common in Swift, their syntax doesn't include the name of the type, just the data enclosed in square brackets
      Ex: var cardButtons: [UIButton]!
      
4. Countable Range (Floating Point Numbers) - is a GENERIC type (like Array is a GENERIC type)
  - When you are creating a for loop with Floating Points (decimals) for a "Countable Range" in Swift 
    - We have to use the global function "STRIDE" 
      Ex: for i in stride(from: 0.5, through: 15.25, by: 0.3) {
        
      }
  - stride has "from", "to" and "by" - it can count over indexes, etc. - and knows how to create a Countable Range 
  
5. Tuple - data structure
  - Is a "grouping" of values 
  - You can use it anywhere you can use a type 
  - Mini struct that has no vars or values
    Ex: let x: (String, Int, Double) = ("hello", 5, 0.85) >> the "type" of x is a TUPLE
        let (word, number, value) = x (this names the tuple elements when ACCESSING the tuple)
        print(word) >> will print hello
        print(number) >> will print 5
        print(value) >> will print 0.85
  - The names of the variables in a tuple is very flexible, either when you define it or after you define it, as in the case of the example above 
  - What is a Tuple good for?
    - It can be used any time you want to group stuff together that is really lightweight 
    - Tuples are VERY GOOD for returning multiple values from a function 
    
6. Computed Properties 
  - All the properties we have in the Concentration game were "stored properties" - i.e. normal variable declarations Ex: var fashion: String = "Zac Posen"
  - In a "Computed Property" the value is not "stored" - it is "set" with code and "get" 
  
    Ex: var fashion: String = "Zac Posen" {
      get {
        // the code you place here, everytime someone asks for the value of var fashion, it gets calculated inside "get"
      }
      
      set {
        // every time someone "sets" the value for var fashion, the code inside "set" gets executed 
      }
    }
    
  ***REMEMBER: you DO NOT have to create a "set" value for your Computed Properties. If you don't they will become "Read Only" Properties***
  
  - What are Computed Properties Used For? 
    - A lot of times you have something that is perceived as a property, of your struct or class, that is actually derived from other state
    - When this happens, you do NOT want to have a stored property, because you don't want to have the same information in two different variables  
    - For Example, in the Concentration game we can "derive" this variable easily from looking at the cards: 
        var indexOfOneAndOnlyFaceUpCard: Int? 
      - It would be BETTER to change this variable to a computed property, where we could assign a "get" value for when the game looked at all the cards to see which one, or if there is one face up 
      - If so, return the card, else, return nil 
        Ex: var indexOfOneAndOnlyFaceUpCard: Int? {
          get {
            // looks at all the cards and see if there is one, and ONLY one, that is face up
            // if so, return it, else return nil 
          }
          
          set {
            // turn all the cards face down except the cards at index newValue 
          }
        }
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
    