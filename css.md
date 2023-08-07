# CSS

HTML elements have their default styles, which can be changed using CSS styling

CSS can be written: Inline | Internal </style> | External style.css

## CSS CheatSheet

- Basic format
- CSS selectors & units
- The Box Model
- CSS properties: Font, Text, Background, Color, Column, animation, Transition, Position, Outline, List, Transform
- CSS Layouts: Floats Flexbox Grid

## Basics

Ways to put CSS:

- inline(inside html tags)
- internal(</style>) / external(.css)

CSS Format:

```css
selector{
    property: value;
    property: value unit;
}
```

- Selector: selects the HTML elements you want to style.
- Property: a style or function for HTML elements.
- Value: a number value (with units) / word value / code / defaults (inherit, initial, unset, ..)

## CSS Selectors

Used to "find" (or select) the HTML elements you want to style.

Categories of selectors:

- Simple
  - element (div/h1/p/span/...)
  - .class
  - #id
- combinator
- Pseudo
  - Pseudo-class
  - pseudo-element
- attribute

> Selector specificity (priority): Declarations marked (!important)  >  Inline style  >  ID(#)  >  Class(.)  >  Element(p,div,..)  >  Universal(*)

Also, in internal/external CSS latest value of same property (bottom most) applies.

- Universal (\*) - Selects all elements - eg.* {color: red;}
- Element (h1/p/..) - Select using element name - eg. p {font-size: 18px;}
- Class (.) - Select single or multiple elements using their class - eg. .button {color: #ffffff}
- id (#) - Select a sinlge element using its unique id - eg #submit-button {disabled: true}
- Attribute ([ ]) - Select an element that has a particular attribute - -eg. a[target="_blank"] {color: #00ff00;}
- Pseudo-class (:) - To Style an element in a particular state. - eg a:hover {background-color: 0000ff;}
- Pseudo-element (::) - To style specified part of an element - eg. p::first-line {color: ff0000}
- Multiple elements (,) - to give multiple elements the same styling - eg. h1, p, .button {font-size: 17px;}
- Child (>) - To style a direct child of an element - eg. .caption > p {color: ff0000}; .parent > *{}
- Descendant (space) - To style a descendant, could be child or lower - eg. .caption p {color: ff0000}
- Adjacent/Sibling (+) -

### Pseudo selectors

#### Pseudo-element

pseudo-element(::) is by default inline

::firt-letter & ::first-line - Adds special styling to 1st letter & line of a text
h1::first-letter{
    font-size: 80px
}
p::first-line{
    font-weight: bold;
}
h3 + p::first-line{
    font-weight: bold;
}

::before & ::after - Adds some content before & after an element
h1::before
h1::after{
    content: "";  -> (mandatory) adds extra content (mostly small styles that we dont want in our HTML)
}

#### Pseudo-class

pseudo-class(:)

##### child

first-child, last-child, nth-child(2), nth-child(even),

li:first-child{
    color: red;
}
article p:first-child{
    font-weight: bold;
}
// if not then apply:
li:not(:last-child){
    margin-bottom: 2rem
}

##### links

// only </a> with href link in it
a:link{}
// cursor hovered
a:hover{}
// while clicking
a:active{}
// visited links
a:visited{}

nav a:link:last-child{
    margin-right: 0;
}

:link & :visited
    Styles an unvisited link & a visited link
:focus & :hover
    An element when with focus & when u mouser over it
:enabled & :disabled
    Styles an enabled element & a disabled element
:checked & :selection
    A checked form element and a highlighted element
:first-child, :last-child & :only-child
    Styles 1st child, last child & only child of an element
:nth-child(n) & :nth-last-child(n)
    The nth child & the nth child counting from the end
:first-of-type, :last-of-type & :only-of-type
    An element that is 1st, last or only type of its siblings
:nth-of-type(n) & :nth-last-of-type(n)
    The nth sibling or nth counting from last of its siblings
:root
    Styles an unvisited link & a visited link
:empty
    An element when with focus & when u mouser over it
:active
    Styles an activated element
:target
    Styles the current active target element

## CSS Units

CSS units:

- Pixel px - Represents pixel on a device
- Points pt - 72 points = 1 inch
- Ems - 1em = current font size
- rem - root em
- Percent % - full is 100%

### Absolute Units

Absolute measurement units do not change with changing browser window or device screen size

- Not good for responsiveness. use only when you know what you are doing
    Centimeter-cm  Millimeter-mm  Inch-in  Point-pt

### Relative Units

Relative measurement units change with changing screen size, pixels, width, etc

- Very good for responsivity. Preferred over absolute units
    Percentage-%
        Styles an unvisited link & a visited link
    Pixel-px
        An element when with focus & when u mouser over it
    em
        Relative to font size of the current element
    Rootem-rem
        Relative to font size of root element(mostly < html>)
    vh & vw
        Relative to the viewport height(vh) or width(vw)
    vm
        Relative to vh or vw, whichever is smaller

### Angles

Degrees-deg  Radians-rad  Grads-grad  Turns-turn

### Frequency

Hertz-Hz  Kilo-Hertz-kHz

### Time

Seconds-s  Milli-seconds-ms

## Box-model

It is essentially a box that wraps around every HTML element.

It consists of:

- the actual _content_ (height, width)
- _padding_
- _border_
- _margin_

-Unless Specified, Value is always a length(px, em, rem, etc) or %

### Content

The content of the box, where text and images appear.

- height & width: Specifies the height & width of content
- max-height & max-width: Cannot be exceeded by height or width value

- float: Positions elements to far left or right. Values: left, right. Make sure the elements are the only 2 in their div. Float one left & the other right
- display: Specifies if/how an element is displayed. Values: none, block, inline, inline-block

### Border

A border that goes around the padding and content, not visible until given a width

- Value: border-width, border-style, border-color eg. border: 3px, solid, red; ( in that order)
- BORDER STYLES: solid, dotted, dashed, double. 3D versions - groove, ridge, inset, outset. none, hidden

Values can also be properties on their own. eg. border-style: 3px; border-top-color: 8px; border-right-style: solid;
    border-top
        Specifies only the top border
        - Same values and same arrangement as border
    border-right
        Specifies only the right border
        - Same values and same arrangement as border
    border-bottom
        Specifies only the bottom border
        - Same values and same arrangement as border
    border-left
        Specifies only the left border
        - Same values and same arrangement as border

### Margin

Used to create space around elements, outside of any defined borders

- Value: margin-top, margin-right, margin-bottom, margin-left - eg. margin: 5px, 10px, 5px, 10px;
    margin-top
        Specifies only the top margin
    margin-right
        Specifies only the right margin
    margin-bottom
        Specifies only the bottom margin
    margin-left
        Specifies only the left margin
    margin- shorthand
        When only 2 vals are specifed. eg. margin: 5px 10px
        1st val - margin-top & bottom. 2nd val - margin-right &lft
    margin-shortest hand
        When only 1 value is specifed. eg. margin: 5px
        The value represent all margins

### Padding

Used to generate space around an element's content, inside of any defined borders

- Value: padding-top, padding-right, padding-bottom, padding-left - eg. padding: 5px, 10px, 5px, 10px;
    padding-top
        Specifies only the top padding
    padding-right
        Specifies only the right padding
    padding-bottom
        Specifies only the bottom padding
    padding-left
        Specifies only the left padding
    padding - shorthand
        When only 2 vals are specifed. eg padding: 5px 10px
        1st val - padding-top & bottom. 2nd val - padding-right &lft
    padding - shortest hand
        When only 1 value is specifed. eg. padding: 5px
        The value represent all paddings

### Box-sizing property

- content-box (default) : final width/height = content + padding + border
- border-box : final width/height = content (padding, border gets into it)

```css
*{
    box-sizing: border-box;
}
```

### Display

Display property specifies the display behaviour of HTML element

- Block - 100% of parent width | box-model applies | ex: body main header footer section nav aside div h1-h6 p ul ol li ...
- Inline - Content's space | box-model applies | ex: span b strong i em a button
- Inline-block - Occupies only Content's space (no line breaks) | box-model is different (height, width don't apply | padding, margin only horizontally) | ex: img

### Position

Specifies the type of positioning method used for an element
Use properties - `top, bottom, right, left` to specify the position after specifying the type of positioning

- Static -
- Absolute - Relative to it's first positioned ancestor.
- Relative - Relative to the elements original position.
- Fixed - Relative to browser window. Fixed to specified location.
- Sticky - Relative to a scroll position. ie. first relative then become fixed.

## CSS propeties

### Font

The CSS font properties define the font family, boldness, size, and the style of a text
    font-family
        Generic Family - Serif, Sans-serif, Monospace
        -Font families: Times New Roman, Verdana, Courier New
    font-size
        Default: 16px.
        - values: px, %, em, rem, vw, small, large, etc.
    font-style
        Mostly used to specify italic text.
        -Values: normal, italic, oblique
    font-weight
        Sets how thick chars in text shld b displayed
        -Values: normal, bold, bolder, lighter, 100 - 900
    font-stretch
        Allows you to make text narrower or wider
        -Values: normal, condensed, expand, ultra-condensed,
        ultra-expanded, semi-condensed, extra-condensed
    font-variant
        For displaying caps letters with a smaller text size
        -Values: normal, small-caps, inherit

### Text

text-decoration
    Specifies the decoration added to text
    - Values: underline, overline, line-through
text-align
    Set the horizontal alignment of texts in a div
    - Values: right, left, justify, center
direction
    Set text direction from left to right or vice versa
    - Values: rtl, ltr, inherit, initial
text-overflow
    Specifies how overflowed text shld b displayed
    - Values: clip, ellipsis, stringz
text-transform
    Controls the capitalization of text
    - Values: capitalize, uppercase, lowercase, none
text-shadow
    eg. text-shadow: 2px 2px 8px #FF0000
    - Value order: horizontal, vertical, blur-radius, color
text-indent
    Specifies indentation of the 1st line in a text-block
    - Values: px, em, %. etc
letter-spacing
    increase/decreases space betwn chars in atext
    - Value: px, em, etc

```css
.text{
    color: (rgb hex hsl hwb + a);
    font-size: __ px em rem %;
    font-weight: (400 600 800 bold bolder);
    font-style: (normal, italic, oblique, ..);
    font-family: (serif, sans-serif, monospace, ..);
    text-transform: (uppercase, lowercase, capitalize);
    line-height: 1(default);
    letter-spacing: normal (.3rem, 3px, ..);
}
```

### Background

Short hand eg - background: lightblue url("img_tree.gif") no-repeat fixed center;
-Order: background-color, background-image, background-repeat, background-attachment, background-position
    background-color
        Specifies the background color to be used
        - Value: color (name, hex, rgba, hsl)
    text-align
        Specifies 1 or more bg images to be used
        - Values: URLs, seperated with a comma
    background-position
        Specifies the position of the background images
        - Values: center(commonly used), left center, etc
    background-size
        Specifies the size of the background images
        - Values: cover(common), auto, contain
    background-attachment
        Specifies mov't of element relative to container
        - Values: scroll, fixed, local
    background- repeat
        Sets if/how a bg image will be repeated
        - Values: repeat, no-repeat, repeat-x, repeat-y, space
    background-origin
        Specifies the positioning area of the bg images
        - Values: border-box-padding-box, content-box
    background-clip
        Specifies the painting area of the bg images
        - Values: border-box-padding-box, content-box

### Color

- Color name: White Black Red Green Blue ..
- Common Hex: `#ffffff #000000 #ff0000 #00ff00 #0000ff` ...See the pattern?
- Common rgb: `rgb(255,255,255) rgb(0, 0, 0) rgb(255, 0, 0)` ...Same Pattern - ff = 255

### Outline

A line that is drawn around elements, outside the borders, to make the element "stand out"
Shorthand - outline: outline-width outline-style outline-color. eg. `outline: 2px solid black`
outline-width
    Values: length(px, em,etc), medium, thin, thick
outline-style
    Values: none, hidden, dotted, dashed. solid, double ect
outline-color
    Value: color
outline-offset
    Adds space b/n an outline and the edge or border, value: px

### List-style

Specifies the styling applied to a list of items, </li>
Shorthand - list-style: list-style-type list-style-position list-style-image. eg. `list-style: square inside url("img.jpg")`
list-style-type
    Values: disc(default), square, circle, decimal, armanian, etc
list-style-position
    Values: outside(default), inside
list-style-image
    Value: image URL. eg. url(my-img.jpg)
__Note__: Any missing list-style value will be replaced by the default

### Transform

Applies a 2D or 3D transformation to an element. allows you to translate, scale, rotate, skew
Values can be an angle(deg), length(px,em,etc), percentage, decimal(unitless)

translate(x,y)
    Defines a 2D translation
translate3d(x,y,z)
    Defines a 3D translation
translateX(x),translateY(y),translateZ(z)
    Defines a translation, using value for the X, Y or Z-axis
scale(x,y)
    Defines a 2D scale transformation
scale3d(x,y,z)
    Defines a 3D scale transformation
scaleX(x),scaleY(y),scaleZ(z)
    Defines a scale transfor mation by givin a val for X, Y or Z-axis
rotate(angle)
    Defines a 2D rotation along an angle(parameter)
rotate3d(x,y,z,angle)
    Defines a 3D rotation
rotateX(angle),rotateY(angle),rotateZ(angle)
    Defines a 3D rotation along the X, Y or Z-axis
skew(x-angle,y-angle)
    Defines a 2D skew transformation along the X & Y-axis
skewX(x-angle),skewY(y-angle)
    Defines a 2D skew transformation along the X or Y-axis
perspective(n)
    Defines a perspective view for a 3D transformed element

#### Transform Properties

transform-style
    allows changing the position of transformed elements
transform-origin
    Specifies how nested elements are rendered in 3D space

### Column

column-count
    Spec no of columns an element should be divided into
    Values: auto(default), number(of columns)
column-fill
    Specifies how to fill columns, balanced or not
    - values: balance(default), auto
column-gap
    Specifies the gap between the columns
    -Values: length(px,em,rem), normal
column-rule
    Sets width, style, & color of rule b/n columns
    -Values: column-rule-width, column-rule-style
column-rule-color
    Specifies the color of the rule between columns
    -Values: color
column-rule-style
    Specifies the style of the rule between columns
    -Values: none, hidden, dotted, dashed, solid, etc
column-rule-width
    Specifies the width of the rule b/n columns
    -Values: length(px, em,rem), medium, thin, thick
column-span
    Spec how many colmns a elemnt shld span across
    -Values: column-rule-width, column-rule-style
column-width
    Specifies the column width
    -Values: auto, length(px,em,rem)
columns
    Shorthand for column-width & column-count
    -Values: column-width, column-count, auto

### Animation

An animation lets an element gradually change from one style to another.
The animation is declared with `@Keyframes`, and the following properties are used to modify it's behavior:

animation
    A shorthand 4 setting all animation properties
    -Values: animation-name, -duration, -timimg-function, -delay, -iteration-count, -direction
animation-name
    Specifies the name of the @keyframes animation
    -Values: text
animation-duration
    Spec time animation should take to complete 1 cycle
animation-timing-function
    Specifies the speed curve of the animation
    -Values: ease, linear, ease-in, ease-out, ease-in-out - Value: time. eg, 4s
animation-delay
    Specifies a delay for the start of an animation
    - Value: time. eg, 4s
animation-iteration-count
    Specif no of times an animation shld b played
    - Value: number
animation-direction
    Specifies the direction of play of the animation
    - Values: normal, reverse, alternate, alternate-reverse
animation-play-state
    Spec whether animation is running or paused
    - Values: paused, running

### Transitions

Allows you to change property values smoothly, over a given duration.
To add transition, at least 2 things must be specified, the transition-property and transition-duration.

transition
    A shorthand 4 setting all transition properties
    -Val: transition-property, -duration, -timimg-function, -delay
transition-property
    Spec name of CSS propaty the transition effect is for
    - Value: CSS Property. eg. width, color
transition-duration
    Spec time(millisec) it takes to complete transition
    - Value: time. eg 4
transition-delay
    Spec a delay (in sec) for the transition effect
    - Value: time eg. 1
transition-timing function
    Specifies the speed curve of the transition effect
    - Values: ease, linear, ease-in, ease-out, ease-in-out
Transition vs Animation
    Transition is a form of animation
    - Except it works on only a start & end value, for more flexibility, use animation

### Speech

Essentially converts your document into speech and feeds it into screen reader for the user
It is best for people with impaired vision or people with reading problems.

cue
    Sets the cue properties in one declaration
    -Values: cue-before, cue-after
cue-before & cue-after
    Sound to play b4 & after speaking elemnt's contnt
    -Values: none, url
elevation
    Sets where the sound should come from
    -Values: angle, below, level, above, higher, lower
pause
    Sets the pause properties in one declaration
    -Values: pause-before, pause-after
pause-before & pause-after
    A pause b4 & after speaking an element's content
    -Values: time, %
voice-family
    Specifies the voice family of the speaking
    -Values: male, female, child, other specifics
pitch
    Specifies the speaking voice
    -Values: frequency, x-low, low, medium, high, x-high
pitch-range
    Specifies the variation in the speaking voice.
    -Value: number
play-during
    A sound to play while speaking an elemnt's content
    -Values: auto, none, url, mix repeat
richness
    Specifies the richness of the speaking voice.
    -Values: number
speak
    Specifies whether content will render aurally
    -Values: normal, nonne, spell-out
speak-header
    Specifies how to handle table headers
    -Values: always, once
speak-numeral
    Specifies how to speak numbers
    -Values: digits, continuous
volume
    Specifies the volume of the speaking
    -Values: number, %, silent, soft, medium, loud
speech-rate
    Specifies the speed of the speaking
    -Values: number, slow, medium, fast, slower, etc
stress
    Specifies the "stress" in the speaking voice
    -Values: number

## Layouts

Layouts: Floats Flexbox Grid

### Float

Floats {outdated}
    Takes the element out of HTML flow
    float: left right center
    clear: left right both (to remove float)

### Flexbox

The Flexible Box Layout Module, makes it easier to design flexible responsive layout structure

Flexbox creates 1D row/column layout. (perfect for component layouts)
main-axis
cross-axis
flex-container
flex-items

Flex container properties:

- flex-direction
- flex-wrap
- flex-flow
- justify-content
- -align-items
- align-content

```css
.parent{
    display: flex
    flex-direction: column row(default)  -  direction of elements(main-axis)

    gap: 
    flex-wrap: wrap nowrap(default) wrap-reverse  -  child elements can wrap them when screen size decreases (stops overflow)

    justify-content: center flex-start/end space-around/between/evenly 
    align-content: center flex-start/end baseline
    justify-items: 
    align-items: 
}

.child{
    flex-grow: 1 (default=0)    - takes the extra space and distribute acc.
    flex-shrink: 0 (default=1)  - takes the min-width to stop overflow
    flex-basis : 0 (default=auto)   - change ratio acc. to content size ie. width
    flex: 1;    (shorthand{flex-grow: 1; flex-shrink: 1; flex-basis: 0})
    align-self: auto(default), stretch, center, baseline, flex-start/end
    order: 0(default), -1(to front), 1(to last)
}
```

display
    Specifies the type of box used for an HTML element
    Set value to "flex" to use flexbox
flex-wrap
    Specifies whether the flex items should wrap or not
    - Values: nowrap, wrap, wrap-reverse
flex-direction
    Specifies direction of the items inside a flex container
    Values: row, row-reverse, column, column-reverse
justify-content
    Horizontally aligns the flex items
    Values: flex-start, flex-end, center, space-between, space-around
flex-flow
    Shorthand property for flex-direction and flex-wrap
    - flex-flow: flex-direction flex-wrap
align-content
    Modifies behavior of the flex-wrap property
    Values: stretch, center, flex-start, flex-end, space-between, etc
align-items
    Vertically aligns the flex items
    Values: stretch, center, flex-start, flex-end, baseline
order
    Specif order of a flexible item relative to the rest
    - Value: number. default = 0.

### Grid

Offers a grid-based layout system, with rows and columns, making it easier to design web pages

Grid creates 2d grid layout (good for page layouts)
column-axis
row-axis
grid-container
grid-items

```css
.parent{
    display: grid

    grid-template-columns: 1fr 1fr 1fr 1fr;     (four columns)
    grid-template-columns: repeat(4, 1fr);
    grid-template-rows: 1fr 1fr;    (two rows)

    gap: 10px;   (previously grid-gap)
    column-gap: 
    row-gap: 

    justify-items: stretch(default), start, center, end
    align-items: 

    (Use to align grid inside container (applies if container > grid)) :
    justify-content: stretch(default), center, end
    align-content: 
}

.child{
    grid-column: 1 / 4
    grid-row: 

    justify-self: stretch(default), start, center, end
    align-self: 
}
```

- grid: grid-template-rows -template-columns -template-areas -auto-rows -auto-columns -auto-flow

grid-template-columns
    Specifies no(& widths) of columns in a grid layout.
    -Values: none, auto, max-content, min-content, length
grid-template-rows
    Specifies no(& heights) of the rows in a grid layout.
    -Values: none, auto, max-content, min-content, length
grid-auto-flow
    Controls how auto-placed items get inserted in grid
    -Values: row, column, dense, row dense
grid-template
    Shorthand property for the grid template properties
    -grid-template: grid-template-rows, -template-columns
grid-auto-rows
    Sets a size for the rows in a grid container
    -Values: auto, max-content, min-content, length
grid-auto-columns
    Sets a size for the columns in a grid container
    -Values: auto, max-content, min-content, length
grid-row
    Shorthand property for the grid-row properties
    - grid-row: grid-row-start grid-row-end
grid-column
    Shorthand property for the grid-column properties
    - grid-column: grid-column-start grid-column-end

#### Grid-Area

Specifies a grid item's size and location in a grid layout. Shorthand property for:

- grid-area: grid-row-start, grid-column-start, grid-row-end, grid-column-end
    grid-row-start
        Specifies on which row to start displaying the item
        -Values: auto(default), row-line
    grid-column-start
        Specifies on which column to start displaying the item
        -Values: auto(default), span n, column-line
    grid-row-end
        Specifies on which row-line to stop displaying the item
        -Values: auto(default), span n, column-line
    grid-column-end
        Specifies on which column-line to stop displaying item
        -Values: auto(default), span n, column-line

#### Grid-Gap

Defines the size of the gap between the rows and columns in a grid layout

- grid-gap: grid-row-gap, grid-column-gap.
    grid-row-gap
        Sets the size of the gap b/n rows in a grid layout
        -Values: length(px, etc), %. 0 is default
    grid-column-gap
        Sets the size of the gap b/n columns in a grid layout
        -Values: length(px, etc), %. 0 is default

## style.css

```css

*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
html{
    font-size: 62.5%;
    scroll-behavior: smooth;
}
body{
    font-size: 1.6rem;
    font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;

    /* CSS box-model : Content(Height Width) Margin Border Padding */
    
    box-sizing: border-box;
    
    width: 50%;
    height: 400px;

    margin: 23px 54px 60px 0px;
    /* top right bottom left */
    margin-top: 5px;
    margin-left: 10px;
    margin-left: auto; /*stuff covers the right side upto need, leaving space in left*/

    margin: auto;  /*makes it center from left-right(horizontally)*/
    text-align: center;
    justify-content: center;

    padding: 23px 54px 60px 0px;
    /* top right bottom left */
    padding-top: 5px;
    
    border: 3px solid red;
    border-top: 2px dashed orange;
    border-width: 3px;
    border-radius: 5px;
    border-style: solid;
    border-color: red;
    
    outline: 4px solid black;  /*It's outside border*/

    box-shadow: 0 0 12px 12px rgba(0, 0, 0, 0.05);


    /* Font */ 
    /* font: style variant weight size family; */
    font-family: sans-serif;
    font-style: italic;
    font-size: 16px;

    /* Text properties */
    color: blue;
    text-align: left;
    text-decoration: none;
    text-transform: uppercase;
    text-indent: 0.5cm;
    letter-spacing: 2px;
    word-spacing: normal;
    /* text-shadow: hoff voff blur #000; */
    text-shadow: 0 0 12px rgba(0, 0, 0, 0.05);
    direction: ltr;


    /* display */
    display: block;
    display: inline;  /*To make stuffs in one line : like navbar list*/

    display: none; /* Hides without taking any space */
    visibility: hidden; /* Hides taking the amout of space needed */


    max-width: fit-content;

    /* position */
    position: absolute;
    position: relative;
    position: fixed; /*make something fixed, even while scrolling*/

    float: left;


    /* flex box */
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center; /*horizontally center*/
    align-items: center; /*vertically center*/

    /* grid */
    display: grid;
    grid-template-columns: repeat(4, 1fr);


    /* color & bg */

    color: cyan;
    color: rgb(23, 183, 211);
    color: #2393dd;
    
    color: hsl(hue, saturation, lightness);
    color: hsla(hue, saturation, lightness, alpha);
    
    color: hsl(98, 69%, 59%);
    color: hsla(98, 69%, 59%, 0.2s);
    
    color: rgb(red, green, blue);
    color: rgba(red, green, blue, alpha);
    
    color: rgb(rgb(146, 73, 73), rgb(72, 189, 72), rgb(20, 20, 161));
    color: rgba(rgb(146, 73, 73), rgb(72, 189, 72), rgb(20, 20, 161), 0.2);
    

    /* background: color image repeat attachment position; */
    background: black url('img/bg.jpg') no-repeat right top fixed;
    background-color: black;
    background-image: url('img/bg.jpg');
    background-repeat: no-repeat;
    background-position: right top;
    background-attachment: fixed;


} 


#id{
    color: #fff;
}
.class{
    color: #000;
} 

/* selector is : all h1 inside Class named .class */
.class h1{
    color: #000;
} 
.class > h1{
    color: #000;
} 

/* selector is : Class named .class & all h1 */
.class, h1{
    color: #000;
} 

/* ----- */


img{
    filter: blur(1px);
    /* blur brightness contrast drop-shadow grayscale invert hue-rotation opacity saturation sepia */
}

/* hover */
a:hover{
    background-color: rgb(3, 141, 49);
    /* bg-color of <a> links will change greenish on hovering */
}
a:active{
    font-size: 3em;
    /* font-size will change to 3em on click */
}
a:visited{
    color: gray;
    /* text-color will change to gray after visiting the link */
}

/* Responsive on different screen size */
@media only screen and (max-width:1199px){}
@media only screen and (max-width:999px){}
@media only screen and (max-width:768px){}
@media only screen and (max-width:600px){
    /* changes of css codes selectors and values here at screen size around 600px */
}

/* latest way is to use max-width for responsiveness. */


.nothing{
    margin: 23px 54px 60px 0px;
    padding: 5px 30px 6px 4px;
    border: 4px solid red;
    border-radius: 5%;

    color: deepskyblue;
    background: #000 url('img.png') no-repeat fixed right top;
    font: italic bold .8em/1.2 Ariel , sans-serif;

    display: none inline block inline-block flex grid;
    display: -webkit-box;
  
    z-index: 0;
    justify-content: center;

    text-align: center;
    text-decoration: none;
    line-height: 1.4;
    text-rendering: optimizeLegibility;

    box-sizing: border-box;
    box-shadow: inset 0 -2px #F2B139;

    max-width: 100%;
    outline: 0;
    
    -webkit-transition: 0.3s;
    transition: 0.3s;
}

.css{
    /* color : rgb hex hsl (a-alpha) */
    color: red;
    color: rgb(255, 0, 0);
    color: #ff0000;
    color: #f00; /*use when all hex_values are repeative like ff dd 00 44*/
    color: hsl(0, 100%, 50%);
    /* with a-alpha value for transparency */
    color: rgba(255, 0, 0, 0.2);
    color: hsla(0, 100%, 50%, 0.2);

    /* BG */
    background-color: green;
    opacity: 0.6; /*background-color opacity value : 0 to 1; Note: all child elements inherit same transparency*/
    background-color: rgba(0, 255, 0, 0.6); /*using rgba it doesn't effect its child elements (only bg)*/
    background-image: url('img.png');
    background-repeat: no-repeat;
    background-position: 0 0;
    background-position: right top;
    background-attachment: fixed;
    background: rgba(0, 255, 0, 0.6) url("img.png") no-repeat right top;    /*Shorthand*/
    /* color image repeat position */
    /* background-attachment: fixed; USED separately */
    background-clip: padding-box;   /*how far bg should extend*/
    background-origin: content-box; /*origin position of a bg_img; Note: no-effect on background-attachment:fixed;*/
    background-size: contain;   /*size of bg_img*/

    /* BORDER */
    border-style: solid;    /*IMP: No other 'border' properties will work without style*/
    border-left-style: solid;   /*try this in blue to a <p>*/
    border-style: dotted solid;
    /* top-bottom right-left */
    border-style: solid none double dashed;
    /* top right bottom left */
    border-width: 2px;  /*px pt cm em..., thin medium thick*/
    border-width: 5px 20px;
    /* top-bottom right-left */
    border-width: 25px 10px 4px 35px;
    /* top right bottom left */
    border-color: green;
    border-color: red green blue yellow;
    /* top right bottom left */
    border: 6px solid red;  /*Shorthand*/
    /* width style color */
    border-bottom: 1px solid #000;
    border-radius: 5px;

    /* margin & padding */
    /* units: px,pt,cm,.. % */
    /* inherit: from parent element like <p>or<h1>from<div>from<body>*/

    /* MARGIN */
    margin: 23px 54px 60px 0px;
    /* top right bottom left */
    margin: 8px 3px;
    /* top+bottom right+left */
    margin-top: 5px;
    margin: auto;   /*horizontally center the element within its container*/
    /* Margin collapse, two margin of close elements collapse into one (largest of the two)*/
    
    /* PADDING */
    padding: 23px 54px 60px 0px;
    /* top right bottom left */
    padding: 8px 3px;
    /* top+bottom right+left */
    padding-left: 5px;
    /* if element has width/height padding will add extra (total width/height = width/height + padding)*/
    /* to keep width value, use box-sizing: border-box;*/

    /* HEIGHT/WIDTH */

    
    /* Shorthand properties  */
    margin: 23px 54px 60px 0px;
    /* top right bottom left */
    margin: 8px 3px;
    /* top+bottom right+left */

    padding: 5px 30px 6px 4px;
    /* top right bottom left */
    padding: 8px 3px;
    /* top+bottom right+left */

    border: 4px solid red;
    /* width style color */

    background: #000 url('img.png') no-repeat right top;
    /* color image repeat position */
    /* background-attachment: fixed; USE separately */

    font: italic bold .8em/1.2 Ariel , sans-serif;
    /* style weight size line-height family */

}

```
