- [Section 1: CSS FUNDAMENTALS](#section-1-css-fundamentals)
  - [WHAT IS CSS?](#what-is-css)
  - [A CSS SYNTAX](#a-css-syntax)
  - [HOW TO ADD CSS](#how-to-add-css)
    - [External CSS](#external-css)
    - [Internal CSS](#internal-css)
    - [Inline CSS](#inline-css)
  - [STYLING TEXT](#styling-text)
  - [CSS Selectors](#css-selectors)
    - [CSS Combinators](#css-combinators)
      - [Simple selectors](#simple-selectors)

# Section 1: CSS FUNDAMENTALS

## WHAT IS CSS?

- Cascading Style Sheets
- CSS describes the visual style and presentation of the content
  written in HTML
- CSS consists of countless properties that developers use to format
  the content: properties about font, text, spacing, layout, etc

## A CSS SYNTAX

```
h1 {
 color: blue;
 text-align: center;
 font-s
}

```

## HOW TO ADD CSS

### External CSS

```
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="mystyle.css" />
  </head>
  <body>
    <h1>This is a heading</h1>
    <p>This is a paragraph.</p>
  </body>
</html>
```

### Internal CSS

```
<!DOCTYPE html>
<html>
  <head>
    <style>
      body {
        background-color: linen;
      }

      h1 {
        color: maroon;
        margin-left: 40px;
      }
    </style>
  </head>
  <body>
    <h1>This is a heading</h1>
    <p>This is a paragraph.</p>
  </body>
</html>
```

### Inline CSS

```
<!DOCTYPE html>
<html>
    <body>
        <h1 style="color:blue;text-align:center;">This is a heading</h1>
        <p style="color:red;">This is a paragraph.</p>
    </body>
</html
```

## STYLING TEXT

- **font-size**: Property is used to specify the size of the text/font.

  - Absolute sizes:px:

    - Pixels offers fixed and precise control over the font size.-
    - xx-small, x-small, small, medium, large, x-large, xx-large. These keywords has a predefined set of sizes in browsers.

  - Relative sizes:
    - em: This unit is relative to the font size of the parent element.
    - rem: This unit is relative to the font size of the root HTML element.
    - %: This unit is relative to the font size of the parent element
      smaller and larger: These units adjust the font size relative to the parent element.

```
<div style="font-size: 20px;">
  <p style="font-size: 1.5em;">Text này = 1.5 × 20px = 30px</p>
</div>
```

```
<html style="font-size: 16px;">
  <div style="font-size: 40px;">
    <p style="font-size: 2rem;">Text này = 2 × 16px = 32px</p>
  </div>
</html>
```

```
<div style="font-size: 20px;">
  <p style="font-size: 150%;">Text này = 150% × 20px = 30px</p>
</div>

```

```
h1 {
  font-size: 40px;
}
```

- **font-family**: property specifies the font for an element.

```
p.normal {
  font-style: normal;
}
```

- **text-transform**: property is used to control the capitalization of text in an element.

  - none - No transformation. Text renders as it is
  - capitalize - Transforms the first character of each word to uppercase
  - uppercase - Transforms all characters to uppercase
  - lowercase - Transforms all characters to lowercase

- **font-style**: property specifies the font style for a text.
  - normal - The text is shown normally
  - italic - The text is shown in italics
  - oblique - The text is "leaning" (oblique is very similar to italic)
- **line-height**: property specifies the height of a line.**Note**: Negative values are not allowed.

```
div.a {
  line-height: normal;
}

div.b {
  line-height: 1.6;
}

div.c {
  line-height: 80%;
}

div.d {
  line-height: 200%;
}
```

## CSS Selectors

### CSS Combinators

#### Simple selectors

- The CSS id Selector: The id selector uses the id attribute of an HTML element to select a specific element.

```
#para1 {
  text-align: center;
  color: red;
}

```

- The CSS class Selector: The class selector selects HTML elements with a specific class attribute..

```
.center {
  text-align: center;
  color: red;
}
```

- The CSS Universal Selector: The universal selector (\*) selects all HTML elements on the page.

```
* {
  text-align: center;
  color: blue;
}

```

- The CSS Grouping Selector: Selects all the HTML elements with the same style definitions

```
h1, h2, h3, p, li {
  font-family: sans-serif;
}

```
