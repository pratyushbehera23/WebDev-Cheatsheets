# HTML

<!-- Notes
    HTML CHEATSHEET
        Basic HTML Tags
        Text Formatting & Quotations
        Objects & iframes
        HTML Forms, Semantic tags, Tables, Lists & Images 

    HTML consists of:
        Elements
        Attributes
        Style & Text formatting
        Links & Images
        Lists
        Tables
        Forms
        Buttons

    HTML5; old vs new html5
    new elements in html5; old elements not to use now
    new attributes of form
    graphics elements <svg> <canvas>
    multimedia elements <audio> <video>
    Semantics elements:
        A semantic element clearly describes its meaning to both browser and the developer.
        Semantic elements : <header>, <nav>, <section>, <article>, <aside>, <form>, <footer>, 
        Non-semantic elements : <div>, <span>, 

>   BASIC HTML TAGS
        <!DOCTYPE>
            Defines the document type
            - commonly written as <! DOCTYPE html>
        <html> ... </html>
            Defines an html document
            - commonly written as <! DOCTYPE html>
            - tells the browser this is an html doc
            - root element, container for all other elements
        <head> ... </head> 
            Defines information about the doc
            - container for all the head elements
            - can contain the following tags: <meta>, <title>, <link>, <style>, <script>
        <title> ... </title>
            Defines a title for the document
            - very important for SEO
            - defines a title in the browser toolbar
            - Go for a longer, descriptive title, 50-60 chars
            - Do not use just words or a list of words
        <body> ... </body>
            Defines the document's body
            - contains all the contents of an HTML doc
            - often used in adding bg color to doc 
        <h1> ... </h1> to <h6> ... </h6>
            Defines HTML headings
            - <h1> defines the most importnt, largest heading
            - use it for main heading on a page
            - <h6> defines the least important heading
            - use headings to appropriately section ur page
        <p> ... </p>
            Defines a paragraph
            - browser automatically adds margins
            - tells the browser this is an html doc
            - use it for paragrahs, helpful in SEO
        <br>
            Inserts a single line break
            - useful for writing addresses or poems
            - don't use it for seperating paragraphs
            - it's an empty tag meaning it has no end tag
        <a> ... </a>
            Defines a hyperlink
            - used to link from one page to another
            - common attributes:
                href - Specifies URL of the page the link goes to
                    values: url/link 
                target - Specifies where to open the linked doc 
                    values: _blank, _self, _parent, _top
                rel - Specifies the relationship between the current document and the linked document 
                    values: alternate, noreferrer, noopener, dofollow
                download - Specifies that the target will be downloaded when a user clicks on the hyperlink 
                    value: file name
        <hr>
            Def a thematic change in the content
            - most often displayed as a horizontal rule that is used to separate content
            - an empty element
        <link>
            Defines rel btn a doc & an external resource
            - mostly used to link to a css file
            - an empty element
            - only goes in the header, can be used multiple
        <meta>
            Defines metadata about an HTML doc
            - always goes in the head element
            - very important for SEO
            - common attributes:
                name - Specifies a name for the metadata 
                    values: description, viewport, author, keywords
                content - Gives the value associated with the http-equiv or name attribute 
                    value: text
                charset - Specifies the character encoding for the HTML document 
                    value: UTF-8 mostly
        < !-- ... -- >
            Comment
            - Comments are not displayed in the browsers
            - use comments to explain your code
            - very helpful in code maintainance

>   HTML TEXT FORMATTING & QUOTATION
        <b> ... </b>
            Defines bold text
            -without any extra importance
        <strong> ... </strong>
            Defines a strong(bold) text
            - denotes an important text, appears bold
        <i> ... </i>
            Defines an italicized tex
            -without any extra importance
        <em> ... </em>
            Defines an emphasized text
            - denotes an important text, appears italicized
        <mark> ... </mark>
            Defines markded/highlighted text
            - text will be highlighted
        <small> ... </small>
            Defines a small text
            -text appears smaller than sorrounding text
        <del> ... </del>
            Defines a deleted text
            - text will be highlighted
        <ins> ... </ins>
            Defines inserted/added text
            - text appears underlined 
        <sub> ... </sub>
            Defines a subscripted text
            - text appears subscripted to the text before it
        <sup> ... </sup>
            Defines a superscripted text
            - text appears superscripted to the text before it 
        <q> ... </q>
            Defines a quote
            - browsers normally. put a quote around this text 
        <address> ... </address>
            Defines contact information
            - text appears italicized
        <blockquote> ... </blockquote>
            Defines a section quoted from a source
            - text appears indented
            - attribute: 
                cite - link to the source of the quote
        <abbr> ... </abbr>
            Defines an abbreviation or acronym
            - text appears italicized
            - attribute:
                title - the full version of the abbreviation
        <cite> ... </cite>
            Defines the title of a work
            - appears italicized
        <bdo> ... </bdo>
            Defines Bi-Directional Override
            - Reverses text order to right-to-left or vice-versa
            - attribute
                dir - the direction to change to values: rtl, ltr
        <code> ... </code>
            Defines a code snippet
        
        APPROPRIATE USE
            - Search engines use these tags to understand web page content, so use them appropriately.
            - Eg. Do not use <em> just to italicize text when it has no importance attached.
            - If these tags are used appropriately, they help optimize your web page for search engines and also give users a smooth experience.

