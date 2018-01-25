<!-- Errors in Swift -->

1. Do, Catch and Try 
  - do block - describes what should happen; also includes the "try" keyword 
    Ex: do {
        try audioPlayer = AVAudioPlayer(contentsOf: soundURL!)
    }
  - catch block - describes what should happen if there is an error 
    Ex: catch {
        print(error)
    }