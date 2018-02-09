<!-- This file highlights how to structure your projects-->

1. Look up what type of framework/library/module iOS has to help implement your code 
  i.e. for tapping into the user's location - iPhone GPS - use CoreLocation
  
2. Creating Data Models 
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

