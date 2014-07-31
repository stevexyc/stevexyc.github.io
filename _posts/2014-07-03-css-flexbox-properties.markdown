---
layout: post
title:  "CSS FlexBox Properties"
date:   2014-07-03 11:37:26
categories: css3
image: code-css.jpg
excerpt: A quick reference of css-flex properties
---

# CSS FLEX BOX 
is a new method to layout, align and distribute space among items in a container, even when their size is unknown and/or dynamic. It arose out of the many screen sizes available today. 


## Container (parent) properties

### display
initiate the flex layout

<pre><code>
  {% highlight css linenos %}
  .container {
    display: flex; /* inline-flex */
  }
  {% endhighlight %}
</code></pre>

### flex-direction
the direction of the flex

	.container {
		flex-direction: 
        row | row-reverse | column | column-reverse;
	}

row: left to right
row-reverse: right to left
column: top to bottom 
column-reverse: bottom to top

### flex-wrap
items will all try to fit onto one line, unless you define it by allowing items to wrap

	.container {
    	flex-wrap: 
        wrap | nowrap | wrap-reverse
    }

### flex-flow 
a shorthand for flex-direction and flex-wrap

	.container {
    	flex-flow: <'flex-direction'> || <'flex-wrap'>
        /* default: row nowrap */
    }

### justify-content
defines alignment along the main axis (defined by flex-direction)

	.container {
    	justify-content: 
        flex-start (default) | flex-end | center 
        | space-between | space-around
    }

- ** flex-start **: items are aligned to start line
- ** flex-end **: items are aligned to end line
- ** center **: items are centered along the line 
- ** space-between **: items evenly distributed in the line, first item at start line, last item on the end line
- ** space-around **: items are evenly distributed in the line with equal space around them


### align-items
defines default behaviour for how flex items are laid out along the cross-axis on the current line. 

	.container {
    	align-items: 
        flex-start | flex-end | center | baseline 
        | stretch (default)
    }
    
### align-content 

	.container {
    	align-content: 
        flex-start | flex-end | center | space-between | space-around
        | stretch (default)
    }


---------------------------


## Item (child) properties

### order
control the order of items

	.item {
		order: <integer>
	}


### flex-grow
allow item to grow in size if necessary

	.item {
    	flex-grow: <number> /* default 0 */
    }

if all child elements have flex-grow = 1, then they all have equal size, but if one were to have a flex-grow =2, then it will be twice as large as the others. 

### flex-shrink
allow item to shrink if necessary

	.item {
    	flex-shrink: <number> /* default 1 */
    }

### flex-basis
defines the default size of element before remaining space is distributed 

	.item {
    	flex-bases <length> | auto /* default auto */
    }

### flex 
shorthand for flex-grow, flex-shrink, flex-basis. flex-shrink and flex-basis are optional. Default is 0 1 auto;

	.item {
    	flex none | [<'flex-grow'>] <'flex-shrink'>? || <'flex-basis'> ]
        /* default: 0 1 auto */
    }

### align-self 
allows the default alignment (assigned by align-items) to be overridden for individual items. 

	.item {
    	align-self: auto | flex-start | flex-end | center | baseline | stretch
    }












