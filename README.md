## 02

Gerneral form

```
selector {
    property: value;
    property2: value;
}
```
```selector```
- can be name of html element
  - ```
    b{

    }
    ```
- can be class name of html element 
- to tell css that the name is class we put dot ```.``` before
  - ```
    .class-name {

    }
    ```
- can be id of html element 
- <b>Caution This is not a best practise to use id as selector</b>
- to tell css that the name is id we put hash ```#``` before
  - ```
    #id-name {

    }
    ```

----

## 03

To specify certin class of certin html element
```
htmlElement .calss-name
{

}
```

style can be used in 3 way
1. external
    ``` 
    <link rel="stylesheet" href="css/main.css">
    ```
2. internal
    ``` 
    <style>

    </style>
    ```
3. inline 
   - <b>Caution This is not a best practise to use inline</b>
   - inline style will override other styles
    ``` 
    <htmlelement style="           "></htmlelement>
    ```

----

## 04

identifiers: any thing u can recognize htmlelement by like ```id``` and ```calss```
   -   cannot start with number
   -   can start with Hyphen```-``` or underscoer ```_``` or any english letter```[a-z]```
   -   don't use camelcase letter u can use Hyphen```-``` or underscoer ```_``` to seprate word instead

----

## 05

colors
   - u can select color by name if its name avliable like ```color: red;```
   - u can use ```rgb(r g b)``` each value start from 0 to 255 if u want alpha u can use for example ```rgb(r g b / 10%)```
   - u can use hex value  like ```#RRGGBB``` each value start from 00 to FF  if u want alpha u can use ```#RRGGBBAA```

using file inside css by ```url(" ")```

----

## 06

```background-attachment``` controls how image will behave while scroll
  - ```fixed``` image will be shown while scroll
  - ```scroll``` image will be scrolled

----

## 07

direction in css is
``` Top Right Bottom Left```

u can imagine it like clock ```clockWise```

```
----  Top  ----
----------------
Left ---- Right
----------------
---- Bttom ----
```

any non given value will take its value from the one it meets

```padding``` dosnot allow negative values

----

## 08

```margin``` allow negative values

if u for example specify container width as 70% of screen
and want to center it u can do that

 ```
 div{
   width: 70%;
   margin-left: 15%;
 }
 ```

 best practise

 ```
 div{
   width: 70%;
   margin-left: auto;
 }
 ```
 the browser will calculate the value

 ----

## 09