>   HTML FORMS 
        <form> ... </form>
            Defines an html form for user input
            Form <form> - Attributes
                action
                    Defines what happens when form submitted
                    - Values: url - mostly of page with server side code
                method
                    Specifies HTTP Method for submitting the form
                    - Values: get, post
                enctype
                    Specifies the encoding scheme, only for POST
                    - Values: url - mostly of page with server side code
                autocomplete
                    Specifies if browser shld autocmplete the form
                    - Values: on, off. default = on
                novalidate
                    Specifies that the browser should not validate the form.
                target
                    Specifies targt of the address in the action attr
                    - Values: _self, _blank, _parent, _top. default = _self

        <input>
            Defines an input control
            Input <input> Attributes:
                type
                    Specifies the type on input
                    - Values: text, email, password, button, radio, submit, date, checkbox, file, number, search, url, tel, image,... 
                name
                    Specifies the name of the input
                    - used to identify the input in server-side code
                value
                    Specifies an initial value for an input field
                    - Value: select in JS to obtain the user's input
                autofocus
                    Specifies if input field shld hve focus on load
                    - Value: true in nature
                readonly
                    Specifies that an input field is read-only
                    - Value: not declared, true in nature
                disabled
                    Specifies that an input field should be disabled
                    -value: true in nature (disables the input field)
                size
                    Specifies the visible width, of an input field.
                    - Value: number (of charactiers)
                maxlength
                    Spec max no of X'ters allowed in an input field
                    - Value: number (of charactiers)
                min & max
                    Specifies the min & max values 4 an input field
                    - Value: number 
                multiple
                    Allows user to enter more than one value
                    - Value: true, works with only email & file inputs
                placeholder
                    specifies a short hint about the expected Salue
                    - Value: usually an example
                required
                    Specifies that an input field must be filled
                    - Value: true in nature
                height & width
                    Specifies height and width of input type image
                    - Value: number
                autocomplete
                    Specifies if input field shold have autocomplete
                    - Value: true in nature
                pattern
                    Specifies regex to check input against on submit
                    - Value: regular expression
                step
                    Specifies the legal no intervls for an input field
                    - Value: number

        <textarea> ... </textarea>
            Defines a multiple control input
            Textarea <textarea> Attributes:
                rows
                    Specifies the visible height of a text area
                    - Value: number
                cols
                    Specifies the visible width of a text area
                    - Value: number
                placeholder
                    Specifies a short hint about the expected Salue
                    - Value: usually an example
                required
                    Specifies that an input field must be filled
                    - Value: true in nature

        <label> ... </label>
            Defines a label for an <input> element

        <select> ... </select>
            Defines a dropdown list
            Select <select> Attributes:
                name
                    Specifies the name of the dopdown list
                    - Value: string
                size
                    Secifies the number of visible values
                -   Value: number
                multiple
                    Allows the user to select more than one value
                    - Value: not declared, true in nature
                required
                    Specifies if choosing an option is required
                    - Value: not declared, true in nature
                autofocus
                    Specifies if the drop-down auto comes in focus
                    - Value: not declared, true in nature
                size
                    Secifies the number of visible values
                    -Value: number

        <option> ... </option>
            Defines options for the <select> dropdown list
            Option <option> Attributes:
                pattern
                    Specifies regex to check input against on submit
                    - Value: regular expression
                step
                    Specifies the legal no intervls for an input field
                    - Value: number
        
        <fieldset> ... </fieldset>
            Defines a group of related elements in a form
        <legend> ... </legend>
            Defines a caption for the <fieldset> element
        <optgroup> ... </optgroup>
            Defines group of related options in a drop-down
        <datalist> ... </datalist>
            Specifies list of pre-defined opts 4 input contrls
        <button> ... </butt on>
            Defines a clickable button
        <output> ... </output>
            Defines the result of a calculation
        

