<!-- JSON - JavaScript Object Notation --> 

1. JSON is used in many programming applications, not just JavaScript, because it is a way of formatting large pieces of data that gets passed around on the internet 

2. JSON is also a data type in Swift 
  - when using JSON, set a constant with type JSON
  - EX. let weatherJSON : JSON = JSON(response.result.value) >> refer to iOS course: Lecture 152  
  - ** REMEMBER: to test your app, include a print statement, i.e. print(longitude) or print("Success!") so you can make sure the code is doing what it is supposed to do - getting to the right lines of the code 
  
3. After you send the HTTP request (Ex: Alamofire.request)
  - create a constant > store the HTTP response value in this constant > inside the response, we want to tap into the result > the result has a few associated properties, we want the value
    Ex: let weatherJSON : JSON = JSON(response.result.value) - ***REMEMEBR to convert data types, place data type (i.e. String, Int, JSON) then the value to convert, into parentheses