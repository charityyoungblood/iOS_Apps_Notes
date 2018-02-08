<!-- Networking - the communication between different computers on network  -->

1. Computer Networking - to facilitate the communication between our app and the specified API's servers

2. HTTP Request 
  - When your browser tries to fetch something from a website, i.e. an image, it's making an HTTP request 
  - It sends the request to the website's servers that host that image and that server responds with a file, which then gets displayed in the browser 
  - Browsers are able to manage these requests and responses 
  - When making networking calls, you have to provide a URL, which serves as an address in the data server - it tells that data server the location of the files that you want to access 
  - Cocoapods >> Alamofire - this is a library of code that will help you make the HTTP requests and simplifying a lot of the networking calls for us
  - this library enables us to make a request with only a few lines of code, instead of having to worry about what to do if the server times out, or if there are connection issues - that is all handled by Alamofire 
  - To make an HTTP Request using Alamofire:
    - place "import Alamofire" at top of class, under "import UIKit"
    - create a "Networking" function (i.e. func getWeatherData(), func getLocationData())
    - depending on function type, enter necessary parameters (i.e. for getWeatherData(url: String, parameters: params))
    - in order to deal with the HTTP request you need to have some sort of response handling, i.e. what you do after request is made 
      Ex. in Alamofire documentation > Usage > Making a Request - the import line goes at the top of your code file above the class declaration, the Alamofire.request line of code, goes into your func getWeatherData or getlocationData (see iOS Course: lecture 150) > Response Handling
    - Alamofire is "asynchronous" meaning it runs in the background 
    
3. When making HTTP Requests there are many different methods you can use. A few of the most common are: 
    - GET Request: think of the Cookie Monster - "Give me cookies" - i.e. "fetch me data" from the Web Server
    - POST Request: think of the "Postman" - this is where you pass data to the server and add data to that server 
    - DELETE Request: think of Oscar the Grouch - you make a request to the server in order to delete some data that is in the server
    