```border``` and ```outline```
- Outline dosen't effect the element sized
- Not best practise to use outline from css v3 new feature make it posible that border dosen't effect the element sized ```flex```
- outline is limited compare to ```border``` u can edit every direction of ````border``` but ```outline``` not

----

## 11

Display

- Block
  - Dosen't allow element beside it
  - Take full width if no width
  - Add line break before element
  - Respect all property

- Inline
  - Allow element beside it
  - Don't respect width or height
  - DO not add line break before element
  - Respect padding and margin only left and right

- InlineBlock
  - Allow element beside it
  - Respect width or height
  - Add line break before element
  - Respect all property

----

## 12

u can hide element by 2 ways

- ```dispaly: none```
  - element will be deleted from tree || hide and its place disapper

- ```visibility: hidden```
  - element will not be deleted from tree || hide and its place still shown

----

## 13

grouping u can group multipule selector like that

```
selector01, selector02, selector03, selector04{

}
```

----

## 13

Nesting selector

```
selector01 selector02 selector03 selector04{

}
```
mean apply this on selector04 which lay in selector03 which lay in selector02 which lay in selector01

----

## 15

dimension

```fit-content``` to fit content inside element

----

## 16

```overflow```

controls overflow elements in current element
  -```hidden``` hide overflowed content  
  -```visible``` show overflowed content <b>"Default value"</b>  
  -```scroll``` show scrollbar to scroll
  -```auto``` show scrollbar only if content overflowed but hide if not
 u can control each direction by using ```Overflow-X``` and ```Overflow-Y```

 ----

## 22

if u want to inherit any value from upper element in the tree use ```inherit```
like

```
.div {
  padding: 20px;
}
.div .p {
  padding: inherit;
}
```

here ```p``` element inside ```div``` element will inherit padding value from ```div```

----

## 22

Position

```static``` 
- default value of postion
- top rigth bottom left don't affect

```relative```
- move depend on his postion
- it required to put it into parent div to make element move depend on it
  - if u delete it the child element will move depednd on nearest parent

```absolute```
- element out of workflow
- move depened on page

```fixed```
  - move depednd on page regardless where it is 
  - move with u while scroll
for example button to go to top of the page

```sticky```
  - fixed at its postion
  - make u scroll screen but when arrive to that element it will be sticky with u
  - requires place to be sticked to use ```top``` or ```left``` .. etc

for example nav bar

----

## 35

Pseudo Elements

```first-letter```

to deal with first letter in element

```first-line```

to deal with first line in element

```selection```

what happen with element when selected

```before``` & ```after```

to show them u must set ```content:""``` property
----

## 37

```counter( )```
  - ```member-counter``` to show count of element

```attr( )```


----

## 41

The default behavouir of any element it add padding and margin to the width and height  of the element
  if u want to have const height and width when u change padding use ```box-sizing: border-box;```


To use ```box-sizing``` u might need to apply this code

```
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
```

If u have some property u want to apply it to all html element u can use this
  
```
* {

}
```

----

## 43

```
  // Time of change
  transition-duration: 1s;
```

```
  // delay taken to start transtion
  // u can define multipule times separeted by comma ,
  transition-delay: 0.2s;
```

```
  // which function will run to start transion
  transition-property: width;

  // u can define multipule property separeted by comma ,
  transition-property: width, height;
```

```
  // curve of transition time
  transition-timing-function: ease-in-out;

  // compact property [property | Delay | duration | function]
  transition: all 2s 0.5s linear;
```

u can for example say that i want transion in width finish in 3s and hight in 2s like this
```
  transition: width 3s,height 2s;
