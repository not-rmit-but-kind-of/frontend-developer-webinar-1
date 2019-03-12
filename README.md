# DEV102 Expert Webinar 01 Intro to HTML & CSS

## Introductions - David and Ben
## House keeping 
  - Please mute your microphone unless talking.
  - Ask questions whenever, via zoom messaging or voice. Will do a Q&A at the end as well and then obviously you can ask questions on slack.
## Disclaimer ;)  
  
## Agenda 
1. Our experiences to date and what we are currently working on
2. Resources we use
    - podcasts
    - web sites
3. Overview of a web page/site
4. Code editor (quick overview)
5. Demo of what we will build during webinar
6. HTML document
7. HTML elements / tags
8. CSS 
9. Browser devtools
10. Finish web page/site building
11. Questions

----

## 1. Our experiences to date and what we are currently working on
- Ben / David
- Coding is part of the job. A lot of what we do day to day is not writing code. Reading code. Requirements. Agile ceremonies. 

## 2. Resources we use
- MDN - https://developer.mozilla.org/en-US/ for guides, references etc for HTML, CSS and JavaScript and much more
- https://css-tricks.com/
- https://syntax.fm
- https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Colors/Color_picker_tool
- icons8.com
- https://color.adobe.com/create/color-wheel/
- http://colormind.io/bootstrap/
- Twitter (@sarah_edo, @addyosmani, @wesbos, @TheLarkInn, @jaffathecake, @keyframers‏, @dan_abramov)

## 3. Overview of a web page/site/app
- HTML, CSS, JavaScript
- HTTP, DOM, Web APIs (Audio, Canvas), Web Components, Web Assembly

## 4. Code editor (quick overview)
  - VS Code (https://code.visualstudio.com/)
  - Provides shortcuts - html, tags autocompletes
  - Formatting
  - Extensions galore
  - Themes

## 5. Demo of what we will build during webinar
  - Travel blog with two pages (travel entries and about me) 
  - Form to submit feedback (not operational - future webinar)
    
## 6. HTML document
  - Create index.html in VS Code (main entry to web site building as part of webinar)
  - DOCTYPE
  - ```<html>```
  - ```<head>```       
    - Not visible on screen.     
    - Every element/tag is lowercase (by convention)
    - Contains title, scripts and style sheet (actual or references) and meta data.
    - See https://developer.mozilla.org/en-US/docs/Web/HTML/Element/head
    - These tags demonstrate important feature - attributes. These are a small subset of what is available.
    - ```<meta name="viewport" content="width=device-width, initial-scale=1">``` - used by mobile devices only. See https://developer.mozilla.org/en-US/docs/Mozilla/Mobile/Viewport_meta_tag
    - See https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta
    - ```<link>``` - used for pulling in external resouces like external style sheets (CSS) files, fonts, images for the web site when launched from a phone/tablet. See https://developer.mozilla.org/en-US/docs/Web/HTML/Element/link
    - In some cases above, you can instruct the browser to prefetch / preload the resouces (i.e. ```<script>```, ```<link>```)
    - Some of these tags can be in the ```<body>```
  - ```<body>``` 
     - Primarily contains the visual content.
     - It is the meaning and structure of a web page.

## 7. HTML elements / tags
  - For a list of all elements see https://developer.mozilla.org/en-US/docs/Web/HTML/Element
  - Semantic / structual elements
  - HTML5 standard introduced a bunch a new semantic elements
  - Example elements:
    - ```<div>``` generic container element (no meaning)
    - ```<span>``` generic container element (no meaning)
    - ```<p>``` paragraph   
    - ```<address>```
    - ```<header>```
    - ```<main>```
    - ```<footer>```
    - ```<h1> <h2> <h3> <h4> <h5> <h6>```
    - ```<img>```
    - ```<input>```
    - ```<label>```
    - ```<form>```
    - ```<table>```
    - ```<a>```
    - ```<ul>```    
    - Some elements are self closing, e.g ```<hr/>```, ```<br/>```, ```<img>```
    - Some elements can contain content and not require an ending tag, e.g. ```<p>hello first line<p>I'm on a new line in the browser``` but it's good practice (and convention) to include.
  - Accessibility considerations

  - Attributes 
    - Example attributes:
      - ```type```
      - ```height``` (img, input)
      - ```border``` (img, border, table)
      - make up your own attributes ```data-*```
      - Accessibility considerations ```alt```       
    - See https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes
     
  - SEO (semantic HTML helps)
  - See https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure
  
  
 ## 8. CSS 
  - Adds the style (appearance) and feel in some case (e.g hover)
  - See https://developer.mozilla.org/en-US/docs/Web/CSS
  - Box model     
    - Each element is represented as a rectangular box, with content, padding, border and margin.     
    - Padding - inner margin (between content and border)
    - Margin - surronds the box (from border outwards). Touches other boxes.
    - Top, left, bottom, right available 
    - Like many CSS properties shorthand properties are available
    - See https://developer.mozilla.org/en-US/docs/Learn/CSS/Introduction_to_CSS/Box_model
    - width, height, min-width, min-height, max-width, max-height (available for content for block / inline-block type elements)
    - background (size, position, image, color)

  - Block vs inline vs inline-block boxes
    - Set via ```display``` property. 
      - ```display: block``` (default for ```<div>``` and many more). 
        - See https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements
        - Boxes are stacked on separate lines. 

      - ```display: inline``` (default for ```<span>``` and more). 
        - See https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements
        - Appear on the same line as other text and other inline elements. 
        - width and height have no effect. 
        - padding, border, margin will affect element's text not the containing block element
      - ```display: inline-block``` 
        - Inherits behaviour from block and inline. 
        - Flows with surrounding text / inline elements, but can be sized with width and height. Maintains its block shape. 
      
    - There are other values for ```display``` but these mostly effect how elements appear inside of the element. See https://developer.mozilla.org/en-US/docs/Web/CSS/display

    - CSS - 3 ways
      - inline
      - internal
      - external 
      - See https://cssreset.com/css-styles-inline-vs-internal-vs-external/
      - global scope
      - These days we have css-modules, css-in-js, which overcome some issues with using traditonal approaches

    - Selectors (internal / external stylesheets)
      - Type
      - Class
      - ID selector
      - Attribute selector  
      - Cominators (e.g. nth child of type, sibling)
      - Pseudo classes, Pseudo elements
      - Rules govern which get applied (specificty) 
      - See https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors
      - See https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity
      - !important (not recommended)

    - http://learnlayout.com/ (really nice short snippets of key aspects)

  - Styling text

  - Styling boxes
    - Maintain aspect ratio and automatically scale background image with padding bottom as a percentage using formula - Height / (Width / 100)


## 9. Browser devtools

## 10. Finish web page/site building

## 11. Questions