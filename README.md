# tmftc-html-css
Teaching my friends to code: HTML &amp; CSS


## What are we learning?
The basics of [Hypertext Markup Language (HTML)](https://en.wikipedia.org/wiki/HTML) and [Cascading Style Sheets (CSS)](https://en.wikipedia.org/wiki/Cascading_Style_Sheets), the two languages used to describe the look and content of web pages.

These languages, along with another: Javascript, are the core technologies for front-end web development. 


## What tools do we need?
The online front-end code editor [Codepen](https://codepen.io/pen/). This tool allows us to immediately see the effects of editing our code.

Codepen also automatically adds some of the extra boilerplate needed for every HTML document, so we can focus on just the interesting bits.


## Why two (or three!) different languages?
We'll worry about Javascript later. Between the other two, HTML describes the content and meaning of the content, while CSS focuses on styling and visual effects.

Using a different CSS style to the same HTML document can result in a very different display. You might imagine that we can use this to give users an option between viewing our site in "light" or "dark" mode, for example.


## Let's Get Started

### HTML
HTML is an angle-bracket denoted markup language. This means that each element in an HTML document is a pair of tags, one "opening" `<tag>`, and one "closing" `</tag>`, sometimes with content and other HTML elements between them, like this:

    <p>This is a paragraph of text. <span>Hi mom!</span></p>
    
Using elements like this, we can give meaning to each section of the document. There are lots of different elements: links (called anchors), images, tables, forms, and so on. All the basic parts that you need to describe the structure of an HTML document.

Some elements that would never have content between the opening and closing tags use an abbreviated form called "self-closing", these elements are written as just a single tag (instead of a pair):

    <hr />
    
#### Element Attributes
Each element can have additional attributes assigned to it. These attributes are written inside the angle-brackets of a tag, after the name of the element, and separated by spaces.

Each attribute consists of a name, an equal sign, and then the (usually) quoted value of the attribute. Like the "href" attribute we see here:

    <a href="https://www.google.com">Link To Google</a>
    
##### CSS Attributes
There are a couple of special attributes that we can assign to an element that will let us apply styling to it with CSS.

We can use the `id` attribute to give the element a specific name that we can reference in CSS, but this name must be unique and should only be assigned to a single element.

    <p id="my-special-paragraph">This is a special paragraph</p>

We can also use the `class` attribute to assign the element to one or more classes. These classes can be referenced in CSS to apply specific styling to those elements.

    <p class="important-text">Some important text that needs special display</p>
    <p class="important-text">Also an important message!</p>

#### HTML Elements
- `p`: paragraph, a block of text, usually with some space around it
- `span`: a span of text, usually to apply some style
- `div`: a division, a block of content that will be styled together
- `a`: a link to some other resource (`a` is for "anchor")
- `hr`: horizontal rule, it's a horizontal line
- `ul`: unordered list
- `ol`: ordered list
- `li`: list item, this element is usually nested inside a `ul` or `ol` element
- `h1`: heading 1, topmost with the largest text
- `h2`: heading 2, usually smaller than heading 1
- `h3`: heading 3, usually smaller than heading 2
- `h4`: heading 4, usually smaller than heading 3
- `h5`: heading 5, usually smaller than heading 4
- `h6`: heading 6, usually smaller than heading 5

Here's a longer example that shows some of the elements used together in a document:

    <h1>Teaching My Friends To Code</h1>
    <p>We're learning HTML and CSS!</p>
    <hr />
    <h2>HTML</h2>
    <p>Some text about HTML</p>
    <hr />
    <h2>CSS</h2>
    <p>Some text about CSS</p>
    <hr />
    <h2>Links to Helpful Resources</h2>
    <ul>
        <li><a href="https://www.google.com">Google</a></li>
        <li><a href="https://www.wikipedia.org">Wikipedia</a></li>
        <li><a href="https://www.stackoverflow.com">Stack Overflow</a></li>
    </ul> 

### CSS
CSS is a language used to describe the presentation of an HTML document.

In CSS, you define "rulesets" by using the names of the elements that you want to style, called the "selector", followed by curly braces `{}` containing a set of property names and values that you want on the selected elements:

    p {
        background: blue;
        color: red;
    }

Here we're saying that all `p` (paragraph) elements in a document should have red text on a blue background.

#### Styling multiple elements
When defining a ruleset, you can apply the same styling to several element types at once by separating them by commas before the curly braces:

    p, h1 {
        background: blue;
        color: red;
    }
    
This sets the same style on the `p` and `h1` elements in the document.
    
#### Element selector types
In addition to using the element names for the selector, we can also select elements by id, class, and attributes.

##### By ID
To select elements by the value of their `id` attribute, prefix the name used in the id attribute with the pound sign `#`:

    #my-special-paragraph {
        font-size: 100px;
        color: yellow;
        background: black;
    }

##### By class
To select elements by their `class` attribute, prefix the name in the class attribute with a period `.`:

    #important-text {
        font-size: 30px;
        color: white;
        background: red;
    }

##### By attribute
To select elements that contain an certain attribute, add the attribute name in brackets after the element type:

    #img[src] {
        border: 1px solid red;
    }
    
#### CSS Properties
CSS properties cover a broad range of styling areas. We're just going to focus on a couple at first: font/text styling and layout.

##### 

### Further Reading
- [Mozilla: HTML Basics](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics)
- [Mozilla: CSS Basics](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics)
- [Mozilla: CSS Selectors](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors)