>   HTML OBJECTS & IFRAMES

        <object> ... </object> - Attributes
        Defines a container for an external resource. It can be a web page, picture, media player, plug in.
            data
                Spec URL of the resurce to b used by the object
                - Values: URL
            name
                Specifies a name for the object
                - value; name
            height & width
                Specifies the height & width of the object
                - Value: pixels
            type
                Speci data type of media in the data attribute
                -media type eg. image/png

        <object> ... </object> - Attributes
        Defines a container for an external resource. It can be a web page, picture, media player, plug in.
            height
                Specifies the height of the embedded content
                - Value: pixel
            width
                Specifies the width of the embedded content
                - Value: pixel
            src
                Specifies address of the external file to embed
                - Value: URL
            type
                Specifies media type of the embedded content
                - Value: media_type. eg video/mp4

        <iframe> ... </iframe> - Attributes
        Used to embed another document within the current HTML document
            name
                Specifies the name of an <iframe>
                - Value: text
            src
                Specifies the address of the doc't to embed
                -value: URL
            height & width
                Specifies the height & width of the object
                - Value: pixels
            srcdoc
                Spec the HTML content of the page to show
                - Value: HTML Code
            allow
                Specifies a feature policy for the <iframe>
                - Value: true in nature
            allowFullScreen
                Set to true if the <iframe> can activate fullscreen
                - Value: true. false

        
        HTML CHARACTER OBJECT CODES
        Special characters. Can be declared using entity name or entitiy numbers. some below
            Copyright Sign 
                entity - &copy; number - &#169;
            Registered Sign 
                entity - &reg; number - &#174;
            Ampersand 
                entity - &amp; number - &#38; 
            Euro
                entity - &euro; number - &#8364;
            Emoji - 😀 
                number - &#128512; 
            Emoji - 😂
                number - &#128514;
            Sum of Math Symbol 
                entity - &sum; number - &#8721; 
            Trademark sign
                entity - &trade; number - &#8482;

        
>   HTML SEMANTICS | IMAGES | TABLES | LISTS | 

    HTML5 SEMANTIC TAGS / NEW TAGS
        <article> ... </article> 
            - Defines an article 
        <aside> ... </aside> 
            - Defines content aside from the page content
        <details> ... </details> 
            - Defines additional details user can view / hide 
        <figcaption> ... </figcaption>
            - Defines a caption for a <figure> element
        <figure> ... </figure> 
            - Specifies self-contained content, like illustrations, diagrams, photos,code listings, etc.
        <header> ... </header>
            - Specifies a header for a document or section
        <footer> ... </footer> 
            - Defines a footer for a document or section 
        <main> ... </main>
            - Specifies the main content of a document
        <mark> ... </mark> 
            - Defines marked/highlighted text 
        <nav> ... </nav>
            - Defines navigation links
        <section> ... </section> 
            - Defines a section in a document 
        <summary> ... </summary>
            - Specifies the main content of a document
        <time> ... </time> 
            - Defines a date/time 
        <menuitem> ... </menuitem>
            - Defines an item in a list or menu

    IMAGES <img> - ATTRIBUTES
        src
            - Defines the URL of the image
            - Value: URL
        alt
            - Defines an alternate text for an image
            -value: text. should not include the word "image"
        height
            - Specifies the height of the image
            - Value: pixels
        width
            - Specifies the width of the image
            - Value: pixels

    TABLE TAGS
        <table> ... </table>
            - Defines a table
        <th> ... </th>
            - Defines a header cell in a table
        <td> ... </td>
            - Defines a cell in a table
        <tr> ... </tr>
            - Defines a row in a table
        <thead> <tbody> <tfoot> ... </..>
            - Defines the table header, body & foot
        <caption> ... </caption>
            - Defines a table caption

    LIST TAGS
        <ol> ... </ol> 
            - Defines a list with an order, numbered
        <ul> ... </ul>    
            - Defines a list without order, bulleted
        <li> ... </li> 
            - Defines an individual item in a list 
        <dl> ... </dl>   
            - Defines list item with definition 
        
-->
<!-- Html elements:

    Block Elements :
    <address> <article> <aside> <blockquote> <canvas> <dd> <div> <dl> <dt> <fieldset> <figcaption> <figure> <footer> <form> <h1> <h6> <header> <hr> <li> <main> <nav> <noscript> <ol> <p> <pre> <section> <table> <tfoot> <ul> <video>
    
    Inline Elements : 
    <a> <abbr> <acronym> <b> <bdo> <big> <br> <button> <cite> <code> <dfn> <em> <i> <img> <input> <kbd> <label> <map> <object> <output> <q> <samp> <script> <select> <small> <span> <strong> <sub> <sup> <textarea> <time> <tt> <var>
