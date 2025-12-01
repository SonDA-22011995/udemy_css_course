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
      - [Descendant combinator (space)](#descendant-combinator-space)
      - [Child Combinator (\>)](#child-combinator-)
      - [Next Sibling Combinator (+)](#next-sibling-combinator-)
      - [Subsequent-sibling Combinator (~)](#subsequent-sibling-combinator-)
    - [CSS Pseudo-classes](#css-pseudo-classes)
    - [CSS Pseudo-elements](#css-pseudo-elements)
    - [CSS Attribute Selectors](#css-attribute-selectors)
      - [CSS \[attribute\] Selector](#css-attribute-selector)
      - [CSS \[attribute="value"\] Selector](#css-attributevalue-selector)
      - [CSS \[attribute~="value"\] Selector](#css-attributevalue-selector-1)
      - [CSS \[attribute|="value"\] Selector](#css-attributevalue-selector-2)
      - [CSS \[attribute^="value"\] Selector](#css-attributevalue-selector-3)
      - [CSS \[attribute$="value"\] Selector](#css-attributevalue-selector-4)
      - [CSS \[attribute\*="value"\] Selector](#css-attributevalue-selector-5)
  - [DEFINING COLORS IN CSS](#defining-colors-in-css)
    - [RGB / RGBA NOTATION](#rgb--rgba-notation)
    - [HEXADECIMAL NOTATION](#hexadecimal-notation)
  - [CONFLICTING SELECTORS AND DECLARATIONS](#conflicting-selectors-and-declarations)
    - [Important CSS rule](#important-css-rule)
  - [CSS inheritance](#css-inheritance)
    - [Basic Concept](#basic-concept)
    - [Using Inheritance on body](#using-inheritance-on-body)
    - [Inheritance on a Smaller Scale](#inheritance-on-a-smaller-scale)
    - [Not All Properties Are Inherited](#not-all-properties-are-inherited)
    - [Universal Selector vs. body](#universal-selector-vs-body)
    - [Key Takeaways](#key-takeaways)
  - [Types of boxes in CSS](#types-of-boxes-in-css)
    - [Block-level Boxes](#block-level-boxes)
    - [INLINE ELEMENTS](#inline-elements)
    - [INLINE-BLOCK BOXES](#inline-block-boxes)
  - [ABSOLUTE POSITIONING](#absolute-positioning)
    - [Normal Flow (default flow)](#normal-flow-default-flow)
    - [ABSOLUTE POSITIONING](#absolute-positioning-1)
    - [Example](#example)
  - [THE CSS BOX MODEL](#the-css-box-model)

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

#### Descendant combinator (space)

- The descendant combinator matches all elements that are descendants (children, grandchildren, etc.) of a specified element.

```
div p {
  background-color: yellow;
}
```

#### Child Combinator (>)

- The child combinator selects all elements that are direct children of a specified element.

```
div > p {
  background-color: yellow;
}

```

#### Next Sibling Combinator (+)

- The next sibling combinator is used to select an element that is directly after a specific element.

```
div + p {
  background-color: yellow;
}
```

#### Subsequent-sibling Combinator (~)

- The subsequent-sibling combinator selects all elements that are next siblings of a specified element.

```
div ~ p {
  background-color: yellow;
}
```

### CSS Pseudo-classes

- A CSS pseudo-class is a keyword that can be added to a selector, to define a style for a special state of an element.

```
selector:pseudo-class-name {
  CSS properties
}
```

- The table below lists all the pseudo-class keywords in CSS:

| Pseudo-class        | Examples                                            | Example description                                                        |
| ------------------- | --------------------------------------------------- | -------------------------------------------------------------------------- |
| :active             | a:active                                            | Selects the active link                                                    |
| :any-link           | a:anylink, area:anylink                             | Selects any <a> or <area> element with an href attribute                   |
| :autofill           | input:autofill                                      | Selects any <input> element with its value autofilled by the browser       |
| :checked            | input:checked, option:checked                       | Matches any <input> or <option> element that is checked                    |
| :default            | input:default, button:default, option:default       | Selects form elements that are default in a group of related elements      |
| :defined            | :defined                                            | Selects any element that has been defined (standard or custom elements)    |
| :dir()              | :dir(ltr), :dir(rtl)                                | Selects any element with the specified text direction                      |
| :disabled           | :disabled, input:disabled, option:disabled          | Selects any element that is disabled. Most used for form elements          |
| :empty              | div:empty                                           | Selects any element that has no children (including text nodes)            |
| :enabled            | :enabled, input:enabled                             | Selects any element that is enabled. Most used for form elements           |
| :first              | @page :first                                        | Represents the first page of a printed document (used with the @page rule) |
| :first-child        | p:first-child, li:first-child                       | Selects the element that is the first child of its parent                  |
| :first-of-type      | p:first-of-type, li:first-of-type                   | Selects the first element of its type among siblings                       |
| :focus              | input:focus, select:focus                           | Selects the element that gets focus. Most used for form elements           |
| :focus-visible      | button:focus-visible                                | Selects elements when keyboard is used to focus (not mouse)                |
| :focus-within       | form:focus-within, label:focus-within               | Matches an element if itself or descendants get focus                      |
| :fullscreen         | :fullscreen                                         | Selects any element in full-screen mode                                    |
| :has()              | h2:has(+p)                                          | Selects h2 elements immediately followed by a p element                    |
| :hover              | a:hover, p:hover                                    | Selects element on mouse over                                              |
| :in-range           | input:in-range                                      | Select any <input> element with a value within the specified range         |
| :indeterminate      | input:indeterminate                                 | Selects form elements in an indeterminate state                            |
| :invalid            | input:invalid, fieldset:invalid                     | Selects invalid form elements                                              |
| :is()               | :is(ul, ol)                                         | Selects all <ul> and <ol> elements                                         |
| :lang()             | p:lang(it)                                          | Selects elements with a specific language                                  |
| :last-child         | li:last-child                                       | Selects any element that is the last child of its parent                   |
| :last-of-type       | p:last-of-type                                      | Selects the last element of its type among siblings                        |
| :left               | @page :left                                         | Represents all left-hand pages of a printed document                       |
| :link               | a:link                                              | Selects any unvisited link                                                 |
| :modal              | :modal                                              | Selects the element in a modal state                                       |
| :not()              | :not(p)                                             | Selects any element that is not a <p> element                              |
| :nth-child()        | p:nth-child(2)                                      | Selects any element that is the nth child of its parent                    |
| :nth-last-child()   | p:nth-last-child(2)                                 | Selects any element counting from the end                                  |
| :nth-last-of-type() | p:nth-last-of-type(2)                               | Selects nth element of its type counting from the end                      |
| :nth-of-type()      | p:nth-of-type(2)                                    | Selects nth element of its type among siblings                             |
| :only-child         | p:only-child                                        | Selects element that is the only child of its parent                       |
| :only-of-type       | p:only-of-type                                      | Selects element that is the only one of its type among siblings            |
| :optional           | input:optional, select:optional, textarea:optional  | Selects elements without a "required" attribute                            |
| :out-of-range       | input:out-of-range                                  | Selects element with value outside range                                   |
| :placeholder-shown  | input:placeholder-shown, textarea:placeholder-shown | Selects elements showing placeholder text                                  |
| :popover-open       | :popover-open                                       | Selects elements in a showing popover state                                |
| :read-only          | input:read-only                                     | Selects input elements with the "readonly" attribute                       |
| :read-write         | input:read-write                                    | Selects editable input elements                                            |
| :required           | input:required                                      | Selects input elements with the "required" attribute                       |
| :right              | @page :right                                        | Represents all right-hand pages of a printed document                      |
| :root               | :root                                               | Selects the document's root element                                        |
| :scope              | :scope                                              | Selects elements that are reference points for selectors                   |
| :state()            | :state()                                            | Selects custom elements with a specified custom state                      |
| :target             | :target                                             | Selects the current active target element                                  |
| :user-invalid       | :user-invalid                                       | Selects form elements with invalid value after user interaction            |
| :user-valid         | :user-valid                                         | Selects form elements with valid value after user interaction              |
| :valid              | input:valid                                         | Selects input elements with valid value                                    |
| :visited            | a:visited, area:visited                             | Selects all visited links                                                  |
| :where()            | :where(ol, ul)                                      | Selects all <ul> and <ol> elements                                         |

### CSS Pseudo-elements

- A CSS pseudo-element is a keyword that can be added to a selector, to style a specific part of an element.

```
selector::pseudo-element-name {
  CSS properties
}
```

- Example

```
h2::before {
  content: "TOP";
  background-color: #ffe70e;
  color: #444;
  font-size: 16px;
  font-weight: bold;
  display: inline-block;
  padding: 5px 10px;
  position: absolute;
  top: -10px;
  right: -25px;
}
```

- The table below shows the different pseudo-elements in CSS:

| Pseudo-element               | Example                                   | Example description                                                                                          |
| ---------------------------- | ----------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| ::after                      | p::after, div::after                      | Inserts something after the content of the specified element                                                 |
| ::backdrop                   | dialog::backdrop                          | Styles the viewbox behind a dialog box or popover element                                                    |
| ::before                     | p::before, div::before                    | Inserts something before the content of the specified element                                                |
| ::file-selector-button       | ::file-selector-button                    | Selects any button of type <input type="file">                                                               |
| ::first-letter               | p::first-letter                           | Selects the first letter of every <p> element                                                                |
| ::first-line                 | p::first-line                             | Selects the first line of every <p> element                                                                  |
| ::grammar-error              | ::grammar-error                           | Styles text flagged as grammatically incorrect by the browser                                                |
| ::highlight()                | ::highlight(custom-name)                  | Selects a custom highlight                                                                                   |
| ::marker                     | ::marker                                  | Selects the markers of list items                                                                            |
| ::placeholder                | input::placeholder, textarea::placeholder | Styles the placeholder text of <input> or <textarea> elements                                                |
| ::selection                  | ::selection                               | Styles the user-selected text                                                                                |
| ::spelling-error             | ::spelling-error                          | Styles text flagged as incorrectly spelled by the browser                                                    |
| ::view-transition            | ::view-transition                         | Represents the root of the view transitions overlay, containing all view transitions on the page             |
| ::view-transition-group      | ::view-transition-group                   | Represents a single view transition snapshot group                                                           |
| ::view-transition-image-pair | ::view-transition-image-pair              | Represents a container for a view transition's "old" and "new" view states - before and after the transition |
| ::view-transition-new        | ::view-transition-new                     | Represents the "new" view state of a view transition                                                         |
| ::view-transition-old        | ::view-transition-old                     | Represents the "old" view state of a view transition                                                         |

### CSS Attribute Selectors

- CSS attribute selectors are used to select and style HTML elements with a specific attribute or attribute value, or both.

#### CSS [attribute] Selector

- The [attribute] selector is used to select elements with a specific attribute.

```
a[target] {
  background-color: yellow;
}
```

#### CSS [attribute="value"] Selector

- The [attribute="value"] selector is used to select elements with a specific attribute with an exact value.

```
a[target="_blank"] {
  background-color: yellow;
}
```

#### CSS [attribute~="value"] Selector

- The [attribute~="value"] selector is used to select elements with an attribute value containing a specific word.

```
[title~="flower"] {
  border: 5px solid yellow;
}
```

#### CSS [attribute|="value"] Selector

- The [attribute|="value"] selector is used to select elements with the specific attribute, whose value can be exactly the specific value, or start with the specific value followed by a hyphen (-).

```
[class|="top"] {
  background: yellow;
}
```

#### CSS [attribute^="value"] Selector

- The [attribute^="value"] selector is used to select elements with the specific attribute, whose value starts with a specific value.

```
[class^="top"] {
  background: yellow;
}
```

#### CSS [attribute$="value"] Selector

- The [attribute$="value"] selector is used to select elements whose attribute value ends with a specific value.

```
[class$="test"] {
  background: yellow;
}
```

#### CSS [attribute*="value"] Selector

- The [attribute*="value"] selector is used to select elements whose attribute value contains a specific value.

```
[class*="te"] {
  background: yellow;
}
```

## DEFINING COLORS IN CSS

### RGB / RGBA NOTATION

```
rgb(0, 255, 255)
```

### HEXADECIMAL NOTATION

```
#00ffff
```

## CONFLICTING SELECTORS AND DECLARATIONS

```
Declarations marked !important
|
v
Inline style (style attribute in HTML)
|
v
ID (#) selector -> Multiple -> Last selector in code applies
|
v
Class (.) -> Multiple -> Last selector in code applies
|
v
Pseudo-class (:) selector -> Multiple -> Last selector in code applies
|
v
Element selector (p, div, li, etc.) -> Multiple -> Last selector in code applies
|
v
Universal selector (\*)
```

### Important CSS rule

```
selector {
  property: value !important;
}
```

## CSS inheritance

### Basic Concept

- Inheritance is a mechanism in CSS where some properties are passed from a parent element to its child elements.

- Example: A `<strong>` inside a `<p>` inherits text-related properties like font-size, font-style, line-height from the `<p>`.

### Using Inheritance on body

- body is the parent of all elements on the page.
- Setting text-related properties (color, font-family, font-size) on body allows them to be inherited by all child elements.
- Child elements without their own declarations will use these values.
- If a child element has its own value, it overrides the inherited one.

### Inheritance on a Smaller Scale

- Inheritance can be applied to any container, not just body

### Not All Properties Are Inherited

- Mainly text-related properties are inherited: color, font-family, font-size, font-style, etc.

- Layout/box properties are not inherited: border, margin, padding, width, height.

  - Example: border-top set on body does not affect child elements.

### Universal Selector vs. body

| Selector       | Mechanism                        | When to Use                                                        |
| -------------- | -------------------------------- | ------------------------------------------------------------------ |
| body           | Inheritance                      | For properties that are inherited (text-related)                   |
| \* (universal) | Applies directly to all elements | For properties that do not inherit (border, margin, padding, etc.) |

- The universal selector (\*) has the lowest priority and can be easily overridden by other selectors.

### Key Takeaways

- Use body to declare basic text properties.

- Not all properties inherit → use universal selector if needed for non-inherited properties.

- Inherited values are easily overridden by more specific rules (higher specificity, inline style, !important).

## Types of boxes in CSS

### Block-level Boxes

- Elements are formatted visually as blocks

- Elements occupy 100% of parent element’s width,
  no matter the content

- Elements are stacked vertically by default, one
  after another

- The box-model applies as showed earlier

- Default for most elements: body, main, header,footer, section, nav, aside, div, h1-h6,p, ul, ol, li, etc..With CSS: display: block

### INLINE ELEMENTS

- Occupies only the space necessary for its content
- Causes no line-breaks after or before the element
- Box model applies in a different way: heights and
  widths do not apply
- Paddings and margins are applied only
  horizontally (left and right)
- Default for most elements: a, img, strong, em, button, etc.With CSS: display: block

### INLINE-BLOCK BOXES

- Looks like inline from the outside, behaves like blocklevel on the inside
- Occupies only content’s space
- Causes no line-breaks
- Box-model applies as showed
- With CSS: display: inline-block

## ABSOLUTE POSITIONING

### Normal Flow (default flow)

- Default positioning
- Element is “in flow”
- Elements are simply laid out according to their order in the HTML code
- `position: relative`

### ABSOLUTE POSITIONING

- Element is removed from the normal flow: “out of flow”
- No impact on surrounding elements, might overlap them
- We use top, bottom, left, or right to offset the element from its relatively positioned container
- `position: absolute`

### Example

```
/* parent container */
.container {
 position: relative;
 background-color: #f7e6c1;
}

/* child container */
el {
 position: absolute;
 top: 100px;
 left: 200px;
 background-color: #f4b33f;
}

```

## THE CSS BOX MODEL

- Content: Text, images, etc.
- Border: A line around the element, still inside of the element
- Padding: Invisible space around the content, inside of the element
- Margin: Space outside of the element, between elements
- Fill area: Area that gets filled with background color or background image
- Final element width = left border + left padding + width + right padding + right border
- Final element height = top border + top padding + height + bottom padding + bottom border

![Diagram](.static/image/lecture_0001.png)
