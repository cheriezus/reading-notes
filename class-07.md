## Domain Modeling
  -modeling is the process of creating a conceptual model in code for a specific problem. 
  - object oriented model- an entity that stores data in properties and encapsulates behaviors in methods

## Tables

-<table> - creates a table
-<tr> - creates new row 
-<td> - the tag used to open and close each cell
-<th> represents heading of column and/or row
- <td colspan="2">Geography</td> - will add an extra column to the cell
-<td rowspan="2">Movie</td>  - will add an extra column to the cell

  - used to distinguish parts of the table
    -<thead> - stores the headings
    -<tbody> - store the body/main content of table
    -<tfoot> footer - will most likely contain different content

## “Functions, Methods, and Objects”

  - constructor notation
  let  hotel = new Object();
      - can be use to add properties and methods to any object 
  let hotel = {}
      - creates and empty object
  
  hotel.name = 'Park';
  hotel['name'] = 'Park';
    - updates value of properties
  
  delete hotel.name;
    - deletes a property
  
  hotel.name = '';
    - clears the value of a property
  
  function Hotel(name, rooms, booked) {
    this.name = name;
    this.rooms = rooms;
    this.booked = booked;
    this.checkAvailability = function() {return this.rooms - this.booked;}
  };
      - this indicates that that property/methid belongs to object that this function creates
      - object constructors can use a function as a template for creating objects when you want several objects to reperesent similar things
    
    let quayHotel = new Hotel('Quay', 40, 25);
          -quayHotel = object
          - new = new keyword
          - Hotel('Quay', 40, 25); = values used in properties of this object

  -this refers to one object
    function windowSize( ) {
      var width = this.innerWidth;
      return [width];
    }

  - when a function is difined inside an object, it becomes a method
  

  - arrays in an object
   property: room1
             room2
             room3
    value: items[420,40,10]
           items[460,20,20]
           items[230,0,0]

      - to access first charge for room1
         cost.room1.items[0];

  - objects in an array
    index number: 0
                  1
                  2
    value: {accom:420,food:40,phone:10}
           {accom:460,food:20,phone:20}
           {accom:230,food:0,phone:0}

## Built-In Objects
  - all helps you write scripts for web pages

    -browser object model - creates a model of the browser tab or window
        -first object represents current browser window or tab. under it represents the other browser features
    
    -document object model
      -creates a model of the current web page
    
    -global javasdript objects
      -group of individual objects that relate to different parts of the JS language

  -let today = new Date();
    - creates an instance of a date object
      -let = variable declaration
      today = variable name
      = - assignment operator
      new = new keyword
      Date() - date object constructor