```

----

## 43

```! important``` declaration u can use it to mark property as important to override any style exsits with change in the same property

  - if u are an expert person and u build all style from scratch u may not use this decleration
  - if u modify others page and u haven't access to source html or main style u may use it many and many 

----

## 44

The margin collapse
  - [1] Only vertical margin collapse
  - [2] Bigger margin wins
  - [3] Collapsing work with element with no thing between

----

## 45

CSS Variables
  - Global Variable
  - Local Variable

to decalre global variable
```
:root {
  --variableName : value;
}
```

to decalre Local variable
```
element {
  --variableName : value;
}
```

to use variable we use ```var(Variable Name, Fall Back Value)```
  - fallback: like default value or value to apply if varibale currapted or not exsist

----

## 46 - 47

Flexible Box

  For Parent
  - display: flex => To Start Flexible Box
  - flex-direction: row => Default Value
  - flex-wrap: nowrap => Default Value
    - what to do with bouns element
  - flex-flow: [Flex-Direction] + [Flex-Wrap]
  - justify-content: flex-start => Default Value
    - organize element horizontaly
  - align-items: stretch => Default Value
    - organize element verticaly
  - align-contents: stretch => Default Value
    - Deals with content

  For Child
  - flex-grow: 0 => Default Value
  - flex-shrink: 1 => Default Value
  - order: 0 => Default Value
    - change order of element inside flex
  - flex-basis: auto => Default Value
    - deals with width when hor or height when ver0.3
    - .0


3
  - flex: [Flex Grow] [Flex Shrink] [Flex Basis] 0 1 Auto
  - align-self: auto => Default Value
    - override align-items for certin content


----

## 54

Filters

```filter: grayscale(0-100)```

```filter:blur()```

```filter:invert(0-100%)```

and there is more but first check browsers compabilty


----

## 55
Gradients

```background-image: gradient```

Linear
```linear-gradient(Direction||Angle , color stop 1, color stop2, .....)```
  -Direction||Angle
    - ```to top``` u can use ```to``` + ```top``` or ```right``` ....
    - ```0deg```
  - Color stop 1
    - u can specify percentage after color for example ```red 80%```
    - u can specify distance after color for example ```red 300px```


----

## 55

Caret Color
  - change mouse cursor color ```caret-color:```

Pointer Events 
  - use for  example to disable mouse interacte with element

----

## ??-62

Grid 

  For Parent
  - ```display: grid```
    - to start grid
  - ```grid-template-columns:``` number of columns in grid in 
    - ````...px```` 
    - ```..%``` 
    - ```Auto``` is shy and take size to fit content
    - ```fr``` is greedy
    - ```repeat(number,...)``` 
    - Mix all pervouis
  - ```grid-template-row:``` number of rows in grid in 
    - ````...px```` 
    - ```..%``` 
    - ```Auto``` is shy and take size to fit content
    - ```fr``` is greedy
    - ```repeat(number,...)``` 
    - Mix all pervouis
  - ```row-gap:```
  - ```column-gap:``` 
  - ```gap:``` is short hand for two prevoius  
  - ```justify content:```  
  - ```align-items:```
  - ```grid-template-area:``` ```"%% %% . %%"```
    - ```%%``` set any name u want but add this peroperty in css code of element ```grid-area: %%```
    - Dot ```.``` mean leave this e=column empty

  For Child
  - ```grid-column: 1 / 7``` mean start from 1 end at 7 this is shorthand for ```column-start``` and ```column-end``` be careful if u use ```1/7``` and column end greater that exsiting column it will add new one it's safe to use ```span 7``` it will start from current and take 7 column 
    - u can use ```2 / span 4``` to select start and how many column to take if column required is greater that exsisting element will go to next row
  - ```grid-area:``` [row start / row end / col start / col end]

----

## 63

Min, Max And Auto Fill
```minmax(minVal,maxVal)``` use with col and rows

```auto-fill``` will auto fill element depend on avaliable space

~~search on ur own~~
```auto-fit```

----

## 69

Matrix
```matrix(scaleX(),skewY(),skewX(),scaleY(),translateX(),translateY())```

---

## 78 - 82

```transform-style: preserve-3d;```

We use this to make element save its postion in 3d

---

## 78 - 82

CSS Selectors
  - *
  - Element => [p, div, h2]
  - Element OtherElement => div p
  - .class-name
  - #id-name
  - .parent .child
  - .class-one.class-two
  - .class-name div, .class-name p
  - Element.class-name => p.class-name
  - .parent > .child => Direct Child
  
  - Element + Other Element => [div + p]
  - Element ~ Other Elements => [p ~ div]
  - [Attribute]
  - Element[Attribute]
  - [Attribute=Value]
  - Element[Attribute=Value] => input[type="submit"]
  - [Attribute~=Value] => Contains A Word
  - [Attribute*=Value] => Contains A Atring
  - [Attribute^=Value] => Start With A String

  - :first-child
  - :last-child
  - :first-of-type
  - :last-of-type
  - :only-child

  - :not(Selectors)
  - :nth-child(n)
  - :nth-last-child(n)
  - :nth-of-type(n)
  - :nth-last-of-type(n)

  - :root
  - :checked
  - :empty
  - :disabled
  - :required
  - :focus
  - ::selection
  - ::placeholder

---

## 84

```
@media (min-width: ){

}
```

Mobile
```max-width: 767px```

small screens
```min-width: 768px```

meduim screens
```min-width: 992px```

Large screens
```min-width: 1200px```

---

## 87

  CSS Global Values
  - inherit
  - initial
  - unset
  --- If Inherit => inherit
  --- If Not => initial
  - revert CSS Level [4]
  - all