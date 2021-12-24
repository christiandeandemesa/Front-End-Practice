# HTML (Hyper Text Markup Language) Introduction
```html
<!--This is a comment in HTML.-->
<!--Declares that this is an HTML5 document.-->
<!DOCTYPE html>
<!--The root element contains the head and body elements.
    The lang attribute declares the page's language and country (e.g. "en" is english, and "US" is the United States).-->
<html lang="en-US">
<!--The head element contains non-visible meta information.-->
<head>
    <!--This shows the text in the page's tab.-->
    <title>Page Title</title>
</head>
<!--The body element contains visible information.-->
<body>
    <!--This shows the text as a large heading.
        Notice that most elements are composed of a start tag <h1>, the element content (i.e. text), and an end tag </h1>.-->
    <h1>This is a heading.</h1>
    <!--This creates a line break between text.
        Notice some elements are empty elements, which are only a start tag <br>.-->
    <br>
    <!--This shows the text as a paragraph.-->
    <p>This is a paragraph.</p>
</body>
</html>
```

# HTML Basic Examples
## HTML Headings
```html
<h1>This is the biggest heading.</h1>
<!--<h2> to <h5> removed for brevity.-->
<h6>This is the smallest heading.</h6>
```

## HTML Links
```html
<!--The a element defines a hyperlink.
    The text will be a hyperlink to the destination in the href attribute.-->
<a href="https://www.w3schools.com/html/default.asp">This is a link</a>
```

## HTML images
```html
<!--This embeds an image where path to the image in the src attribute, and text that appears if the image fails to load in the alt
    attribute.
    The width and height attributes size the image in pixels.
    The below example uses an absolute URL (an image hosted on another website), but it is recommended to use a relative URL (an image you saved).-->
<img src="https://cdn.akamai.steamstatic.com/steam/apps/747660/capsule_616x353.jpg?t=1639706417" alt="FNAF Security Breach" width="600" height="400">
```

## Relative file paths
- <img src="picture.jpg"> means picture.jpg is in the same folder as the current HTML.
- <img src="images/picture.jpg"> means picture.jpg is in a folder named images, and that folder in the same folder as the current HTML.
- <img src="/images/picture.jpg"> means picture.jpg is in a folder named images, and that folder is in the root folder.
- <img src="../picture.jpg"> means picture.jpg is in a folder named images, and that folder and the folder the current HTML is in are in the same folder.

# HTML Attributes
## The title attribute
```html
<!--The title attribute will show its text when you hover over the element content.-->
<p title="This is a tooltip">Element Content</p>
```

## Single or Double Quotes?
```html
<!--If the text uses single quotes, wrap it in double quotes.-->
<p title="Dwayne 'The Rock' Johnson"></p>
<!--If the text uses double quotes, wrap it in single quotes.-->
<p title='Dwayne "The Rock" Johnson'></p>
```

# HTML Paragraphs
## HTML Horizontal Rules
```html
<!--This creates a line break with a horizontal line between text.-->
<hr>
```

## The Poem Problem
```html
<!--The below will display on a single line.-->
<p>
    Once upon a midnight dreary,
    While I pondered weak and weary...
</p>
<!--The pre element formats the text as it is written.-->
<pre>
    Once upon a midnight dreary,
    While I pondered weak and weary...
</pre>
```

# HTML Text Formatting
## HTML <sub> element
```html
<!--The sub element makes the text appear as a subscript.-->
<p>H<sub>2</sub>O</p>
```

## HTML <sup> element
```html
<!--The sup element makes the text appear as a superscript.-->
<p>Footnote<sup>[1]</sup></p>
```

# HTML Quotation and Citation Elements
## HTML <blockquote> for Quotations
```html
<!--The blockquote element places all the text in a quote block.
    The cite attribute is the destination to where the quote came from.-->
<blockquote cite="https://www.philosophybasics.com/general_quotes.html">“This is patently absurd; but whoever wishes to become a philosopher must learn not to be frightened by absurdities” – Bertrand Russell</blockquote>
```

## HTML <bdo> for Bi-Directional Override
```html
<!--The bdo element overrides the text's direction.
    The dir attribute is given an "ltr" value for text to be left to right, or a "rtl" value for text to be right to left.-->
<p><bdo dir="rtl">This text is read right to left</bdo></p>
```

# HTML Styles - CSS
- CSS is used to format the layout (i.e. style) of HTML.
- Check the CSS Notes.md for more information.

## Inline CSS
```html
<!--Styles all the element content.-->
<h1 style="color:red">A red heading</h1>
```

## Internal CSS
```html
<!--Internal CSS styles all the content in an HTML page.-->
<head>
<!--The style element is placed within the head element.-->
<style>
    /*Styling is written similar to a CSS file.*/
    body {background-color: blue;}
    h1 {color: red;}
</style>
</head>
<body>
    <h1>The text is blue, and the background is red</h1>
</body>
```

