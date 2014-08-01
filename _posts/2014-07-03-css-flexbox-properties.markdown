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

## Overview 
{% highlight css %}
.container {
  display: flex;
  flex-direction: row | column;
  flex-wrap: wrap | nowrap | wrap-reverse;
  justify-content: flex-start | flex-end | center | space-between | space-around; 
  align-items: flex-start | flex-end | center | baseline | stretch; 
}

.item {
  order: <integer>;
  flex-grow: <integer>;
  flex-shrink: <integer>;
  flex-basis: <length> | auto;
  align-self: auto | flex-start | flex-end | center | baseline | stretch;
}

{% endhighlight %}


## Container (parent) properties

__display__: initiate the flex layout

{% highlight css %}
.container {
  display: flex; /* inline-flex */
}
{% endhighlight %}

__flex-direction__: the direction of the flex

{% highlight css %}
.container {
  flex-direction: 
      row | row-reverse | column | column-reverse;
}
{% endhighlight %}

row: left to right
row-reverse: right to left
column: top to bottom 
column-reverse: bottom to top

__flex-wrap__: items will all try to fit onto one line, unless you define it by allowing items to wrap

{% highlight css %}
.container {
  flex-wrap: 
    wrap | nowrap | wrap-reverse
}
{% endhighlight %}

__flex-flow__: a shorthand for flex-direction and flex-wrap

{% highlight css %}
.container {
  flex-flow: <'flex-direction'> || <'flex-wrap'>
    /* default: row nowrap */
}
{% endhighlight %}

__justify-content__: defines alignment along the main axis (defined by flex-direction)

{% highlight css %}
.container {
  justify-content: 
    flex-start (default) | flex-end | center 
    | space-between | space-around
}
{% endhighlight %}

- _flex-start_: items are aligned to start line
- _flex-end_: items are aligned to end line
- _center_: items are centered along the line 
- _space-between_: items evenly distributed in the line, first item at start line, last item on the end line
- _space-around_: items are evenly distributed in the line with equal space around them


__align-items__: defines default behaviour for how flex items are laid out along the cross-axis on the current line. 

{% highlight css %}
.container {
  align-items: 
    flex-start | flex-end | center | baseline 
    | stretch (default)
}
{% endhighlight %}
    
__align-content__ 

{% highlight css %}
.container {
  align-content: 
    flex-start | flex-end | center | space-between | space-around
    | stretch (default)
}
{% endhighlight %}


## Item (child) properties

__order__: control the order of items

{% highlight css %}
.item {
  order: <integer>
}
{% endhighlight %}


__flex-grow__: allow item to grow in size if necessary

{% highlight css %}
.item {
  flex-grow: <number> /* default 0 */
}
{% endhighlight %}

if all child elements have flex-grow = 1, then they all have equal size, but if one were to have a flex-grow =2, then it will be twice as large as the others. 

__flex-shrink__: allow item to shrink if necessary

{% highlight css %}
.item {
  flex-shrink: <number> /* default 1 */
}
{% endhighlight %}

__flex-basis__: defines the default size of element before remaining space is distributed 

{% highlight css %}
.item {
  flex-bases <length> | auto /* default auto */
}
{% endhighlight %}

__flex__: shorthand for flex-grow, flex-shrink, flex-basis. flex-shrink and flex-basis are optional. Default is 0 1 auto;

{% highlight css %}
.item {
  flex none | [<'flex-grow'>] <'flex-shrink'>? || <'flex-basis'> ]
    /* default: 0 1 auto */
}
{% endhighlight %}

__align-self__: allows the default alignment (assigned by align-items) to be overridden for individual items. 

{% highlight css %}
.item {
  align-self: auto | flex-start | flex-end | center | baseline | stretch
}
{% endhighlight %}












