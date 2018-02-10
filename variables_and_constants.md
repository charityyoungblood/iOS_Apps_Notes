1. In Playground - you can see all of your variable values on the right side panel in playground 

2. In order to interpolate strings with integers - you'll need to use the escape character 
    - i.e. "\(myName), \(myAge)" would print Charity, 34

3. Image names should be listed as strings

4. In Swift, any time you declare a local variable or property, that is initialized at the beginning and never changes - i.e. it's a constant, use "let" keyword instead of "var" 
  - We do this for two reasons:
    1. This helps when others are reading your code to recognize that variable/property will never change, it's a constant 
    
    2. If that variable or property was an array or a dictionary, and you use the "let" keyword, that means nothing can be put into that dictionary or array or taken out - this is how you would create "read only" arrays and dictionaries 