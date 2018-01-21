1. When creating functions, you have to declare data types in Swift 

  // create a function that takes in parameters: weight, height - return BMI
  // BMI is calculated as mass(kg)/(height(m)) * height(m) - height squared

    func calculateBMI(height: Int, weight: Int) -> Int {
    let bmi = weight/(height * height)
    return bmi
        }

    calculateBMI(height: 4, weight: 73)
