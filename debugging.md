<!-- Debugging in XCode --> 

1. Command + Shift + y - to show debugger 

2. First place we check for explanation of errors is the "stack trace" located in the debugger console (bottom right)
    - Scroll up at the top > can place exact error into Google, if you are unsure what they error code is referring to 
    
3. If our application is crashing at a PARTICULAR point in our app - we'll want to implement "BREAKPOINTS" - this is similar to rspec in Ruby - it will break down the code at the stopping point 

4. In the Debugger Console after the (lldb) type "po"  or "p" (for print out, and print) + variable/class name to see information about that particular item 
    Ex: po game 
        p game 
        
5. Connections Inspector: When you receieve a "key value compliant" error - be sure to look in your connections inpector first - check for spelling errors and what methods/variables are connected via IBOutlet and/or IBAction 