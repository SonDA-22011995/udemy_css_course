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
