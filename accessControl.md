<!-- Examples of Access Control --> 

- When you are the ONLY programmer working on a project, it doesn't necessarily matter if you have classes and methods that are accessible to all of your code 

- When you work on LARGE TEAMS - i.e. Tory Burch or Neiman Marcus - your tasks will probably be grouped into certain departments, i.e. UI Elements, Game Design, etc 

- In cases like this, you DO NOT want the other team accessing every part of your code, ESPECIALLY if something is changed that affects your application and now your application is crashing 

- You want to be able to PROTECT the internal implementation of data structures 

- To make it CLEAR exactly WHICH METHODSCODE is accessible to other teams, we use ACCESS CONTROL 

- Access Control 
  - Using KEYWORDS that we will put into our API, onto our methods and variables, that says to other GROUPS that we are programming with "Yes, you ARE allowed to call this method. I promise not to break anything!" 
  - Access Control also tells them how to use your methods and variables, as the ones that they are allowed to call, are the ones that are available to them 
  
- Swift supports the following keywords (for Access Control): 

  - internal: this is the "default" - any var or function, etc that has this keyword before it is usable by any object in the app or framework 
    - since "internal" is the access control default, we don't have to type this keyword in - all variables, methods, etc are AUTOMATICALLY "internal" 
    
  - private: means it's internal implementation to this object, NO OTHER objects can call it - this will keep other programmers from accessing that code 
  
  