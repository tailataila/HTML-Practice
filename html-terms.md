**HTML** stands for HyperText Markup Language and is used to create the structure and content of a webpage. A markup language is a computer language that defines the structure and presentation of raw text. HyperText is text displayed on a computer or device that provides access to other text through links, also known as hyperlinks.

**Element** — a unit of content in an HTML document formed by tags and the text or media it contains. HTML is composed of elements. These elements structure the webpage and define its content.

**Tag** is a set of characters constituting a formatted command for a web page.

Opening Tag — the first HTML tag used to start an HTML element. The tag type is surrounded by opening and closing angle brackets.

Content — The information (text or other elements) contained between the opening and closing tags of an HTML element.

Closing tag — the second HTML tag used to end an HTML element. Closing tags have a forward slash (/) inside of them, directly after the left angle bracket.

HTML is organized as a collection of family tree relationships.
When an element is contained inside another element, it is considered the *child* of that element. The child element is said to be nested inside of the *parent* element.
*Hierarchy* - the relationship between elements and their ancestor and descendent elements.

**Attributes** can be added to the opening tag of an HTML element to change its default behavior or provide additional data about it.  Attributes are made up of the following two parts:
- The name of the attribute
- The value of the attribute

< p > - paragraph element = TAG and CONTENT in between

< p >< span > - відокремити частину тексту, але не розділ

< body >
< h1 > - heading largest, < h6 > - smallest
  
< div > division or a container that divides the page into sections. < div >s allow us to group HTML elements to apply the same styles for all HTML elements inside
id="text" - attribute identify
< em > - emphasize - italic
< strong > - highlight = bold
< br > - spacing
< ul > < li > < /li > < /ul > - unordered list
< ol > < li > < /li > < /ol > - ordered list
< img src="" alt="" / > - src - URL, alt - image description

< a href="URL" target="_blank" >Link Name</a > - URL, target attribute blank - open in new window

**Video**

< video src="myVideo.mp4" width="320" height="240" controls >
  Video not supported
< /video > - The controls attribute instructs the browser to include basic video controls such as pausing and playing.  The text, Video not supported, between the opening and closing video tags will only be displayed if the browser is unable to load the video.

**Audio**

< audio autoplay controls >

  < source src="iAmAnAudioFile.mp3" type="audio/mp3" >
  
< /audio >

List of audio attributes: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio#attributes

**Index**
< p id="top" >Top< /p >
< a href="#top" >Top< /a >

<!-- Comment -->

**Table**

< table >

   < tr >  - Table row

    < th scope="row" >< /th > - Table heading element, scope attribute - "row" - this value makes it clear that the heading is for a row, "col" - this value makes it clear that the heading is for a column
    
   < /tr >
   
   < tr > - Table row
   
       < td >73< /td > - data points
       
   < /tr >
   
< /table >

**Forms Input**

< form action="/example.html" method="POST" >

  < label for="meal" >What do you want to eat?< /label >

  < input type="text" name="food" id="meal" >

< /form >

< input type ="password" > element will replace input text with another character like an asterisk (*) or a dot (•)

**Number input** - < input id="years" name="years" **type="number"** step="1" >

**Slider** - < input id="volume" name="volume" **type="range" min="0" max="100" step="1"** >
Smaller step values will make the slider move more fluidly, whereas larger step values will make the slider move more noticeably

**Checkbox** - < input id="cheese" name="topping" **type="checkbox"** value="cheese" >

**Radio button** - < input type="radio" id="two" name="answer" value="2" > 

**Dropdown list**

  < select id="lunch" name="lunch" >
  
    < option value="pizza">Pizza</option >
    
    < option value="curry">Curry</option >
    
    < option value="salad">Salad</option >
    
  < /select >

  **Datalist Input** - users can type in the input field to search for a particular option. If none of the options match, the user can still use what they typed in

 < input type="text" **list="cities"** id="city" name="city" >

  < datalist id="cities" >
    
    <option value="New York City"></option>
    
    <option value="Tokyo"></option>
    
    <option value="Barcelona"></option>
    
  < /datalist >

**Textarea** - cases where users need to write in more information, like a blog post

< textarea id="blog" name="blog" rows="5" cols="30" > Adding default text < /textarea >

**Submit form**

< form >

< input type="submit" value="Send" >

