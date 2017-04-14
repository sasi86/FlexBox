# FlexBox

FlexBox Basic:

FlexBox is all about the relationship b/w the parent container and i.e., Flex container and its direct decendent child items i.e., flex items

To display a div as a Flex container user property display : flex/inline-flex {inline/block/Table/Cell}


properties on flex container

Flex Direction:
==============

1. In the container Flex items by default flow from left to right on the Main Axis. To control this direction of flow use property flex-direction

flex-direction : {row/row-reverse/column/column-reverse}

Flex Line Wrapping
==================

2. flex items can be wraped if the container width/height is not enough. To control wrapping of items inside the container use property flex-wraped

flex-wrap : {wrap/wrap-reverse/nowrap(flow in a single line on the main axis)}

Shorthand:
=========

Shorthand for to combine flex-direction and flex-wrap

flex-flow : column wrap { row/row-reverse/column/column-reverse wrap/wrap-reverse/nowrap }

Display Order:
==============

All the flex items by default have an order of 0. If order is same for more than one flex-item then the order is determined by the order in the source code 
see example 3.

Note: The changes only visual re-ordering and not the logical re-ordering(source code)

order : {...-1,0,1....}

Example 1:

div1 - order : 0
div2 - order : 0
div3 - order : 0
div4 - order : 0

All div placed in order-group-0

div1 div2 div3 div4

Example 2:

div1 - order : 0
div2 - order : 0
div3 - order : 1
div4 - order : 0

div1,div2,div4 placed in order-group-0
div3 placed in order-group-1

div1 div2 div4 div3

Example 3:

div1 - order : 0
div2 - order : 1
div3 - order : 1
div4 - order : 0

div1,div3,div4 placed in order-group-0
div2 and div3 placed in order-group-1

div1 div4 div2 div3

Flexibility:
============


flex-grow property makes the flex-items grow by the given number for this property to fill the available space.

flex-grow factor which controls how much a given item in a row or column will strech relative to the other items within their row or column in order to fillup the
postitive free space 

flex-shrink factor it controls how the space is distributed when there is not enough space for the items to fit 

flex-basis sets the initial size of the item before the extra space is distributed. It shares many similarity with the width property even uses the exact same
unit as width.


Shorthand:
==========

flex : flex-grow flex-shrink flex-basis


Alignment:
==========

flex-box alignment can be handled in two different ways.

1. It can be applied to all the flex-items in the given container(justify-content, align-items, align-content)
2. It can be applied to the individual flex-items themselves(align-self)

property(applied on the container)
justify-content : {flex-start/flex-end/center/space-between/space-around}

Allows to align the flex-items along the main axis(horizontal and runs left to right). Always streches the flex-items to full container unless flex-items 
have specific heights.


property(applied on the container)
align-items : {flex-start/flex-end/center/strech/baseline(if we have text in the items and align the items to the baseline of the text use this)}
 
Allows to align the flex-items along the cross axis(vertical and runs top to bottom)	

property(applied on the item)
align-self  : {flex-start/flex-end/center/strech}


property

When flex-items that wrap on to muliple lines 

div-container {display :  flex-wrap; wrap}



Main Axis - flow from flex start(left) to flex end(right)

cross axis(vertical and runs top to bottom)	
