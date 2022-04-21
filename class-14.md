# What Google Learned From Its Quest to Build the Perfect Team

  - individual personalities in a team are not that important

  ### Five Key Characteristics of "enhanced teams"

    1. everyone feels safe taking risks
    2. everyone completes quality work on time
    3. everyone knows what they need to do in their team
    4. everyone has a sense of purpose in their work
    5. everyone sees that their hard work matters

# CSS Transforms

## Transform Property

  - comes in 2 and 3 dimensional setting
  - 2 dimension works on the x & y axes, a.k.a horizontal and vertical axes
  - 3 dimension work on the x & y axes and z axis. helps to define length, width, and depth
  
### Transform Syntax
  - value specifies the transform type followed by a specific amount inside parentheses.
  - uses multiple vendor prefixes to cover support for different browsers
    - ex (from learn.shayhowe.com)
      - div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}
### 2D Transforms

  -2D Rotate
    - rotate - provides ability to rotate an element 0 to 360 degrees.
    - positive value = clockwise and negative value will rotate to counterclockwise
    -  defulat point of ration: center of element, 50% horizontally and 50% vertically
      - Rotate Demo:

      <figure class="box-1">Box 1</figure>
    <figure class="box-2">Box 2</figure>

      .box-1 {
   transform: rotate(20deg);
  }
  .box-2 {
   transform: rotate(-55deg);
  }

  -2D Scale
    - scale - value that changes the size of an element. default scale value = 1. .99 to .01 makes things smaller and 1.01 and up makes things look larger

    <figure class="box-1">Box 1</figure>
    <figure class="box-2">Box 2</figure>
      .box-1 {
     transform: scale(.75);
   }
    .box-2 {
     transform: scale(1.25);
    }

   - scaleX - value that scales width of element.
   - scaleY - value that scales height of element
      ex: <figure class="box-1">Box 1</figure>
          <figure class="box-2">Box 2</figure>
          <figure class="box-3">Box 3</figure>

     .box-1 {
    transform: scaleX(.5);
    }
    .box-2 {
    transform: scaleY(1.15);
    }
    .box-3 {
    transform: scale(.5, 1.15);
    }     

### 2D Translate
  - pushing and pulling an element in different directions without interrupting normal flow of document.
    - translateX - changes position on the horizontal axis
    - translateY - change position on vertical axis

      ex: <figure class="box-1">Box 1</figure>
          <figure class="box-2">Box 2</figure>
          <figure class="box-3">Box 3</figure>

          .box-1 {
            transform: translateX(-10px);
            }
          .box-2 {
             transform: translateY(25%);
            }
            .box-3 {
           transform: translate(-10px, 25%);
            }

### CSS3 Transitions & Animations
    
    - ability to altered in multiple keyframes
    - transitions - provide a change from one state to another
    - animations - set multiple points of transition upon different keyframes

  #### Values for Transitions
    - :hover, :focus, :active, :target - pseudo-classes
  
  #### Properties for Transitions
  - transition-property, transition-duration, transition-timing-function, transition-delay. 
  
  background-color
  background-position
  border-color
  border-width
  border-spacing
  bottom
  clip
  color
  crop
  font-size
  font-weight
  height
  left
  letter-spacing
  line-height
  margin
  max-height
  max-width
  min-height
  min-width
  opacity
  outline-color
  outline-offset
  outline-width
  padding
  righttext-indent
  text-shadow
  top
  vertical-align
  visibility
  width
  word-spacing