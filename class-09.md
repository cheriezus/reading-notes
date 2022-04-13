# Forms

- <form> creates a form
- action - value where uRL of site that keeps info from form
- method - how forms can be sent
  - get - values from the form are added to
            the end of the URL specified in the action attribute
              great for: retreving data from the web server
  - post - values are sent in what are known as HTTP headers
              great for:  allows users to upload a file, contains sensitive data, adds information to, or deletes information from, a database

- id - identify the form distinctly from other elements on the page

## Text Input

    - <input> creates specific different form controls
    - type='text' - creates sidngle line text input
    - name - identifies the form control and is sent along with the  information they enter to the server
    - maxlength - limits number of characters
  
## Password Input

    - type="password" - creates a text line input that hides the characters
    - size, maxlength - same
  
## Text Area

    - <textarea> - creates multi-line text input
  
## Radio Button

    - type="radio" - give user multiple options but only lets them choose one
      - name - where the name of options are placed
      - value - option selected that is sent to server
      - checked - when page loads, this tells page what option is already selected

## Checkbox

    - type="checkbox" - allows users to select/deselect multiple  options
    - name - same
    - value - same 
    - checked - same

## Drop Down List Box

    - <select> - select one option from a drop down list
    - selected - same
    - value - same
  
## Multiple Select Box

    - <select>
      - size - turns a drop down select box into a box that shows more than one option
      - multiple - allow users to select multiple options from list 

## File Input Box

    - <input>
      - type="file" - creates a box that looks like a text input followed by a Browse button.
  
## Submit Button

    - <input>
      - type="submit" - sends a form to the server
      - name - not necessary but can be used
      - value - control the text that appears on a button
  
## Image Button

    - <input>
      - type="image" -  use an image for the submit button
        - uses: src, width, height, and alt - just like <img>
  
## Button & Hidden Controls

    - <button> - allows other elements to appear inside the button
    - <input>
      - type="hidden" - adds values to forms that users cannot see
  
## Labeling Form Controls

    - <label> - each form control should have its own <label> element as this makes the form accessible to vision-impaired users.
    - for - states which form control the label belongs to
  
## Grouping Form Elements

    - <fieldset> -  group related form controls together 
    - <legend> - ontains a caption which helps identify the purpose of that group of form controls - comes after fieldset

## Form Validation

    - give users messages if the form control has not been filled in correctly

## Data Input

    - <input> 
      - type="date" - creates a date input 
  
## Email & URL Input

    - <input>
      - type="email"
      - type="url"
  
## Search Input

    - <input>
      - type="search"
      - place holder

# Lists, Tables & Forms

## Bullet Point Styles

    - list-style-type - allows you to control the shape or style of a bullet point. same rules as list elements

      - Unordered Lists
          - none
          - disc
          - circle 
          - square
        
        - Ordered Lsts
          - decimal
          - decimal-leading-zero
          - lower-alpha
          - upper-alpha
          - lower-roman
          - upper-roman

## Images For Bullets

      - list-style-image
          - starts with the letters url and is followed by a pair
of parentheses. Inside the parentheses, the path to the image is given inside double quotes.

## Positioning the Marker

    - list-style-position - ndicates whether the marker should appear on the inside or the outside of the box containing the main points
      - outside - sits to the left of the block of text - a.k.a default behavior
      - inside - inside
  
## Table Properties

  - width - to set the width of the table
  - padding - to set the space between the border of each table cell and its content
  - text-transform - to convert the content of the table headers to uppercase
  - letter-spacing, font-size - to add additional styling to the content of the table headers
  - border-top, border-bottom - to set borders above and below the table headers
  - text-align - to align the writing to the left of some table cells and to the right of the others
  - background-color - to change the background color of the alternating table rows
  - :hover - highlight a table row

## Border on Empty Cells
show - show borders
hide - hide
inherit - obey rules of the containing table

## Gaps Between Cells
 - border-spacing, border-collapse
    - collapse - borders are collapsed into a single border where possible
    - seperate - boorders detached from eachother

## Styling Text Inputs
   - font-size 
    - color - text color
    - background-color
    - border
    - border-radius can be used to create rounded corners
    - :focus pseudo-class - used to change the background color of the text input when it is being used
    - :hover psuedo-class applies the same styles when the user hovers over them
    - background-image adds a background image to the box

## Styling Submit Buttons
    - color
    - text-shadow - can give a 3D look to the text
    - border-bottom - make the bottom border of the button slightly   thicker. gives it 3D feel.
    - background-color 
    - :hover - used to change the appearance of the button when the user hovers over it
  
## Styling Field Sets & Legends
    - width 
    - color
    - background-color
    - border
    - border-radius
    - padding

## Cursor Styles 
    - auto, crosshair, default, pointer, move, text, wait,
help, url("cursor.gif");

# Events

  - event handling 
    1. select the element node that you want the script to respond to 
    2. which event triggers the response
    3. what code will run when the event occurs
  
  - creating an event handler
      - element.oneevent = functionname;
    
  - event listeners - can deal with more than one function at a time
    - element.addEventListener('event',functionName[, Boolean]);
  
  - anonymous function - el.addEventListener('blur'.function) {
    checkUsername(5);
    }, false);

  ## Event Flow
    - flow of event only really matters when you code has event handles on an element and one of its ancestor or descendent elements
    event object - when an event occurs, the event object tells you info about the event and the element it happened upon

    - load event - used to trigger scripts that access the contents of the page
    - a mutation event occurs whenever elements are added or removed from the DOM