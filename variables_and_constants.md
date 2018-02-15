1. In Playground - you can see all of your variable values on the right side panel in playground 

2. In order to interpolate strings with integers - you'll need to use the escape character 
    - i.e. "\(myName), \(myAge)" would print Charity, 34

3. Image names should be listed as strings

4. In Swift, any time you declare a local variable or property, that is initialized at the beginning and never changes - i.e. it's a constant, use "let" keyword instead of "var" 
  - We do this for two reasons:
    - This helps when others are reading your code to recognize that variable/property will never change, it's a constant 
    
    - If that variable or property was an array or a dictionary, and you use the "let" keyword, that means nothing can be put into that dictionary or array or taken out - this is how you would create "read only" arrays and dictionaries 
    
5. Computed Variables/Property and Stored Variables/Properties 
  - Computed Variable/Property: when we need to create a variable that "tracks" a part of our app (i.e. in the Calculator app we needed to track if the value was a Double), we create this type of variable
    - Inside the curly braces, we place code to "calculate" the value, both when we "set" the variable and when we "get" (retrieve) the variable
    - We create a "set" value: for when someone tries to "set" the value
    - We create a "get" value: for when someone tries to "get" the value 
    - If you need to create a variable that is "read only", i.e. you don't want it to change, use only the "get" portion
      Ex: var bestFashion: String {
          get {
            return "Michael Costello"
          }
          
          set {
            display.text = "Michael Kors"
          }
      }