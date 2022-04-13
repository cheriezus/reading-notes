# Chapter 4: Ch.4 “Links” (pp.74-93)

## Linking to other websites
<a href="link">the text the user clicks on</a>

## Linking to other pages on the same website
 - instead of adding the full URL, you use the relative URL
 ex: about-us.html
- allows you to create links between pages without having to host the website 

root folder- contains all files and folders of that website

index.html
- homepage of a website

relationships
- describing the relationship of one file or folder to another the same way you would describe a relationship in a family tree

## How to get computer to navigate through relative URLS
  - same folder - just use the file name
  - chold folder - name of child folder/file name
  - granchild folder - name of child folder/grandchild folder/filename
  - parent folder - ../filename
  - grandparent folder - ../../filename

  mailto: creates a link that allows you to send an email to a specific email address

-target - attribute used to open a link in a new tab
ex: <a href="http://www.imdb.com" target="_blank">

## link to specific part of same page
 ex: <h1 id="top"> </h1>
  - first create and id
  <p><a href="#top"> </a></p>
 - to a specific part of a diffrent page
 - <a href ="http:/www.htmlandcssbook.com/#bottom">


# Chapter 15: “Layout” (pp.358-404)

## Containing Elements
parent element - when a block element is nested inside another block element
<div> - can be used as a containing element

## Positioning Schemes
  - normal flow - default behavior of a block element. appears on a new line
  - relative positioning -  shifts the element to top, bottom, left or right and does not affect elements around them
  - absolute positioning - elements that follow you as you scroll up and down the page, but does not affect the other elements

  box offset - tells how far away from the sides the block should be positioned
  - fixed positioning - positions block in relation to browser window, but is same as absolute positioning 
  - floating elements - allows you to move the element to the far left or right of a block. The rest of the content in the box moves around it
  - z-index - allows you to control which box, when using the flowing element, appears on top 
  - position:static - the way blocks are originally created as
  -position:relative - moves it to where it would have been in normal flow
  -position:absolute - can be moved without affecting the position of other elements
 - position:fixed - makes the element stay in place on the page no matter where the visitor scrolls

## Floating Elements
 - float - allows you to move part of the block element as far as you want, left or right, while the rest of the block element flows around it. should use the width property in order to indicate how far away the rest of the block element should flow around it
 - to make things side by side:
  - clear - allows you to ensure that no element touches the sides of the box
    values for clear - left, right, both, none

# Multi-Column Layouts w/Floats
 - by using <div> for each column you would like to create
 - width- width of the columns
 - float- positions columns side by side
 - margin - creates a gap between cplumns
 
# Page Size
- average size of a browser window without scrolling: 1000px by 570px

## Types of Layouts
 - fix width layouts - static lauyout design even if user changes size of browser window - uses pixels
 - liquid layouts - stretches or shrinks based on the user changes size of their browser window - uses percentages

 ## Layout Grids
  - used to set consistent propertions around the page
  - setting a 12 column grid - a class attribute is given to the element that contains the entire page and the value becomes 'container_12'

  Note: some people use multiple style sheets in order to organize elements 
  - use @import in your linked stylesheet in order to import the rest of your style sheets

# Chapter 3 (first part): “Functions, Methods, and Objects” (pp.86-99 ONLY)

-funtions - let you group a series of statements in in order to perform a specific task
- code block (in between the curly braces) are where the steps and any info is stored in order for a function to complete its task a.k.a parameters
return value- when you expect an output from a function 
 - function declaration - where you give a funciton a name and the the statements/steps needed to achieve its task
 - calling the function - using the name of the function followed by parentheses
 - arguments - tells the function what values it should use in order to acheive its task
  - as values : getArea(3,5);
  - as variables : wallWidth =3;
                   wallHeight = 5;
                   getArea(wallWidth, wallHeight);

NOTE: parameters are less specific than arguments in functions. ex: parameter = width & height - tells function what it needs to find to calculate. 
arguments = wallWidth - 3; wallHeight = 5; - gives the function the specific info it needs to acheive its task

## Getting a single value out of a function
ex: function calculateArea(width, height) {
  let area = width * height;
  return area;
}

let wallOne = calculateArea(3, 5);
let wallTwo = calculateArea(8, 5);

##Using an array in a function

function getSize(width, height, depth) {
  let area = width * height;
  let volume = width * height * depth;
  let sizes = [area, volume];
  return sizes;
}
let areaOne = getSize(3, 2, 3)[0];
let volumeOne = getSize(3, 2, 3)[1];

- function expression - interpreter treating a function as an express, because it expects to see an expression
-anonymous function - a function with no name. note: you cannot make afunction start before interpreter gets its info

# Article: “6 Reasons for Pair Programming”

- practive of two developers working together to create codes
- needs the driver and navigator
  -driver - the person who is typing the code/operating the computer
  - navigator - guides the driver

# In Class Notes

## functions 
- a group of statements that perform a task
-stored in a structure that precents them from  running until the function is called or invokes
-functions are resuable
-functions help to keep our code DRY
- help prevent/find bugs

define/declare

     
function sum(a,b) 
{return a + b}


arguments - declare
parameter- define


Example of ${} placeholders
let a = 5;
let b = 10;
console.log(`Fifteen is ${a + b} and
not ${2 * a + b}.`);
// "Fifteen is 15 and
// not 20."

