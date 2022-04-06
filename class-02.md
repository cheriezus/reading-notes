Chapter 2: “Text” (pp.40-61)

structual markup - elements that you can use for heading and paragraphs

semantic markup - provides specific info in your tags

<br /> - adds line breaks inside paragraphs

<hr /> - adds a horizontal line between elements

empty elements - elements that have nothing between the opening and closing tag and usually has one tag

<blocquote> - used for longer quotes

<q> - used for shorter quotes

<abbr> - used for when you are abbreviating something

<cite> used to reference someone else's work

<dfn> - used to indicate a term being defined

<address> used to caontain contact info of author/creator

<ins> shows contant that has been added to a page

<del> shows text that has been deleted from a page

<s> - used to indicate content that is no longer relevant but should not be removed

Chapter 10: Ch.10 “Introducing CSS” (pp.226-245)

<audio> - includes audio files
  - src - tells where audio is coming from
  - controls - indicates if video player should show controls
  - autoplay - indicates that audio should play as soon as web page is open
  - preload - used if audio is not set to autoplay
  -loop - lets audio know that is should play again once done
<source> -used to specify more than one audio source. useful for when browsers support different players

## CSS
used to design your web page.

selector: which element you are trying change
declarations - tells how the element will change
ex: h1 {background-color: blue;}

property - tells the page what part of an element that you want to change
value - tell the page HOW you want the page to change the element

## Linking CSS file to HTML

<link href="css/styles.css">

## Selectors

* () - targets all elements

element () - targets only the elements you choose

.note () - targets any element that has been labeled by class
p.note () targets a specific element that has been labeled by class

#p () - targets the element that has been labeled by id

## How CSS rules decide which rule to implement

- if the same, then it will choose the latter rule

- if rule is more specific

- if !important is added to property value

Chapter 2: “Basic JavaScript Instructions” (pp.53-84)

JavaScript is made up of scripts that specify each step the computer must take to commit an action on a webpage

as computers work programmatically, every step must be specific

JavaScript uses:
numbers - all numbers including negative numbers
strings - text
boolean - true or false


Chapter 4: “Decisions and Loops” pp.145-162)

conditional statements- used to give computer the next steps of a script

if else - used to run code based on the condition being true or false

Comparison Operators

 Comparison Operators
== comparative equal or loosely equals
=== strictly equals


!= loosely not equal
!== strictly not equal 
&& - and - logical operator
|| - or
! - not - the opposite

- truthy
numbers (except 0)
strings (except empty strings)

falsey
(only 0)
`""`
