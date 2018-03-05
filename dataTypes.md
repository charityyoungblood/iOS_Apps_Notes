<!-- Data Types in Swift --> 

1. Swift is an EXTREMELY strongly TYPED language - in most cases, you want to be VERY specific about what data types you are using 

2. Swift also has STRONG TYPE INFERENCE - in most cases, if it can, it will guess the type for you 

3. Array is a GENERIC CLASS in Swift - this means you can't have the class "array" on it's on listed as a TYPE in Swift 
  - When you create an array, you have to specifiy what type of data is in the array so that Swift can breathe easy 
  - Since arrays are so common in Swift, their syntax doesn't include the name of the type, just the data enclosed in square brackets
      Ex: var cardButtons: [UIButton]!