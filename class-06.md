# Difference Between primitive Values & Objects References in Javascript

### critical distinction between ummutable & mutable data

- a;; data types in JS put in 2 categories: IMMUTABLE & mUTABLE dATA

    -JS supports
  - JS supports * data types
            -boolean
            -null
            -undefined
            -number
            -BigInt
            -String
            -Objects  
                -array
                -functions
                -dates

### Primitive Objects (let foo = 'bar')

    - variable is set to that value directly

#### When a varibale is assigned with an object

    - variable contains a reference to it

    const moe = {
      name: 'Moe Szyslak' (ex: primitive value - when a variable is set to that value directly)
      occuptation: 'Bartneder'
      voicedBy: 'Hank Azaria;
    }
        -JS creates, initiates it, and stores it

#### Immutable data let word = 'snow'

    (ex:strings)
    -can access individual letters of the string by using []
        - ex: console.log(word[0]) // "s"
        - cannot change the function later
         -ex: (console.log(word[0]) // "s"
            -(how to bypass) word = `k${word.slice(1)}`
                              console.log(word) // "know"

#### Mutable Data -

    -(ex: arrays)
    - let letters = ['s', 'n', 'o', 'w']
      letters[0] = 'k'
      console.log(letters) // (4) ["k", "n", "o", "w"]
          - can alter them directly

- const prevents you from reassigning values, but it does not prevent you from mutating existing values.
    let lead = 'John Lennon'
    let coLead = lead
    coLead = 'Paul McCartney'
    console.log(lead, coLead) // John Lennon Paul McCartney
  - although we assigned lead to coLead on the second line, the two values remained different after coLead was reassigned on the third line

-If you want to create a new object instead of a second reference to the same object (as we did above), you should use Object.assign
   let lead = {
  name: 'John Lennon',
  group: 'The Beatles'
}
let coLead = Object.assign({}, lead, {
  name: 'Paul McCartney'
})
console.log(lead, coLead)
// {name: "John Lennon", group: "The Beatles"}
// {name: "Paul McCartney", group: "The Beatles"}
In the example above a new object ({})is created as the target (first argument), and then each property from the lead object is applied to it (second argument), and then a new name property (‘Paul McCartney’) is applied as well (third argument).
This approach allows you to copy one object from another and still keep the original object unchanged.

== - loose equality
=== - strict equality

    -object references do not contain values directly

{ name: 'Moe Szyslak' } === { name: 'Moe Szyslak' } // false
    - can be possible when the reference (memory addres) they are stored at is different

  - wgen you take a duplicate refernec eto that object
let lead = {
  name: 'John Lennon',
  group: 'The Beatles'
}
let coLead = lead
console.log(lead === coLead) // true

In order to check whether the contents (not the reference) of two objects are the same you need to either:
Iterate through the object and check that each key and value match. This can be tricky because an object’s property can be an object in itself.
Convert the object to a suitable primitive before doing the equality check.
const moeA = { name: 'Moe Szyslak' }
const moeB = { name: 'Moe Szyslak' }
moeA === moeB // false
JSON.stringify(moeA) === JSON.stringify(moeB) // true

const dateA = new Date(0)
const dateB = new Date(0)
dateA === dateB // false
dateA.getTime() === dateB.getTime() // true


  understanding the problem is the most critical piece to the equation. 

  - this is that it is often beneficial to take a part of the problem and fully understand that part before expanding the problem domain.

  ## Object Literals

  -groups a set of variels and functions to create a model of something you would recognize in the real world

    property - a  variable that is part of the object
    method - a function that is part of an object
      - tasks that are associated with the object

        -properties and methods have a name & value
        key - the name of an object. object can't have more than one key
  - each item in an array has a name/value pair because it has an index and value
  - named functions - a swt of statements to run if the function is called
  - objects - keys(name) and value pairs

literal notation - 
  Properties:
let hotel ={name: 'Express Inn'., 
rooms:40,
  Method:
checkAvailability: function() {return this.rooms - this.booked;
}
};

checkAvailability: function() 
used to show that it is using the rooms and booked properties of this object.

### dot notation - hotel.name:
used to access properties or methos of an object
hotl = object
. - member operator
name; property/method name

# Dom
 - specifies how browsers should create a model of an HTML page and how JS can access and update the contents of a wed page while it is in the browser window

 - consists of 4 types of nodes
  - document - starting point for all visits to the DOM tree
  - element - decribes the structure of an HTML page
  - attribute - specific JS methods and properties to read or change that to element's attirbutes 
  - text - technically the content within an element

- nodeValue - lets you access or update contents of a text node
- innerHTML - accesses cheld elements and tect content

- createElement() - creates new node
  createTextNode() = create text within a node
  appendChild(( / removeChild)) - add/ remove nodes from a tree

  className / id - helps you retrieve or update the value 

  Attribue()
  -has - check if attribute exists
  -get - retrieves its value
  -set - updates value
  -remove - removes value

  #DOM queries - getElementById('one');

   - if a method can return more than one node, it will return a Node element by using an index #

 - returns a signle element
   - getElementById('id')
   - querySelector('css selector')

- returns more than one elements
  - getELementByClassName('class')
  -getElementsByTagName('tagName')
  -querySelectorAll('css selector')

-Array Syntax
 let elements = document.getElementsByClassName('hot');
 if (elements.lnegth >=1 {
    let firstItem = elements[0];
 }

-Repeating Actions for an entire Nodelist

  lethotItem = document.querySlectorAll('li.hot');
  for (let i=0; i<hotItems.length; i++) {hotItems[i].className ='cool';
  }

  - changing a list item
    let item;
    item = '<em>Fresh</em> figs';

  -attribute note
    document.getElementById('one').getAttribute('class');

  -removing attributes
    let firstItem = document.getElementById('one');
    if(firstItem.hasAttribute('class')) {
      firstItem.removeAttribute('class');
    }

# In Class Notes

- command b hides your side panel

- function signature - what are the inputs and outputs

- you can test your code in the console
  - just type it in then test it ex: sumArray([])

const programmer = {
  name: "Grace Hopper",
  age:100,
  lovesDebugging: true,
  greet:function() {
    return "H1";
  }
};

console.log(programmer.greet());
(invokes function)
