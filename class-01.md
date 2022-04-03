# HTML Chapter 1: “Structure” (pp.12-39)

This topic matters because it is very important to keep your web page organized and readable to not only yourself later, but to other web developers that might read your HTML.  

### HTML

-hypertext markup language
-ability to provide additional meaning to content

### Elements and Tags

  -elenents - the opening and closing tags and any content that lies between them

- tags - indicate what is going on between its opening and closing tags
- attribute - provides additional info regarding how the element will affect the content within it. Comprised of: name: what kind of info and value: a specific type from the info

### Body

- stores the content that will be displayed on website

### Head

- what goes between title

### Title

- what shows up in the browser tab

### Code in a Content Management System

- used to update content
-usually created with a template in mind so that people without software experience can update the website

In 102, we were shown how all websites used this same, if not extremely similar, structure on every page. I learned that there is no need to reinvent the wheel and that this basic structure sets the precedent for CSS and then JavaScript.

HTML Chapter 8: “Extra Markup” (p.176-199)

This is important because we still need to use many of the characters that your HTML doc will otherwise try to render on your site and this will stop any future confusion that mistake may provide.

### Markups

- <!--> - used to add comments in your code without it disrupting or showing up on your website.
- id - used to differentiate from other elements on the page. names used for ids can only be used once
- class - used to differentiate a specific group of elements

### Difference between Block and Inline elements

- block elements start on a new line. (ex: <h1> <p> <li>)
- inline elements continue from where you added it. (ex: <a> <b> <img>)

### Div

- allows you to group elements together in one block
- adding div to class or id will allow you to use CSS to customize the whole block

### Escape Characters

- in order to show characters that automoatically come out as code, you use extra markup so that it is seen as regular text on your page. (ex:&lt: for less than sign)

This is very useful to know, as I have been struggling to add to my notes the right way to write things, but to also make sure that it does not intefere with any code that I actually used for the function of my page.

HTML Chapter 17: “HTML5 Layout” (pp.428-451)

This topic is important because it makes the coding part of your page easier if you know exactly where you plan on placing everything. Also very helpful to show to clients so that the line of communication and how their website will function is clear.

### Elements used to section out your page

- nav - links to other parts pages of the website
- header - top of the page or can be used for a specific sections
- footer - bottom of page or can be used for a specific sections
- article - another way to section your page
- div - keep in mind to use to group together related elements

### a Element

- using a allows you to make a section into a whole link

HTML Chapter 18: “Process & Design” (pp.452-475)

### How to plan your site

1. who is this website for?
2. why are they coming to your website?
3. how does your website help them with that?
4. what reasons are they likely to visit your website more than once?

### Sitemap

- used to plan how each page of your website is organized and grouped
- card sorting - listing all the info a visitor to your website might need or want to know and then grouping them together

### Wireframes

- technique where you sketch out where you will be placing all relevant info on a page. highly suggested that THIS is shown to client so you are both on the same page on how the website is to function

### Visual Hierarchy

- used to help visitors focus on the most important info and then the following info.
- using visual contrast helps visitors get quickly to info that they are most likely looking for. this is done by using color, style (fonts, how the blocks and images are displayed) and size
- grouping relevant information makes the site easier to navigate and read

Planning is very important and makes sure that, once you are finishe with your page, you have acheived the goal of your website and the goal of your client. It's very useful to me as well since it makes sure that I don't miss any key features of the site that I need and makes the page look more attractive and be more informative to any visitors.

JS Chapter 1: “The ABC of Programming” (pp.11-52)

This topic is important because in order to make sure the website runs smoothly, you need to ensure that your functions follow how the computer can read it, and that it covers every step your computer will need to start it.

### Scripts

- in order for a computer to do JS, it must be given precise, detailed instructions- as if it has never done it before- for each step

1. What is the goal of the function?
2. list the steps needed in order to reach the goal (NOTE: each step might need a series of smaller steps. BE detailed)
3. turn said steps into JS using <strong>vocabulary</strong> - the words that a computer understands and <strong>syntax</strong> - putting said vocab together in a way that the computer can follow.

- programmatically - how a computer will run your code; step by step

- flowcharts - used to map out the tasks you would like the computer to do. this helps to make sure every step has been accounted for when creating a script
- NOTE: use "Generic Step", "Event", Input or output", "Decision" when creating the flow chart

### How does a computer understand all of the info that we give them?
-objects - each physical thing in data; each object might have its own: Property, Event, and/or Method.

- properties - characteristics of the object
- properties can have a <strong>name</strong> and a <strong>value</strong>
- events - how people interact with the object. this triggers part of the code
- method - where values are updated or brought up after being triggered

### Document.write

- document.write('Ello mate');
- document - represents the entire page
- . - used to access the methods and properties of an object
- ('') - where info is places in order for the method to work

### Note

- keep in mind where you place the script as that is where it will load and will affect the rest of the page

With this, it makes creating functions a lot more easier now that I know what the computer needs in order to read it. I can also use it as a checklist to assist with any future debugging if I happen to miss an important part of a script

## Things I want to know more about

Do you suggest using figure and figcaption?
Which ones are you keen on us using?

Can you explain the document object?

The example in the book uses var- which I was told is something that we should not use anymore -AND examples to use javascript within the same doc as your HTML
