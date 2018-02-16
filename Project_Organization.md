<!-- This file highlights how to structure your projects-->

1. Look up what type of framework/library/module iOS has to help implement your code 
  i.e. for tapping into the user's location - iPhone GPS - use CoreLocation
  
2. When creating your projects, think about how you want the data displayed - this will help you when you create your data models, as well as when you create objects from those models, and create your functions 
  
3. Creating Data Models 
  - First, consider how the data you have gathered (via API or other source) will be displayed on screen (view), then create individual data models (classes) to represent the data you need to access 
  - The models will encaspulate properties >> For exmaple, in the WeatherDataModel you would store properties like, weather condition, temperature and city and you will use the model to update your app 
  - When creating the variables in your method, think about what properties are associated with the data
    i.e. for a music application, some properties would be songType, artistName, albumName, albumTitle
    i.e. for the Weather application example (lecture 152) the properties would be temperature, condition, city, weatherIconName
  - Once you have determined the properties > you can create your variables based on those properties
    i.e. for songType property >> let songType : String = "" > would start out with an empty string 
    i.e. for temperature property >> let temp : Int = 0 >> 0 would be the starting value
  - After the data model(s) are created, add them to your ViewController class by initializing a new object and storing that object into an instance variable 
    ** REMEMBER: Data models are just like "classes" in Ruby > you can initialize a new instance of the class/data model object, by creating an instance variable or instance of that object 
      Ex: class MusicLibrary > new instance would be let newMusic = MusicLibrary()
  - *** REMEMBER: to access class/data model properties in Swift, we use dot notation
      Ex: newMusic.songType or weatherData.temperature
  - Depending on how you want your data displayed on the screen, you will set the instance variable + property to the data you want to present on screen 
      Ex: func displayProducts(json: JSON){
            let coatInventory = json["main"]["coats"]
            productInventoryModel.coats = coatInventory
            productInventoryModel.dresses = json["main"]["dressName"] >> this would pull the value of the json object with key "main" with key "dressName" 
            productInventoryModel.shoes = json["main"]["shoes"][0]["id"].intValue >> this would pull the value of the json object within the key "main" with key "shoes" at index 0 with the key "id"
            }
  - When working with data that includes id numbers, i.e. id 702 - dress, id 702 coat, use a switch statement for your control flow
    - set the switch expression to the variable for id number, then adjust each case for a different return value, based on the id number 
      Ex: function newDesignerIcon(designer: String) -> String {
            switch(designer) {
              case 0...10 : 
               return "michael_kors" >> the string references an image, without the ".png" file type 
              case 11...20 : 
                return "michael_costello"
              case 21...30 :
                return "prada"
              case 31...40 :
                return "tadashi_shoji"
              case 41...50 :
                return "christian_siriano"
    
            }
      
          } 
  
4. When creating methods to update your UI (View) 
   - ***REMEMBER: labels are of String data type - so if you are retrieving data from one of your data models that is not of String data type, you will have to convert it 
    Ex: temperatureLabel.text = Str(weatherDataModel.temperature)
    
    
5. XCode API 
   - Public Methods: any class can call any of the methods in any of the classes we created **You DO NOT want to make ALL of your methods PUBLIC >> this can crash your app if the wrong class accesses a function/method that should not be called by that class 
   - Private Methods: NO other classes can call private methods 
      - this is implemented by adding the keyword "private" before the function or var keyword
        Ex: private var fashionDesigner = "Zac Posen"
            private func dressType(silhouette: String){
              print("The \(silouette) is by (fashionDesigner).")
            }
            
6. Auto Indent or Indent Multiple lines 
  - Control + I > the control key, then the i 
      
      
      
      
      
      
      
      
      
      
      
      
      
      
      
      
      
      
      
      
      
      
      
      