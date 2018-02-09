<!-- JSON - JavaScript Object Notation --> 

1. JSON is used in many programming applications, not just JavaScript, because it is a way of formatting large pieces of data that gets passed around on the internet 

2. JSON is also a data type in Swift 
  - when using JSON, set a constant with type JSON
  - EX. let weatherJSON : JSON = JSON(response.result.value) >> refer to iOS course: Lecture 152  
  - ** REMEMBER: to test your app, include a print statement, i.e. print(longitude) or print("Success!") so you can make sure the code is doing what it is supposed to do - getting to the right lines of the code 
  
3. After you send the HTTP request (Ex: Alamofire.request)
  - create a constant > store the HTTP response value in this constant > inside the response, we want to tap into the result > the result has a few associated properties, we want the value
    Ex: let weatherJSON : JSON = JSON(response.result.value!) - ***REMEMEBR to convert data types, place data type (i.e. String, Int, JSON) then the value to convert, into parentheses
  - you can think of "response" - that is, what is received back as a response from the HTTP request, as a "package" 
  - the ! after value is a "forced wrapping" which is ok, as long as you include a function to check for a "successful" response >> this is done here: 
                  Alamofire.request(url, method: .get, parameters: parameters).responseJSON {
                    response in
                      if response.result.isSuccess{
                        print("Success! Got the weather data")
                      
                        let weatherJSON : JSON = JSON(response.result.value!) - ignore grey color, this is NOT a comment
                      }
                      else {
                        print("Error \(response.result.error)")
                        
                      }
                      
                      }
4. To evaluate JSON code, go to www.jsoneditoronline.org
   - this will display the JSON in a more "human readable" way 
   - the system will structure the data into categories, including the number of objects and the key:value pairs 
   - ** for most public API's, the data that you get back is most likely going to be formatted in JSON 

5. The Alamofire method contains a "closure" - which is a function that is within a function
   - Whenever you see the keyword "in" then you know you are inside a closure 

6. When you are parsing JSON, trying to access the values via keys, create a constant to store the values
  - you access the keys with bracket notation []
  - Ex. if you wanted to get the temperature from the Weater Data (lecture 152)
      func updateWeatherData(json : JSON) {
        let tempResult = json["main"]["temp"] >> here you are using type: JSON, then the key "main" and within the key "main", you are looking for the key "temp" 
        - nested keys 
        
      }



















