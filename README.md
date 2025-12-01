- [Section 1: CSS FUNDAMENTALS](#section-1-css-fundamentals)
  - [WHAT IS CSS?](#what-is-css)
  - [A CSS SYNTAX](#a-css-syntax)
  - [HOW TO ADD CSS](#how-to-add-css)
    - [External CSS](#external-css)
    - [Internal CSS](#internal-css)
    - [Inline CSS](#inline-css)
  - [STYLING TEXT](#styling-text)

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

- **text-transform**
  - none - No transformation. Text renders as it is
  - capitalize - Transforms the first character of each word to uppercase
  - uppercase - Transforms all characters to uppercase
  - lowercase - Transforms all characters to lowercase