-->
<!-- HTML Semantics Tags: 

    --------------------------------------------------------------------------  
    |                                                                        | 
    |                               <header>                                 | 
    |                                                                        | 
    -------------------------------------------------------------------------- 
    |                                                |                       | 
    |                                                |                       | 
    |                                                |                       | 
    |                  <section>                     |                       | 
    |                                                |                       | 
    |                                                |                       | 
    |------------------------------------------------|       <aside>         | 
    |                                                |                       | 
    |                                                |                       | 
    |                  <article>                     |                       | 
    |                                                |                       | 
    |                                                |                       | 
    -------------------------------------------------------------------------- 
    |                                                                        | 
    |                               <footer>                                 | 
    |                                                                        | 
    -------------------------------------------------------------------------- 

    Semantics tags are used in HTML5, and are good for SEO 
    more semantics tags : <details> <form> <figure> <figcaption> <summary> <table> etc.

    <nav>
        The <nav> HTML element represents a section of a page whose purpose is to provide navigation links, either within the current document or to other documents. Common examples of navigation sections are menus, tables of contents, and indexes.
        
    <main>
        The <main> element is used to denote the content of a webpage that relates to the central topic of that page or application. It should include content that is unique to that page and should not include content that is duplicated across multiple webpages, such as headers, footers, and primary navigation elements.
        The <main> HTML element represents the dominant content of the <body> of a document. The main content area consists of content that is directly related to or expands upon the central topic of a document, or the central functionality of an application.
        An HTML document can have more than one <main> element, but only one can be visible. If more than one <main> element is present in a document, all other instances must be hidden using the hidden attribute.
        
    <section>
        Section tag defines the section of documents such as chapters, headers, footers or any other sections. The section tag divides the content into section and subsections. The section tag is used when requirements of two headers or footers or any other section of documents needed.
        
    <aside>
        The <aside> HTML element represents a portion of a document whose content is only indirectly related to the document's main content. Asides are frequently presented as sidebars or call-out boxes.

    Should I use section or article? The section tag defines sections in a document, such as chapters, headers, footers, or any other sections of the document. ... The article tag specifies independent, self-contained content. An article should make sense on its own and it should be possible to distribute it independently from the rest of the site. 
    Anything which can have an author should be using an <article> element. Using sections should be reserved for separating sections of your website, such as an introduction (to what your site might be about), some news articles, or an area within an article used for comments.
    The <article> element represents a self-contained composition in a document, page, application, or site, which is intended to be independently distributable or reusable (e.g., in syndication). Examples include: a forum post, a magazine or newspaper article, or a blog entry, a product card, a user-submitted comment, an interactive widget or gadget, or any other independent item of content.
    A given document can have multiple articles in it; for example, on a blog that shows the text of each article one after another as the reader scrolls, each post would be contained in an <article> element, possibly with one or more <section>s within.

-->

<!-- index.html -->

