### A review of the current grid systems

right now, the way to use the grid/layout system is like this 

	<div class="row">
    	<div class="col-xs-12 col-sm-6 col-md-3 col-lg-3">
        	<div class="panel">
            	etc...
            </div>
        </div>
    </div>

But is that the ideal way to write code?

I would contend that the ideal way to write code is to make it much more expressive. There is already a lot of code already just to create a row and and a div inside. How about, if we can do something like this... 

	<row>
    	<column xs=12 sm=6 md=3 lg=3>
        	<panel>
            	etc...
            </panel>
        </column>
    </row>

Again, this already looks much better. And i would contend that you can have more options. For example, in bootstrap, classes define everything. 

	<div class="col-xs-12 col-sm-6 col-md-3 text-center visible-sm-only sr-only">

However, if we use the attribute system, we can write 

	<column xs=12 sm=6 md=3 text-center visible-sm-only sr-only>

Yes, the only difference may be the difference in quotations, but still, I believe it is quite an improvement, especially when it comes to more complex components. 

Plus, lets not forget with web components and css-flex, we can simply write 

	<column xs=12 sm=6 md=3 order-xs=1 order-sm=2 order-md=5>

### So, what is the proposed project?

Well, my idea is to combine css-flex-grid with web-components. Why would we do this? well it simplifies the code dramatically. I theorize that once people start using the new system, they will not turn back. Although some may say it is a simple improvement, I suggest that it is actually quite a big one because it fundamentally changes how code is written. 

Web components will allow us to create our own tags, (ie <row>, <column>) and we can utilize its attribute functionality (ie. xs=12 order=6). 

Css flex, although not yet adopted by all the browsers out there, is the future. It allows us to position, align, and order our objects so much easier. Combining the two will provide the best of both worlds. 

### How do I get started?

well to begin, i must get familiar with web components again. I made a shitty component a while back but I have since forgotten most of it. I have to learn css properties work in web components (ie polymer)

Also, I must get used to css-flex. I know that the grid system is not something that's fairly complex, but still, there are a lot of variety in how people use the grid. So it would be best to come up with a flexible solution. 


































-
