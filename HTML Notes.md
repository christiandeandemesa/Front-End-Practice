# HTML (Hyper Text Markup Language) Introduction
```html
<!--This is a comment in HTML.-->
<!--Declares that this is an HTML5 document.-->
<!DOCTYPE html>
<!--The root element contains the head and body elements.
    The lang attribute declares the page's language and country (e.g. "en" is english, and "US" is the United States).-->
<html lang="en-US">
<!--The head element contains meta information.-->
<head>
    <!--This shows the text in the page's tab.-->
    <title>Page Title</title>
</head>
<!--The body element contains all the visible information.-->
<body>
    <!--This shows the text as a large heading.
        Notice that most elements are composed of a start tag <h1>, the element content (i.e. text), and an end tag </h1>.-->
    <h1>This is a heading.</h1>
    <!--This creates a line break between text.
        Notice some elements are empty elements, which are only a start tag <br>.-->
    <br>
    <!--This shows the text as a paragraph.
        Paragraphs always start on a new line, and are given margins before and after it.-->
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

## HTML Images
```html
<!--This embeds an image where path to the image in the src attribute, and text that appears if the image fails to load in the alt
    attribute.
    The width and height attributes size the image in pixels.
    The below example uses an absolute URL (an image hosted on another website), but you can use a relative URL for images you saved (e.g. src="FNAF.jpg").-->
<img src="https://cdn.akamai.steamstatic.com/steam/apps/747660/capsule_616x353.jpg?t=1639706417" alt="FNAF Security Breach" width="600" height="400">
```

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
- CSS is used to format the layout (i.e. style) HTML.
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

## ADD INFO
- [<map>](https://www.w3schools.com/tags/tag_map.asp)
- [<area>](https://www.w3schools.com/tags/tag_area.asp)
- [<picture>](https://www.w3schools.com/tags/tag_picture.asp)