## External CSS
```html
<!--External CSS links this HTML page to a CSS file.-->
<head>
    <!--The link tag links the HTML page to an external resource.
    The rel attribute specifies the relationship of the  linked document the HTML page.
    The href attribute links to the CSS file's path.-->
    <link rel="stylesheet" href="styles.css">
</head>
```
- It is recommended to use external CSS.

# HTML Links
## The target attribute
```html
<!--The target attribute specifies how the linked document is opened.-->
<a href="https://www.w3schools.com/html/default.asp" target="_self">This is a link</a>
```
- "_self" replaces the current page with the linked page.
- "_blank" opens the linked page in a new tab.

## Use an image as a link
```html
<!--The image will be a hyperlink.-->
<a href="https://store.steampowered.com/app/747660/Five_Nights_at_Freddys_Security_Breach/"><img src="https://cdn.akamai.steamstatic.com/steam/apps/747660/capsule_616x353.jpg?t=1639706417" alt="FNAF Security Breach"></a>
```

## Link to an email address
```html
<!--mailto: links to the user's email program.-->
<a href="mailto:someone@example.com">Send email</a>
```

## Button as a link
```html
<!--The button element creates a button with the text displayed in the button.
    Check the JS Notes.md for more information.-->
<button onclick="document.location='default.asp'">HTML Tutorial</button>
```

# HTML Links - Create Bookmarks
```html
<!--Use the id attribute to create a bookmark.-->
<h1 id="bookmark">This is bookmarked</h1>
<!--Clicking on the below text will jump up to the bookmark in the same page.
    The # signifies the id.-->
<a href="#bookmark">This jumps to the bookmark</a>
<!--Clicking on the below text will jump to the bookmark on another page.-->
<a href="index.html#bookmark">This jumps to the bookmark in index.html</a>
```

# HTML Images
## Animated images
```html
<!--You can also embed animated GIFs.-->
<img src="https://c.tenor.com/0kttxe9UTw8AAAAd/fnaf-five-nights-at-freddys.gif" alt="Glamrock Freddy">
```

## Common image formats
- Image file types supported in all browsers are .apng, .gif, .ico, .cur, .jpg, .jpeg, .jiff, .pjpeg, .pjp, .png, and .svg.

# HTML Image Maps
- An image map is an image with different clickable areas.
```html
<!--The usemap attribute's value must include a #, and the the value of the map element's name attribute.-->
<img src="workplace.jpg" alt="Workplace" usemap="#workmap">
<!--The map element is used to create an image map.
    The name attribute specifies a name for the element.-->
<map name="workmap">
    <!--The area element defines a clickable area in an image map.
        The shape attribute defines the shape of the area element.
        The coords attribute specifies the coordinates of the area.
        The coordinates for a rectangle will be the top left corner (e.g. 33,44), and the bottom right corner (e.g. 270,350).-->
    <area shape="rect" coords="34,44,270,350" alt="Computer" href="computer.htm">
    <!--The coordinates for a circle will be the center (e.g. 337,300), and the radius (e.g. 44).-->
    <area shape="circle" coords="337,300,44" alt="Coffee" href="coffee.htm">
    <!--The coordinates for a polygon will be the edges of the area, but there is no set limit for the number of coordinates.-->
    <area shape="poly" coords="140,121,181,116,204,160,204,222,191,270,140,329,85,355,58,352,37,322,40,259,103,161,128,147" href="croissant.htm">
</map>
```

# HTML <picture> Element
```html
<!--The picture element specifies which images will show based on the browser screen's width.-->
<picture>
    <!--The source element specifies multiple media attributes.
    The media attribute specifies which media the HTML is optimized for.
    The srcset attribute is used instead of the src attribute for picture elements.-->
    <source media="(min-width: 650px)" srcset="img_food.jpg">
    <source media="(min-width: 465px)" srcset="img_car.jpg">
    <!--This image will show if all the previous images do not show.-->
    <img src="img_girl.jpg">
</picture>
```

# HTML Favicon
- A favicon is an image that shows in the browser's tab, and can be created [here](https://www.favicon.cc/).
```html
<head>
    <title>My Page Title</title>
    <!--The type attribute for the link element specifies the media type.-->
    <link rel="icon" type="image/x-icon" href="/images/favicon.ico">
</head>
```

# HTML Tables
```html
<!--The caption element places text as a header above the table.-->
<caption>My favorite anime</caption>
<!--The table element creates a table.-->
<table>
    <!--The tr (i.e. table row) element defines the horizontal row in a table.-->
    <tr>
        <!--The th (i.e. table header) element defines a cell in the table as a header.-->
        <th>Anime</th>
    </tr>
    <tr>
        <!--The td (i.e. table data) element defines a cell in the table.-->
        <td>Toradora</td>
    </tr>
    <tr>
        <td>Nichijou</td>
    </tr>
</table>
```

## Vertical table headers
```html
<table>
    <tr>
        <th>Anime</th>
        <td>Konasuba</td>
        <td>Haikyuu</td>
    </tr>
</table>
```

