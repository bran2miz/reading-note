# HTML and CSS

**HTML- Hyper Text Markup Language**

### Introduction

- HTML and CSS allows web developers the tools to make a page *interesting* and **Engaging**.
- An html document contain tags (ie <tags></      tags>) that are used to implement *unique* features on the web page. 
- **CSS** allows the the web developer the ability to style and design the page, affecting the look and presentation of a site. 

### Chapter 1

**What are elements?**

    - Elements are essentially specific words within angled brackets (ie <angled></angled>) known as tags.
    - HTML elements have both an opening (<opening>) and closing (/opening) tag.
*note* - it is very important to have a closing tag otherwise the code will be jumbled.

**Attributes**

- In between the opening and closing tag contains the information. 

- Within the opening tag contains *attributes*
    - included in the opening tag is the *name* of the attribute and its *value*
        - the attribute *name* is extra information that is used to further enhance the content of the element. 

**!DOCTYPE HTML**

- important to start with this declaration
- tells the browser that the user wants to create an HTML document.


#### Broad Types of Tags 

**< body >** tag- everything within the body is displayed on the browser

**< head >** tag- the header tag is not show on the main browser.
    - can add the title of your page within the header using the < title> </ title> tag.
    - The header tag is used for search engines to locate your page. 

**<! -- -->** - not a tag, however this can be used to add a comment that doesn't affect the code. 

#### Id and Class

*What is an id?*
- an **id** is used to specifically "identify" an element.
    *note* - it is very important in CSS for enhancing specific elements. 
- an id is considered a "global attribute" because it can be placed within any type of element.

*What is a class attribute?*

- Different from an id attribute, a class attribute is used to identify multiple elements. 
    - Differs from an id attribute in that it can also be implement within elements, but an id can only identify one type of element. 

#### Block and Inline elements 

*Block* elements are used to essentially separate parts or areas of a webpage.
    - Such *block* elements include: 
        1. < h1></ h1> - header tag
        2. < p>< /p> - paragraph tag
        3. < ul>< /ul> - unordered list tag
        4. < li>< /li> - list tag

*Inline* elements - elements that can make changes within elements without breaking the code syntax.
    - Such *inline* elements include:
        1. < a>< /a> tag- can be used for linking to another page.
        2. <b> < /b> tag
        3. < em> < /em> tag
        4. < img> < /img>

#### Block and Inline Tags

**< div>** tag- groups elements in one block
**< span>** tag- inline version of the *div* element
    - The span tag controls specific parts within an element using CSS.
- **< iframe>** tag- includes features to alter an image. 
    - Within the iframe element includes attributes such as:
        1. src- the URL aspect of the element
        2. height- height of the iframe in pixels
        3. width- the width of the iframe in pixels
        4. scrolling- adds scrollbars within the iframe
    - Frameborder- gives a border to the iframe.
    - Seamless- used when one doesn't want to implement a scrollbar.

**< meta>** tag- contains information about the web page. 
    - the content within the meta tag is not visible on the browser, however it provides details about the page. 
    - useful in that it provides keywords for the search engine.
    - can provide information about time sensitivity
    - provide the creator's name. 

### Chapter 7

#### HTML 5

*What is HTML 5?*

**HTML 5**- provides brand new elements for the user, allowing simplified code to further promote the creation of unique web pages.
    - Easier to "describe the structure of the page". (**book reference**) 
    - ie < div> is no longer required

##### HTML 5 New Tags

**< header> < footer>** tag- header or footer that can appear either at either vertical ends of the webpage.
    - can further provide structure and organziation to the page. 

**< nav>** tag- navigation tag; essentially a guide and organizational tool to properly naviage a webpage. 
    - usually will contain different important main topics that are to be featured within the webpage. 

**< article>** tag- stand alone section of a webpage. 
    - An article tag is similar to the following:
        1. Blog Post
        2. Article
        3. Comment Section
    - can create individual *< article>* elements for each article block. 

**< aside>** tag- contained within an article element. 
    *note* - Think of it as a sort of glossary. 
    - It is a part of the article, but ot quite a part of the overall comprehension of the article. 

**< section>** tag- similar to the *class* attribute in that it connects similar parts of the page together. 

**< hgroup>** tag- groups similar conent within the header together. 
    - essentially creates a header under one "umbrella".

**< figure> < figcaption>** tags - These tags are used as a way to connect to the article.
    - only used to reference the article. 

#### What Helps Older Browser Understand HTML 5

Older Browsers that cannot compute HTML 5 styled elements need to include which sections are desired to be *block* elements and not *inline* elements. 
    - *note*- in order for HTML 5 to work in older browsers, such as older version of Internet Explorer, the HTML document also needs to include speficif JavaScript, which can be found and copied from Google.

### Chapter 18

#### Steps to Create A Website

- **Identify who the target audience is**
    Factors can include:
        1. Age
        2. Origin
        3. Income
        4. Housing
        5. Occupation

- What **purpose** is the target audience "clicking" on or arriving onto the page. 

- What sort of information is necessary to include on the page.

- Frequency of the target audience (or the amount of visitation per person).

##### Important Tools to Create A Webpage

**Site Map**
    - create a site map to display the overall flow of the webpage.
        - Begin with a flow chart starting with the hompage, with "branches" that flow to different parts and other pages of the web site. 
        - A site map can inlcude links to different parts of the site. 

**Wireframes** - low fidelity sketch of a digital interface. Wireframes help navigate the product of the webpage. 
    - 2 types of wireframe:
        1. **handrawn sketch**
        2. **digital sketch**
    *note* - a pro tipe is to look at example wireframes as a source of inspiration.

**Visual Hierachy** - what aspects of the webpage will visually attract people to the website. 
    - i.e. Group together blocks of content to make the page easier to navigate
        Remember: **A MORE SIMPLE PAGE THE BETTER**

# JavaScript

*What is the definition of script in coding terms?*

A *script* is:
    - instructions for a computer to process in order to attain the desired *objective*.
    - think of a script as a:
        1. Recipe Book
        2. Manual

**Writing Script in the primitive terms**
    - What is the *objective*?
    - Design the script within *task* or the process of steps
    - Writing in a language the computer understands. 

### Object, Event, and Methods

**Object** - tangible thing in the world and can have different *types*.

**Properties**- features of the obejct that contain both a *name* and a *value*.

**Events** - when the user interacts with the computer.
    - In basic terms: a situation occurs and an *event* alerts the user. 

**Methods** - properties of the obejct can be obtained or altered through methods. 

[<== Back](README.md)