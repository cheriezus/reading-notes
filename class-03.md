Chapter 3: “Lists” (pp.62-73)

<ol> - ordered list using numbers
<ul> - unordered lists - such as bullet points. can be used to create a list within a list by placing it within the block element again
<li> - the opening tag that is used to start <ol> and <ul>
<dl> - used to create terms and their definitions
<dt> - contains the term
<dd> - contains the definition



Chapter 13: “Boxes” (pp.300-329)
To control the size of a box around a block element, people usually use percentage or piccels or ems.

Percentages are relative to the size of the web page or the size of the box around it. 

Pixels are different for many computers

 min-width - creates the smallest box possible around the block

 max-width - creates the biggest box you can make in your browser

 min-height - limits the height of a block element

 max-height - maximizes height of a block element

 overflow - instructs the browser on how to configure the content inside of a block element

 hidden - hides and content that can't fit in the box

 scroll - adds a scroll bar to the box

 border -- seperates end pieces of a block from another edge of another block

 margin - the space outside of a border

 padding - the space within a border

 border-width - control width of border. cannot use percentages
  -border-top-width
  -border-right-width
  -border-bottom-width
  -border-left-width

  border-style - controls the type of borer that is around the block
  you can control each side of a border using: border-top-style 
  border-left-style 
  border-right-style 
  border-bottom-style

  border-color - changes color of a border. you can also control each side of a border using the above

  border - allows yoou to control style, width and color in shorthand
  ex : h1 {width: 250px; border: 3px dotted #0088dd;}

  centering a block element - set the width of the block then put left-margin and right-margin to auto

  text-align used for older browsers

  display - changes inline element to block element and vice versa
  display: inline or display: block

  border-image - applies image to border of any block. take image and seperates into 9 pieces
   - needs:
    1. url of image
    2. where to cut image
    3. what to do with straight edges using:
      - stetch, repeat or round
      *must have border width to see image*

## box-shadow
  - allows you to add a drop shadow around a box
    - horizontal offset - negative changes positions shadow to left
    - vertical offset - negative changes positions shadow to top
    - spread of shadow - positive increases are aof reach of shadows

## border-radius
  border-top-right-radius
  border-bottom-right-radius 
  border-bottom-left-radius 
  border-top-left-radius
  - using shorthand:
 going by clockwise order
  ex: border-radius: 5px, 10px, 5px, 10px;
- note: can make a circle bu making border-radius same height as the square
  


 Chapter 2: “Basic JavaScript Instructions” (pp.70-73)

## arrays 
 - used to store a list of items that you are unsure will be the final amount or might be added to later
 - stores list of values that relate to one another
 ex: let colors = newArray ('white', 'black', 'custom');
 - numbers on list start at 0
 - shows up as a table w/index on the left and value on the right. index starts at 0 and value is where the items are displayed
 - can store a string, a boolean & number in the same array

## Creating the array
let colors;
colors = ['white', 'black', 'custom'];

## Retreiving item from the array
let itemThree;
itemThree = colors[2];
 
##Holding the number of items in an array
  let numColors;
  numColors = colors.length;
 

Chapter 4: “Decisions and Loops” from switch statements on (pp.162-182)

if... else - allows you to provide code for any chosen output in response to any input provided by the visitor

ex: if (score >= 50) {congratulate();
}
else {encourage();
}

## Using switch
- the default option if no matched input if found
- break - stops the rest of switch statement if match is found

ex: switch (level) {case 'One';
title = 'Level 1';
break;

case 'Two';
title - 'Level 2';
break;

case 'Three'; 
title = 'Test';
break;
}

type coercion - changes value in order to complete an operation
To avoid this, it is suggested to use === and !== in order to make sure that JS does not convert the value in order to make it true

## Truthy and Falsy

falsy values- values that are treated as false
ex: false; 0; ''; 10/'score; highScore;

truthy - values that are treated as true
ex: true; 1; 'carrot'; 10/5; 'true'; '0'; 'false';

unary ooperator - returns a result with just one operand

