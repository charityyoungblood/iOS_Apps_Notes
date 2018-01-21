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
    
3. Tags in Storyboards - tags are useful when you are grouping information 