```html

<!DOCTYPE html>
<html lang="en" oncontextmenu="return false">
<!-- ^ as above the whole page can't be right clicked -->

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="This content is shown by google in the list of site while searched. It's important to show people what's in your site to attaract and get them clicked. #imp_seo_tip">    <!--Description of page to show in google search page-->
    <meta name="author" content="Pratyush"> <!--Author to recognize-->
    <meta name="keywords" content="Coding Python Web-development Javascript Developer"> <!--All keywords related to content of the page-->

    <title>MySite</title>
    <!-- <link rel="shortcut icon" href="favicon.ico" type="image/x-icon"> -->
    <!-- <link rel="icon" type="image/x-icon" href="/images/favicon.ico"> -->
    <link rel="shortcut icon" href="media/iconpg.png" type="image/x-icon">
    <!-- Animated GIF will work only in Firefox (i guess) -->
    <!-- <link rel="icon" href="http://example.com/favicon.gif" type="image/gif" /> -->

    <link rel="stylesheet" href="style.css">

    <style>
        /* *{
            margin: 0;
            padding: 0;
        } */
        #spidey{
            height: 200px;
            width: 350px;
        }

        /* Text-selection-color */
        ::-moz-selection { /* for Firefox */
        color: yellow;
        background: green;
        }
        ::selection {
        color: yellow;
        background: green;
        }

        /* Scroll-bar */
        ::-webkit-scrollbar {
            width: 10px;
        }
        ::-webkit-scrollbar-track {
            box-shadow: inset 0 0 5px #333;
            border-radius: 5px !important;
            margin: 5px;
        }
        ::-webkit-scrollbar-thumb {
            background: rgba(9, 0, 128, 0.5) !important;
            border-radius: 5px !important;
        }
        ::-webkit-slider-thumb:hover {
            background: #000 !important;
        }
    </style>
    <script></script>
</head>

<body onload="alert('Nice to Meet You!')">

    <header>
        <nav></nav>
    </header>

    <!-- Basics -->
    <div class="basics">

        <!-- Headings -->
        <h1>Hello</h1>
        <h2>World</h2>
        <h3>World</h3>
        <h4>World</h4>
        <h5>World</h5>
        <h6>World</h6>

        <p>This is a paragraph...Lorem ipsum dolor sit amet consectetur adipisicing elit. Itaque, illo?</p>
        <!-- HTML entities & -->
        <p>These are some popular entities: &lt; &gt; &amp; &copy; &reg; &trade;</p>
        <!-- emojis using HTML -->
        <p>&#128514; &#128515; &#128516; &#128520; &#128521; &#128522; &#128523; &#128524; &#128525; (&#128526; 😎) &#128578; &#129297; &#129313; &#129324; &#129349; &#129351; &#129396; </p>

        <br>
        <hr>

        <!-- Formatting -->
        <abbr title="">Defines an abbreviation or an acronym</abbr>
        <b>Defines bold text</b>
        <blockquote>Defines a section that is quoted from another source</blockquote>
        <code>Defines a piece of computer code</code>
        <em>Defines emphasized text</em>
        <mark>Defines marked/highlighted text</mark>
        <pre>Defines preformatted text</pre>
        <progress>Represent the progress of a task</progress>
        <q>Defines a short quotation</q>
        <small>Defines smaller text</small>
        <p>My favorite color is <del>blue</del> red.</p>
        <p>My favorite color is <del>blue</del> <ins>red</ins>.</p>

        <!-- Text Formatting -->
        <b>Hey, it's bold.</b>
        <strong>I'm strong important.</strong>
        <i>Oh, then italic here.</i>
        <em>Emphasized text</em>
        <u>Yep underlined.</u>
        <big>Yo big bro.</big>  <!--The tags in red are removed from HTML5; like <big> <center> etc. | use their alternatives or CSS to do so.-->
        <small>I'm small one.</small>

        <br>
        <!-- subscript & superscript -->
        <p>H<sub>2</sub>O, CO<sub>2</sub></p>
        <p>base<sup>power</sup>; A<sup>2</sup>=a<sup>3</sup></p>

        <p>HTML Quotation and Citation Elements:</p>
        <p>Here is a quote from WWF's website:</p>
        <blockquote cite="http://www.worldwildlife.org/who/index.html">For 50 years, WWF has been protecting the future of nature. The world's leading conservation organization, WWF works in 100 countries and is supported by 1.2 million members in the United States and close to 5 million globally.</blockquote>
        <p>WWF's goal is to: <q>Build a future where people live in harmony with nature.</q></p>
        <p>The <abbr title="World Health Organization">WHO</abbr> was founded in 1948.</p>
        <address>
            Written by John Doe.<br>
            Visit us at:<br>
            Example.com<br>
            Box 564, Disneyland<br>
            USA
        </address>
        <p><cite>The Scream</cite> by Edvard Munch. Painted in 1893.</p>
        <bdo dir="rtl">This text will be written from right to left</bdo>

        
        <!-- The <abbr> element represents an abbreviation or acronym; the optional title attribute can provide an expansion or description for the abbreviation. If present, title must contain this full description and nothing else. -->
        <p>You can use <abbr title="Cascading Style Sheets">CSS</abbr> to style your <abbr title="HyperText Markup Language">HTML</abbr>. <br> Hover over those dotted for info done by &lt; abbr &gt; tag.</p>
        <!-- You can use <abbr> in tandem with <dfn> to more formally define an abbreviation -->
        <p>A <dfn id="spec">Specification</dfn>(<abbr title="Specification">spec</abbr>) is important.</p>
        <!-- The <wbr> (Word Break Opportunity) tag specifies where in a text it would be ok to add a line-break. Tip: When a word is too long, the browser might break it at the wrong place. You can use the <wbr> element to add word break opportunities. -->
        <p>To learn AJAX, you must be familiar with the XML<wbr>Http<wbr>Request Object.</p>

        <!-- pre tag : writes everything inside as it is; including spaces newLines.. -->
        <!-- pre tag represents pre-formatted text -->
        <pre>
            hey,        there
                one two, three

    Okey, my name is      Pratyush.
            pre tag represents a block of preformatted text on webpage ;)
                you can show any text     as it is here
        </pre>

        <!-- code tag is used to represent source codes -->
        <code>
            # hello world <br>
            var1 = 5 <br>
            var2 = 6 <br>
            add = var1 + var2 <br>
            print("Addition:",var1,'+',var2,'=',add) <br>
            o/p: Addition: 5 + 6 = 11 <br>
        </code>

        <!-- Images -->
        <img src="" alt="">
        <map name=""></map>
        <area shape="" coords="" href="" alt="">
        <canvas></canvas>
        <figcaption></figcaption>
        <figure></figure>
        <picture></picture>
        <svg></svg>

        <img src="media/hero.jpg">
        <img src="heySpidey.jpg" alt="Image of Spider-man into the spidey-verse">
        <!-- alt helps the visually impared to hear about the image as can't be seen & also if any error occurs to show the image it displays the text about it -->

        <a href="https://youtube.com">YouTube</a>
        <a href="https://youtube.com" target="_main">YouTube(inNewTab)</a>
        <a href="/contact">Contact us</a>
        <a href="/contact" target="_blank">ContactUs(inNewTab)</a>
        <!-- any content: text, img, heading,... can be put inside an anchor tag for use as a link-->
        <br>
        <!-- HTML Link -->
        <!-- Image as a link -->
        <a href="goto.html"><img src="media/iconpg.png" alt="imagelink"></a>
        <!-- Link to an Email address -->
        <a href="mailto:ipratyush02@gmail.com">Send email</a>
        <!-- Button as a link -->
        <a href="https://www.google.com"><button>Google page</button></a>
        <!-- Link to PhoneNo or Fax -->
        <a href="tel:+919692002521">Call us</a>
        <a href="fax:+919692002521">Send fax</a>
        <!-- Link 'Title' attribute -->
        <a href="https://www.google.com" title="Google home page">google.com</a>
        <!-- Link for downloading content from Internet -->
        <a href="https://www.yoursite.com/notes.pdf" download target="_blank" title="Click To Download">Download PDF</a>
        <!-- Link JS -->
        <a href="JavaScript:self.close();" id="close">CLOSE</a>

        <hr>

        <div id="oneliners">
            <!-- Tooltip: extra information -->
            <p title="like"></p>
            <!-- Download: download the link(href) instead of opening it -->
            <!-- <a href="resume.png" download=""></a> -->
            <a href="resume.png" download></a>
            <!-- Text-direction -->
            <p dir="auto">This text is following auto; as per the language</p>
            <p dir="ltr">This text is following left to right</p>
            <p dir="rtl">This text is following right to left</p>
            <!-- Content-Editable -->
            <p contenteditable="true"> This paragraph is editable just click and edit..</p>
            <!-- Basic-Accordion -->
            <details>
                <summary>About lorem ipsum</summary>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquid inventore ipsa iusto expedita nemo voluptas dolor modi id incidunt! Perspiciatis molestias dolores esse, suscipit quasi nesciunt impedit enim architecto perferendis!</p>
            </details>
        </div>

        
        <!-- Marquee : moving text -->
        <marquee direction="right" behaviour="alternate"> Hello World </marquee>

        <!-- LISTS -->
        
        <!-- Unordered list -->
        <!-- type : circle, disc, square -->
        <ul type="square">   <!-- type attribute for ul - don't use - use CSS list-style-type property instead -->
            <li>Home</li>   <!-- li : list items -->
            <li>About</li>
            <li>Contact</li>
        </ul>
        <ul type="circle">
            <li>Home</li>
            <li>About</li>
            <li>Services</li>
            <li>Contact</li>
        </ul>

        <!-- Ordered list -->
        <!-- type : 1, A, a, I, i -->
        <!-- start="4" to start count from 4 -->
        <ol type="A">
            <li>Home</li>
            <li>About</li>
                <ol type="a">
                    <li>Nested about</li>
                    <li>Social link</li>
                </ol>
            <li>Contact</li>
                <ul>
                    <li>Phone</li>
                    <li>Email</li>
                </ul>
        </ol>
        <ol type="i">
            <li>Home</li>
            <li>About</li>
            <li>Services</li>
            <li>Contact</li>
        </ol>

        <ul>
            <li><a href="https://example.com">Website</a></li>
            <li><a href="mailto:m.ronydodger@gmail.com">Email</a></li>
            <li><a href="tel:+919692002521">Phone</a></li>
        </ul>
        
        <details>
            <summary>This is summary</summary>
            <p>Inside details-summary :</p>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Nam illo reprehenderit nisi eaque neque et libero corrupti! Ex, ipsa numquam. Nisi, nam aliquam nesciunt expedita nostrum id eos in debitis.</p>
        </details>

        <!-- div acts as a container to pack -->
        <div>
            <h1>It's a div #1</h1>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Illum?</p>
        </div>
        <div>
            <h1>It's a div #2</h1>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Names?</p>
        </div>

    </div>


    <div class="unknown">
        <fieldset>
            <legend>Choose your pokemon! ◓</legend>

            <input type="radio" id="Charmender" name="poke">
            <label for="Charmender" style="color: red;">Charmender 🔥</label><br/>

            <input type="radio" id="Bulbasaur" name="poke">
            <label for="Bulbasaur" style="color: green;">Bulbasaur 🌿</label><br/>

            <input type="radio" id="Squirtle" name="poke">
            <label for="Squirtle" style="color: blue;">Squirtle 💧</label>
        </fieldset>

        <figure>
            <blockquote>
                <p>Design is not how it look, but design is how it works.</p>
            </blockquote>
            <figcaption> -Steve Jobs, <cite>Apple</cite> </figcaption>
        </figure>
        <!-- same with css -->
        <figure>
            <blockquote id="bq">
                <p id="bqp">Design is not how it look, but design is how it works.</p>
            </blockquote>
            <figcaption> -Steve Jobs, <cite>Apple</cite> </figcaption>
        </figure>


        <!-- <frame>
        <frameset></frameset>
        <noframes></noframes> -->
    </div>

    <!-- The <area> element defines an area inside an image map that has predefined clickable areas. An image map allows geometric areas on an image to be associated with hypertext link. This element is used only within a <map> element. -->
    <map name="infographic">
        <area shape="rect" coords="184,6,253,27" href="https://mozilla.org" target="_blank" alt="Mozilla" />
        <area shape="circle" coords="130,136,60" href="https://developer.mozilla.org/" target="_blank" alt="MDN" />
        <area shape="poly" coords="130,6,253,96,223,106,130,39" href="https://developer.mozilla.org/docs/Web/Guide/Graphics" target="_blank" alt="Graphics" />
        <area shape="poly" coords="253,96,207,241,189,217,223,103" href="https://developer.mozilla.org/docs/Web/HTML" target="_blank" alt="HTML" />
        <area shape="poly" coords="207,241,54,241,72,217,189,217" href="https://developer.mozilla.org/docs/Web/JavaScript" target="_blank" alt="JavaScript" />
        <area shape="poly" coords="54,241,6,97,36,107,72,217" href="https://developer.mozilla.org/docs/Web/API" target="_blank" alt="Web APIs" />
        <area shape="poly" coords="6,97,130,6,130,39,36,107" href="https://developer.mozilla.org/docs/Web/CSS" target="_blank" alt="CSS" />
    </map>
    <img usemap="#infographic" src="media/mdn.png" alt="MDN infographic" style="display: block; margin: 0 auto; width: 260px; height: 248px;"/>
    
    <div oncontextmenu="return false">
        <div class="txt">You can't right-click over me!</div>
    </div>

    <!-- Media -->
    <div class="media">
        <hr>

        <img id="spidey" src="media/heySpidey.jpg" alt="Spider-man image">
        <img src="media/heySpidey.jpg" height="100px" width="155px"> <!--not recomended directly; use CSS as above-->
        <img src="media/heySpidey.jpg" height="100px"> <!--if only height/width given, another will be set automatically; no change in aspect ratio-->

        <audio controls>
        <source src="media/pusher.mp3" type="audio/mpeg">Your browser does not support the audio element.</audio>

        <video src="media/flip.mp4" controls width="560px"></video>
        <video src="media/fly.mp4" controls autoplay loop width="480px"></video>

        <video width="480" height="320" controls>
        <source src="media/flip.mp4" type="video/mp4">Your browser does not support the video tag.</video>
        
        <!-- <br> -->
        <!-- iframe is mostly used for youtube video embedding -->
        <iframe src="https://bing.com" frameborder="0" width="560" height="315"></iframe>
        <!-- I hate T-series : they keeps all songs by rules; below commented songs not working -->
        <!-- <iframe width="560" height="315" src="https://www.youtube.com/embed/raPwjc8br1U" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe> -->
        <!-- <iframe width="560" height="315" src="https://www.youtube.com/embed/CCCunpnok5g" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe> -->
        <iframe width="560" height="315" src="https://www.youtube.com/embed/5IEbR79kBPY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>


    <hr>
    <!-- Table -->
    <div class="table">
        <h2>Table</h2>

        <table>
            <caption>Programming Languages</caption>
            <thead>
                <tr>
                    <th>No.</th>
                    <th>Language</th>
                    <th>Uses</th>
                    <!-- colspan attribute captures multiple columns -->
                    <!-- <th colspan="3">Uses</th> : captures three columns (like, ML AI DSA (3 columns) in python Uses  -->
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>1</td>
                    <td>Javascript</td>
                    <td>Web</td>
                </tr>
                <tr>
                    <td>2</td>
                    <td>Python</td>
                    <td>Machine</td>
                </tr>
                <tr>
                    <td>3</td>
                    <td>Java</td>
                    <td>Android</td>
                </tr>
            </tbody>
            <tfoot>
                <tr>
                    <td>&nbsp;</td>
                    <td>Total:</td>
                    <td>100k</td>
                </tr>
            </tfoot>
        </table>
        
    </div>


    <hr>


    <!-- Forms and Input -->
    <form action=""></form>
    <input type="text">
    <textarea name="" id="" cols="30" rows="10"></textarea>
    <button></button>
    <select name="" id=""></select>
    <optgroup></optgroup>
    <option value=""></option>
    <label for=""></label>
    <fieldset></fieldset>
    <legend></legend>

    <!-- Input -->
    <label for="name">Name (4-8 character) :</label>
    <input type="text" id="name" name="name" placeholder="Text" required minlength="4" maxlength="8" size="10">
    <input type="number" placeholder="Number" name="" id="" min="0">
    <input type="tel" placeholder="+91 XXXXXXXXXX" name="" id="">
    <input type="email" placeholder="abc@xyz.com" name="" id="">
    <input type="url" placeholder="www.xyz.com" name="" id="">
    <input type="password" placeholder="password" name="" id="">
    <input type="search" placeholder="🔍 Search here" name="" id="">
    <input type="time" name="" id="">
    <input type="date" name="" id="">
    <input type="datetime-local" name="" id="">
    <input type="week" name="" id="">
    <input type="month" name="" id="">
    <input type="button" name="" id="">
    <input type="submit" name="" id="">
    <input type="reset" name="" id="">
    <input type="checkbox" name="" id="">
    <input type="radio" name="" id="">
    <input type="range" name="" id="">
    <input type="color" name="" id="">
    <input type="hidden" name="">
    <input type="file" name="" id="">
    <input type="image" src="media/iconpg.png" alt="">


    <!-- Form -->
    <div class="contact">

        <h2>Contact Form</h2>
        <form action="form.php" method="">    <!-- <form action="backend_file_name.php" method="GET/POST/DIALOG"> -->

            <!-- element of form; different element for different input -->

            <div>
                <label for="name">Name: </label>
                <input type="text" name="myName" placeholder="Enter your name" id="name" required>
            </div>
            <div>
                <label for="mailme">Email: </label>
                <input type="email" name="myEmail" placeholder="xyz@email.com" id="mailme" required>
            </div>
            <div>
                <label for="password">Password:</label>
                <input type="password" name="password" placeholder="" required>
            </div>
            <div>
                <label for="age">Age: </label>
                <input type="number" name="myAge" id="age">
            </div>
            <!--<div>
                 <label for="genderidm">
                    <input type="radio" name="gender" value="Male" id="genderidm">Male
                </label>
                <label for="genderidf">
                    <input type="radio" name="gender" value="Female" id="genderidf">Female
                </label> 
            </div>-->
            <div>
                <label>Gender :</label>
                <!-- Male <input type="radio" name="myGender" id=""> Female <input type="radio" name="myGender" id=""> -->
                <label for="genderidm">
                    <input type="radio" name="gender" value="Male" id="genderidm"> Male
                </label>
                <label for="genderidf">
                    <input type="radio" name="gender" value="Female" id="genderidf"> Female
                </label>
                <!-- 'name' must be same so that only one option can be choosen -->
            </div>
            <div>
                <label for="date">Date: </label>
                <input type="date" name="myDate" id="date">
            </div>
            <div>
                <label for="mytime">Time: </label>
                <input type="time" name="myTime" id="mytime">
            </div>
            
            <label for="month">Birthday</label>
            <select name="month" id="">
                <option value="0" selected disabled>Month</option>
                <option value="jan">jan</option>
                <option value="feb">feb</option>
                <option value="mar">mar</option>
                <option value="apr">apr</option>
                <option value="may">may</option>
                <option value="jun">jun</option>
                <option value="jul">jul</option>
                <option value="aug">aug</option>
                <option value="sep">sep</option>
                <option value="oct">oct</option>
                <option value="nov">nov</option>
                <option value="dec">dec</option>
            </select>

            <div>
                <label for="want">What do you want?</label>
                <select name="want" id="want">
                    <option value="site" selected>Static Website</option>  <!--selected - to firsty set-->
                    <option value="web">Dynamic Website</option>
                    <option value="app">Application</option>
                </select>
            </div>
            <select name="want" id="want">
                <option value="select" selected disabled>What do you want?</option>
                <option value="web">Website</option>
                <option value="app">Application</option>
            </select>
            <div>
                <label for="explain">Whats your project:</label>
                <br>
                <textarea name="explain" id="explain" cols="30" rows="6" placeholder="Describe.."></textarea>
            </div>
            <div>
                <input type="checkbox" name="promotion" id="mail">
                <label for="mail">Want promotion mails.</label>
                <br>
                <input type="checkbox" name="info" id="agree" checked>
                <label for="agree">Agree to all rules.</label>
            </div>
            <div>
                <label for="mail">Want promotion mails.</label>
                <input type="checkbox" name="promotion" id="mail">
                <br>
                <input type="checkbox" name="info" id="agree" checked>  <!--checked - to check(tick) previously-->
                <label for="agree">Agree to all rules.</label>
            </div>

            <div>
                <input type="reset" value="Reset">
                <input type="submit" value="Submit">
            </div>
        </form>
    </div>

    <!-- The <address> element indicates that the enclosed HTML provides contact information for a person or people, or for an organization including contact information that is needed, such as a physical address, URL, email address, phone number, social media handle, geographic coordinates, and so forth.. -->
    <p>Contact the author of this page:</p>
    <address>
        <a href="mailto:pratyush23pro@gmail.com">pratyush23pro@gmail.com</a><br>
        <a href="tel:+919692002521">9692002521</a>
    </address>

    <footer></footer>

    <noscript></noscript>

    <script></script>
    <script src="script.js"></script>

</body>
</html>
```