< /form >

**Form validation** - required fields should be filled in < input id="allergies" name="allergies" type="text" **required** >

**Min and max number of charecters to submit** - < input id="summary" name="summary" type="text" **minlength="5" maxlength="250"** required >

**Matching a Pattern** - check for a valid credit card number (a 14 to 16 digit number). We could use the regex: [0-9]{14,16} which checks that the user provided only numbers and that they entered at least 14 digits and at most 16 digits. limit usernames to only letters and numbers [a-zA-Z0-9]+

  < input id="payment" name="payment" type="text" **required pattern="[0-9]{14,16}"** >
  
  < input type="submit" value="Submit" >

  **CSS**

  p { color: blue; } - p - selector, brackets and inside brackets - declaration block, inside brackets - declaration, color - property, blue - value

  **Linking HTML and CSS together**

  < link href='https://www.codecademy.com/stylesheets/style.css' rel='stylesheet' >
  
  < link href='./style.css' rel='stylesheet' > - stored in the same directory

  CSS classes are meant to be reused over many elements.

  ID is meant to style only one element. IDs override the styles of types and classes.

**Select and style all elements with class="intro"**

  .intro {
  
  background-color: yellow;
  
}

 **Specificity** is the order by which the browser decides which CSS styles will be displayed. A best practice in CSS is to style elements while using the lowest degree of specificity so that if an element needs a new style, it is easy to override. IDs are the most specific selector in CSS, followed by classes, and finally, type. 

  **Chaining** is done by combining multiple selectors. h1.special { } The code above would select only the < h1 > elements with a class of special.

**Background image**

.main-banner {

  background-image: url('https://www.example.com/image.jpg');
  
}

  **Important**

  !important can be applied to override the rules.

  p {
  
  color: blue **!important**;
  
}

**Border** width, style, color, border-radius

p {

  border: 3px solid coral; 
  border-radius: 5px;
}

You can create a border that is a perfect circle by first creating an element with the same width and height, and then setting the radius equal to half the width of the box, which is 50%.

Padding is the space between the contents of a box and the borders of a box.

**Overflow**

p {

  overflow: scroll; 
  
}

The **overflow** property controls what happens to content that spills, or overflows, outside its box. The most commonly used values are:

hidden—when set to this value, any content that overflows will be hidden from view.

scroll—when set to this value, a scrollbar will be added to the element’s box so that the rest of the content can be viewed by scrolling.

visible—when set to this value, the overflow content will be displayed outside of the containing element. Note, this is the default value.

**Resetting Defaults**

"*" {

  margin: 0;
  
  padding: 0;
  
}

The code in the example above resets the default margin and padding values of all HTML elements. It is often the first CSS rule in an external stylesheet.

**Visibility**

Elements can be hidden from view with the visibility property.

hidden — hides an element.

visible — displays an element.

collapse — collapses an element.

The difference between display: none and visibility: hidden? An element with display: none will be completely removed from the web page. An element with visibility: hidden, however, will not be visible on the web page, but the space reserved for it will.

**Box Model**

Content-vox model - defaul

box-sizing: content-box

Bordr box model - In this box model, the height and width of the box will remain fixed.

"*" {

  box-sizing: border-box;
  
}

**Positioning**

The default position of an element can be changed by setting its **position** property.

The position property can take one of five values:

**static** - the default value, **relative** (relative to its statick position - top, bottom, left, right), **absolute** (all other elements on the page will ignore the element and act like it is not present on the page), **fixed** (fix an element to a specific position on the page regardless of user scrolling), **sticky** (keeps an element in the document flow as the user scrolls, but sticks to a specified position as the page is scrolled further)

**Z-index** property controls how far back or how far forward an element should appear on the web page when elements overlap (does not work on static elements).

**Display**

Display property values - **inline** exemple < strong > (inline elements cannot be altered in size with the height or width, share line with other elements), **block** exemple < h1 > (not displayed in the same line as the content around them), and **inline-block** example image (can appear next to each other and we can specify their dimensions using the width and height properties).

**Float** is moving an element as far left or as far right as possible in the container. The float property is commonly used for wrapping text around an image. 

**Clear** property specifies how elements should behave when they bump into each other on the page.

HTML - site structure. CSS - це його наповнення. JavaScript - actions на сайті.
