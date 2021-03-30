# Responsive Web Design and Regular Expressions


**Regular expressions (regex or regexp)** are extremely useful in ***extracting information*** from any text by searching for one or more matches of a specific search pattern

* **One of the most interesting features** is that once you’ve learned the syntax, you can actually use this tool in (almost) all programming languages ​​(JavaScript, Java, VB, C #, C / C++, Python, Perl, Ruby, Delphi, R, Tcl, and many others) with the slightest distinctions about the support of the most advanced features and syntax versions supported by the engines).

## Basic topics
*  ^ and $

    * ^The        matches any string that starts with The 
    * end$        matches a string that ends with end
    * ^The end$   exact string match (starts and ends with The end)
    * roar        matches any string that has the text roar in it

    + ? and {}
    * abc*        matches a string that has ab followed by zero or more c 
    * abc+        matches a string that has ab followed by one or more c
    * abc?        matches a string that has ab followed by zero or one c
    * abc{2}      matches a string that has ab followed by 2 c
    * abc{2,}     matches a string that has ab followed by 2 or more c
    * abc{2,5}    matches a string that has ab followed by 2 up to 5 c
    * a(bc)*      matches a string that has a followed by zero or more copies of the sequence bc
    * a(bc){2,5}  matches a string that has a followed by 2 up to 5 copies of the sequence bc

* OR operator — | or []
    *  a(b|c)     matches a string that has a followed by b or c (and captures b or c)
    *  a[bc]      same as previous, but without capturing b or c    

   

 ## A Complete Guide to Grid
* display 
    
    .container {
    display: grid | inline-grid;
    }
   
* grid-template-columns
* grid-template-rows


.container {
  grid-template-columns: 40px 50px auto 50px 40px;
  grid-template-rows: 25% 100px auto;
}


* justify-content


.container {
  justify-content: start | end | center | stretch | space-around | space-between | space-evenly;    
}





## Common Responsive Layouts with CSS Grid (and some without!)
The `repeat()` function takes two arguments, the first will define the number of column tracks and the second, what width the tracks should be.
In this case, for the first argument, I’ve used auto-fill which will create a grid with as many tracks as will fit into the container. The second argument, which defines the width of the tracks, I’ve set to minmax(250px, 1fr). The minmax function will create track widths that can be a minimum of 250px wide and a maximum of 1fr. An fr is a ‘fraction unit’, a unit of measurement to define a fraction of the available space of the container. The width of the elements in the row will increase from 250px until the point where another element could potentially fit beside the first. Try changing the width of your browser while looking at the example to see this in action.
`grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));`

Often when we put images in a responsive grid layout like this we come across the problem of the images stretching out of proportion. Using

can help here, as that will stop the image from stretching, but it will cause cropping to happen. What we end up with is equally sized grid ‘cells’ which will fill increasing numbers of columns as the page width increases.
The final thing of note here is the grid-gap property. This defines the size of the space between the columns and the rows. This will affect the number of elements that will fit in a track, so you may need to adjust your minmax sizes accordingly. To create similar gaps between elements with flexbox we currently have to use a combination of margin and the justify-content properties, however column-gap and row-gap are in the works.
The rest of the position styling in this example has been done using flexbox, as these are one dimensional layouts. Flexbox is still my favourite tool for vertically centering elements on the page. Grid is brilliant for creating grids, but it doesn’t mean that our other layout tools are no longer necessary.

