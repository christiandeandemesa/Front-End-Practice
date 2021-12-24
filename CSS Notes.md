# CSS (Cascading Style Sheets) Introduction
- CSS is used to format the layout (i.e. style) of HTML.
- All of the following information and examples will be used for external CSS, but can be used for inline and internal CSS (If you have not read the HTML Notes.md, stop here and read it first).

# CSS Syntax
```css
/*  This is a comment in CSS  */
/*  The text before the curly brackets is the selector, or what element(s) in the HTML will be styled.
    Each pair of words separated by semicolons, and within the curly brackets are known as declarations.
    The first word before the colon in each declaration is the property, which is what styling you are applying to the selector.
    The second word after the colon in each declaration is the value, which is what kind of property you are using.  */
p {color: blue;}
```

# CSS Selectors
- Selectors are divided into five categories:
    1. Simple selectors select elements based on their element, class, or id.
    2. Combinator selectors select elements based on a specific relationship between them.
    3. Pseudo-class selectors select elements based on a specific state.
    4. Pseudo-element selectors select parts of an element.
    5. Attribute selectors select elements based on attribute or attribute value.

## The CSS element selector
```css
/*  The selector states all <p> elements will be styled.  */
p {color: blue;}
```

## The CSS class selector
```css
/*  The class selector states all elements with a class attribute with a value of "class" (e.g. <h1 class="class>) will be styled.
    Notice how the class selector has a period in front of it, and a class' value cannot start with a number.  */
.class {color: blue;}
```

## The CSS id selector
```css
/*  The id selector states all elements with an id attribute with a value of "id" (e.g. <div id="id">) will be styled.
    Notice how the id selector has a hash in front of it, and an id's value cannot start with a number.  */
#id {color: blue;}
```

## The CSS universal selector
```css
/*  The universal selector states every element will be styled.  */
* {color: blue;}
```

## The CSS grouping selector
```css
/*  You can group selectors by separating them with commas to give them all the same styling.  */
p, .class, #id {color: blue;}
```

# How to Add CSS
## Multiple Style Sheets
```css
    /*  style.css  */
    p {color: red;}
```
```html
<head>
    <!--Because the internal CSS is below the external CSS, all the <p> elements' text will be blue.
        If you want all the <p> elements' text to be red, you will have to place the external CSS below the internal CSS.-->
    <link rel="stylesheet" type="text/css" href="style.css">
    <style>
        p {color: blue;}
    </style>
</head>
```

## Cascading Order
- If there are multiple style sheets, the priority will be as follows:
    1. Inline CSS.
    2. Internal or external CSS.
    3. Browser default.

# CSS Colors
## CSS color names
```css
/*  The color property specifies the color of the text.  */
p {color: tomato;}
```

## CSS background color
```css
/*  The background-color property specifies the color of the background behind the text.  */
p {background-color: rebeccapurple;}
```

# CSS RGB Colors
## RGB value
- You can specify a color by its RGB value where the first number is how red, the second number is how green, and the third number is how blue it is.
```css
/*  Each of the rgb numbers has a range from 0 to 255.
    Test RGB values [here](https://www.w3schools.com/css/css_colors_rgb.asp).  */
p {color: rgb(0, 0, 255);}
```

## RGBA value
- The RGBA value adds a fourth number that determines how opaque the color is.
```css
/*  The "a" (i.e. fourth) number has a range from 0.0 to 1.0 in increments of 0.1.
    Test RGBA values [here](https://www.w3schools.com/css/css_colors_rgb.asp).  */
p {color: rgba(0, 0, 255, 0.5);}
```

# CSS HEX Colors
- You can specify a color by its hexadecimal (i.e. HEX) value where the first pair of values is how red, the second pair of values is how green, and the third pair of numbers is how blue it is.
```css
/*  Each of the hex values has a range from 0 to f.
    Test HEX values [here](https://www.w3schools.com/css/css_colors_hex.asp).  */
p {color: #0000ff;}
/*  If each pair in the hex value have the same value, you can shorthand the hex value as three digits.  */
p {color: #00f;}
```

# CSS HSL Colors
## HSL value
- You can specify a color by its HSL value where the first number is the hue, the second number is the saturation, and the the third number is the lightness.
```css
/*  The hue number has a value from 0 to 360.
    The saturation and lightness have values from 0% to 100%.
    Test HSL values [here](https://www.w3schools.com/css/css_colors_hsl.asp).  */
p {color: hsl(240, 100%, 50%);}
```

## HSLA value
- The HSLA value adds a fourth value that determines how opaque the color is.
```css
/*  The "a" (i.e. fourth) number has a range from 0.0 to 1.0 in increments of 0.1.
    Test HSLA values [here](https://www.w3schools.com/css/css_colors_hsl.asp).  */
p {color: hsla(240, 100%, 50%, 0.5);}
```

# CSS Background Image
```css
/*  The background-image property specifies an image in the background.
    The url function is used to include an absolute or relative URL.  */
body {background-image: url("picture.jpg");}
```

## CSS background-repeat
```css
/*  The background-repeat property specifies how the background image is repeated.
    The repeat-x value repeats the image horizontally, the repeat-y value repeats the image vertically, and the no-repeat value does not repeat the image.  */
body {
    background-image: url("picture.jpg");
    background-repeat: repeat-x;
}
```

## CSS background-position
```css
/*  The background-position property specifies the position of the background image.  */
body {
    background-image: url("picture.jpg");
    background-position: center;
}
```

# CSS Background Attachment
```css
/*  The background-attachment property specifies if the background image will scroll with the web page or not.
    The scroll value will have the background image scroll, and the fixed value will not have the background image scroll.  */
body {
    background-image: url("picture.jpg");
    background-attachment: fixed;
}
```

# CSS Background Shorthand
```css
body {
    background-color: blue;
    background-image: url("picture.jpg");
    background-repeat: no-repeat;
    background-attachment: fixed;
    background-position: center;
}
/*  Below is a shorthand way to write all or some of the above background properties in the following order: background-color, background-image, background-repeat, background-attachment, and/or background-position.  */
body {background: blue url("picture.jpg") no-repeat fixed center;}
```

# CSS Borders