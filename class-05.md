#Chapter 5: “Images” (pp.94-125)

## Adding Images
- <img> empty element - can carry these attributes:
    - src - tell where to find the image. you can use relative URLS
    - <alt> - provides description of image
    <title> - an extra place to provide info about image. usually appears when someone hovers over an image
    height - changes height
    width - changes width

- website use jpeg, gif or png format for photos
- save image how based on what size you would like it on your page

<figure> - contains the image and the image caption
<figcaption> adds a caption to an image

Chapter 11: “Color” (pp.246-263)

  - Really cool website I found [Color Picker](https://htmlcolorcodes.com/color-picker/)
  - background-color
  - you can create colors using:
  RGB values
  hex codes
  color names - about 147 of them
  saturation - how much gray in a color
  brightness - how much black is in a color

hue - expressed using 0-360 degress
saturation - expressed as a percentage
lightness - using percentages. 0% = white, 50% = normal, 100% = black
alpha - expressed as decimal. 0.5 = 50% transparency, 0.75 = 75% transparency


Chapter 12: “Text” (pp.264-299)

##typeface terminology
serif - sans serif - monospace

font weight - can turn letters bold. light - medium - bold - black
style - basically italic. 
normal - italic - oblique
stretch - adds or remove space between letters. condensed - regular - extended

font-family
  - allows you to specify the type face that should be used
font-size - sizes up and down font size
you can use: pixels, percentages and EMS

@font-face - allows you to download font onto someone computer
ex: @font-face {font-familyL 'ChunkFiveRegular'; src: url('fonts/chunkfive.eot');}

www.fontsquirrel.com/ fontface/generator - will convert your fonts into different formats for each browser
should appear in your code in this order:
1: eot
2: woff
3: ttf/otf 
4: svg

uppercase- all text appears in all caps
lowercase- all text
capitalize - capitalizes first letter of each word

text-decoration -
- none - removes any decoration
- underline - add a line underneath text
overline - add a line above text
line-through - strikethrough text
blink - animates text
line-height - adds height to whole line of text

text-aline - controls alighnment of tect
  - left - right - center - justify (makes paragraph reach farest edges of box )

vertical-align - used for <img> <em>, or <strong> elements.
Values: baseline, sub super, top, tect-top, middle, bottom, text-bottom, length (specified in pixels or ems) or line height (in percentages)

text-indent - can take negative values and is given in pixels or ems.

text-shadow - text-shadoe: 1pc 1px 3px #6666666; 
1. how far to the left or right is should fall
2. distance to the top or bottom
3. specifies amount of blue
4. color of the shadow

:first-letter & :first-line - placed inside an element
considered a pseudo-element

:link- set styles for links not yet visited
:visited: set styles for links that you have clicked on

:hover - changes the appearance of links when users hover over them 

:active - used to make a button or link feel more like it being pressed by changing the style or position slightly

:focus - when the browser notices youo are about to focus on something like when you are about to text in a box


JPEG vs PNG vs GIF 

PNG - for images w/transparency or images with sharp text or object or logos

jpeg - used for photographs and paintings of natural scenes

gif - for animation


https://blog.imagekit.io/jpeg-vs-png-vs-gif-which-image-format-to-use-and-when-c8913ae3e01d