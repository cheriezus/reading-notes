# CSS Layout

  -display property
    -determines if the box it is applied to is an inline or block
  
  -can't set an explicit width and height on inline elements

  - block element will expand to the size of the inline dimension

  -display: flex - makes element box a block-level box, and also converts its children to flex items. This enables the flex properties that control alignment, ordering and flow
    - flexbox will align the element's children next to each other, in the inline direction, and stretch them in the block direction, so they're all the same height
    can use:
     flex-grow
     flex-shrink
     flex-basis

  - align-items - vertically center items
  - justify-content - push items away from eachother
  - flex-wrap - enables/disables wrapping
  
  - grid - designed to control multi-axis layouts
    repeat()
    minmax()
    fr - unit - fraction of remaining space
      ex: grid-template-columns: repeat(12, 1fr);
    grid-row
    grid-column
      - first element in the grid to span to the start of the fourth column, from the first column, then span to the third row, from the first row.

  - inline-block - gives you a box that has some of the characteristics of a block-level element, but still flows inline with the text.
  - float property - instructs an element to "float" to the direction specified
    - allows sibling elements to "wrap" around it
    - clear: both
      display: flow-root
    to prevent elements following the floated element from
  - .countries {
	column-count: 2;
	column-gap: 1em;
} 

- column-width - define a minimum desired width, using 

- position property -changes how an element behaves in the normal flow of the document, and how it relates to other elements.
  adding position: relative to an element also makes it the containing block of any child elements with position: absolute. This means that its child will now be repositioned to this particular element, instead of the topmost relative parent, when it has an absolute position applied to it.

absolute - You can position this element wherever you like, using top, right, bottom and left in its nearest relative parent.
All of the content surrounding an absolute element reflows to fill the remaining space left by that element.
fixed - elements stay anchored from the top left based on the top, right, bottom and left values that you set.
sticky - stays on in viewpoint of screen



