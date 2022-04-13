# JS Debugging

 ## Order of Execution

  2. function greetUser() {
     return 'Hello ' + getName();
   }
  3. function getName() {
     let name ='Molly';
     return name;
   }
  1.  let greeting =greetUser();
  4.  alert(greeting);

  1. greeting variable get its value from greetUser() function
  2. greetUser() creates the message by combining the string 'Hello with the result of getName()
  3. getName() returns the name to greetUser()
  2. greetUser() now knows the name, and combines it with the string. It then returns the message to the statement that called it in step 1
  1. the value of the greeting is stored in memeory
  4. the greeting variable is written to an alert box.

  ## Execution Context
    - global - code is in script, but not in a function. only one in any page
    - function - code that is being run with a function
    -eval - executed like cide in an internal function called (eval)

  ## Variable Scope
    - global - a variable that can be used anywhere if its declared outside a function
    - function-level - when a variable is declared within a function. it can only be used in that function

  ## Execution Context & Hoisting
    - when a script enters a new execution context, 2 phases of activity:

    1. Prepare
      - new scope is created
      - variable, function, & arguments are created
      - the value of the 'this' keyword is determined

    2. Execute
      - now it can assign values to variable
      - referebce functions and run their code
      - execute statements
  
    -lexical scope - functiions in JS A.K.A linked to the object they were defined within
      - if variable not found in the current variable it is in, it can look in the parent variable object
      - a function gets its own execution context and variables object
      - when an outer function calls an inner function, the inner function can have a new variables object
    
    - if you are expecting that something in your code may cause an eeror, you can use a set of statements to handle the error
      - when an exception is thrown, the interpreter stops and checks the current exevution context for exception-handling code

    - error objects can help you find where your mistakes are
      contains the following properties:
        name, message, file number, line number

  ## Debugging Workflow

    -where is the problem?
      - try to narrow down the area where the problem seems to be 
        1. look at the error message 
        2. check how far the script is running
        3. use breakpoint where things are going wrong
    
    -what exactly is the problem?
      -try to find the actual line of code that is causing the error
          1. see if the variables around them have the values you would expect them to
          2. break down parts of the code to test smaller pieces
          3. check the # of parameters for a function, or the items in an array

    - testing code in the console is a great way to find issues