## HTML table - colspan
```html
<table>
    <tr>
        <!--The colspan attribute defines how many cells the cell should stretch across horizontally.
            The colspan attribute can also be used on the td element.-->
        <th colspan="2">Name</th>
    </tr>
    <tr>
        <td>Christian</td>
        <td>Demesa</td>
    </tr>
</table>
```

## HTML table - rowspan
```html
<table>
    <tr>
        <!--The rowspan attribute defines how many cells the cell should stretch across vertically.
            The rowspan attribute can also be used on the td element.-->
        <th rowpan="2">Name</th>
        <td>Christian</td>
    </tr>
    <tr>
        <td>Demesa</td>
    </tr>
</table>
```

# HTML Table colgroup
```html
<table>
    <!--The colgroup element groups vertical columns.-->
    <colgroup>
        <!--The col element specifies how many column(s) are grouped.
            The span attribute specifies how many cells the cell should stretch across.-->
        <col span="1">
        <col span="2" style="background-color: yellow">
    </colgroup>
    <!--Other table tags removed for brevity.-->
</table>
```

# HTML Lists
## Unordered HTML list
- An unordered list lists items with bullet points.
```html
<!--The ul (i.e. unordered list) element defines an unordered list.-->
<ul>
    <!--The li element defines a list item.-->
    <li>Milk
        <!--Notice you can nest unordered lists.-->
        <ul>
            <li>1%</li>
            <li>Soy</li>
        </ul>
    </li>
    <li>Cookies</li>
</ul>
```

## Ordered HTML list
```html
<!--The ol (i.e. ordered list) element defines an ordered list.
    The type attribute specifies the list item marker.
    The start attribute is used with number list markers to specify which number to start at.-->
<ol type="1" start="1">
    <li>Go to the gym
        <!--Notice you can nest ordered lists.-->
        <ol>
            <li>Cardio</li>
            <li>Weight lifting</li>
        </ol>
    </li>
    <li>Buy groceries</li>
</ol>
```
- Values for the type attribute include "1" (numbers), "A" (uppercase letters), "a" (lowercase letters), "I" (uppercase Roman numbers), and "i" (lowercase Roman numbers).

## HTML description lists
```html
<!--The dl (i.e. description list) element defines a list of terms.-->
<dl>
    <!--The dt (i.e. description term) element defines the term.-->
    <dt>Milk</dt>
    <!--The dd element defines an indented description for each term.-->
    <dd>1% or soy</dd>
    <dt>Cookies</dt>
    <dd>Chocolate chip please</dd>
</dl>
```

# HTML Block and Inline Elements
## Block-level elements
- [Block-level elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Block-level_elements) start on a new line, take up the full width, and have a top and bottom margin.

## Inline elements
- [Inline elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements) do not start on a new line, take up as much width as the element content, and do not have a top and bottom margin.

## The <div> element
```html
<body>
    <!--The div element is used as a container for other elements.-->
    <div>
        <p>Hello World</p>
    </div>
</body>
```

## The <span> element
```html
<!--The span element is used to style specific parts of the text.-->
<p><span style="color:red">WARNING</span> there is trouble</p>
```

# HTML Iframes
```html
<!--The iframe element embeds a web page.
    All the attributes for the img element also apply to the iframe element.-->
<iframe src="https://www.w3schools.com/html/html_iframe.asp">
```

# HTML JavaScript
```html
<body>
    <!--The script element is placed within the body element.-->
    <script>
        // Check the JS Notes.md for more information.
        document.getElementById("demo").innerHTML = "Hello JavaScript!";
    </script>
    <!--The noscript element displays the text if the browser does not support scripts.-->
    <noscript>Sorry, your browser does not support JavaScript!</noscript>
</body>
```
- It is recommended to use external JS (i.e. JavaScript).

# HTML - The Head Element
## The HTML <meta> element
- Metadata is used by browsers to display content or reload the page, by search engines for keywords, and other web services.
```html
<head>
    <!--The meta element defines metadata.
        The charset attribute specifies the character encoding for HTML.
        It is recommended to use "UTF-8".-->
    <meta charset="UTF-8">
    <!--The name attribute for a meta element specifies what type of metadata.
        The content attribute is the value associated with the name attribute.
        The below metadata defines keywords for search engines.-->
    <meta name="keywords" content="HTML, CSS, JavaScript">
    <!--The below metadata defines a description for the web page.-->
    <meta name="description" content="HTML Notes">
    <!--The below metadata defines the author for a web page.-->
    <meta name="author" content="Christian Demesa">
    <!--The http-equiv attribute provides an HTTP header.
        The below metadata refreshes the HTML every 30 seconds.-->
    <meta http-equiv="refresh" content="30">
    <!--The below metadata sets the viewport (i.e. the visible area of a web page).
        "width=device-width" specifies that the width of web page follows the width of the device's screen.
        "initial-scale=1.0" sets the initial zoom level when the web page loads.-->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
```

## The HTML <base> element
```html
<head>
    <!--There can only be one base element, and it specifies the base URL and/or target for all relative URLs.-->
    <base href="https://www.marvel.com/" target="_blank">
</head>
```