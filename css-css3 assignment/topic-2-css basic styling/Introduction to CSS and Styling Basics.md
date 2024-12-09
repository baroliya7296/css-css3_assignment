Q-1:- Explain the difference between inline, internal, and external CSS.

1. Inline CSS
Definition:- Inline CSS refers to styling directly within an HTML tag using the style attribute.
How to use:- It is applied to a specific HTML element.
Example:-
html
<p style="color: red; font-size: 18px;">This is a red colored paragraph.</p>
Characteristics:-
Suitable for quick styling of a single element but not scalable for large websites.
2. Internal CSS
Definition: Internal CSS refers to styles defined within the <style> tag in the <head> section of the HTML document.
How to use: It is placed in the <head> section and can apply to multiple elements within the page.
Example:
html
<html>
<head>
  <style>
    p {
      color: blue;
      font-size: 18px;
    }
  </style>
</head>
<body>
  <p>This is a blue colored paragraph.</p>
</body>
</html>
Characteristics:
Styles are not shared across multiple pages, so it's less efficient for large websites.
3. External CSS
Definition: External CSS is when styles are written in a separate .css file and linked to the HTML document via the <link> tag.
How to use: The CSS rules are placed in a separate file, and the file is linked to the HTML document.
Example:
CSS File (styles.css):
css
p {
  color: green;
  font-size: 18px;
}
HTML File:
html
<html>
<head>
  <link rel="stylesheet" type="text/css" href="styles.css">
</head>
<body>
  <p>This is a green colored paragraph.</p>
</body>
</html>
Characteristics:-
Can cache styles in the browser, which improves website loading speed on subsequent visits.
<hr>
Q-2:- Describe CSS selectors and list the types of selectors (e.g., element, class, id).

1. Element Selector (Type Selector)
Description: Selects HTML elements based on their tag name.
Element Selector :element name
Example:
p {
  color: red;
}
This will select all <p> elements and make text color red.

1. Class Selector
Description: Selects HTML elements that have a specific class attribute. It can apply to multiple elements with the same class.
class selector: .className
Example:
.highlight {
  background-color: yellow;
}
This will select all elements with the class highlight and give  a yellow background.

1. ID Selector
Description: Selects a unique element with a specific id attribute. The id should be unique within the page.
Id selector: #idName
Example:
#header {
  font-size: 24px;
}
This will select the element with the id of header and change its font size 24px.

1. Universal Selector
Description: Selects all elements on the page.
Universal Selector: *all element to apply effect
Example:
* {
  margin: 0;
  padding: 0;
}
This will remove all margins and padding from all elements on the page.

1. Attribute Selector
Description: Selects elements based on the presence or value of an attribute.
Attribute Selector: [attribute]
Example:
a[href] {
  color: blue;
}
This will select all elements that have an href attribute and make text color blue.

1. Pseudo-class Selector
Description: Selects elements based on their state or position, such as when a user hovers over an element or when it’s the first child in a parent.
Pseudo-class Selector:pseudo-class
Example:
a:hover {
  color: green;
}
This will change the color of a link to green when the user hovers over it.

1. Pseudo-element Selector
Description: Selects part of an element, such as the first letter or first line of text, or adds content before or after the element.
Pseudo-element Selector: ::pseudo-element
Example:
p::first-letter {
  font-size: 2em;
  color: blue;
}
This will make the first letter of each <p> element larger and blue.

1. Descendant Selector
Description: Selects elements that are nested within other elements.
Descendant Selector: ancestor descendant
Example:
div p {
  color: orange;
}
This will select all <p> elements inside a <div> and make the text orange.

1. Child Selector
Description: Selects elements that are direct children of a specified element.
Child Selector: parent > child
Example:
div > p {
  font-weight: bold;
}
This will select only <p> elements that are directly inside a <div> and make the text bold.

1.  Adjacent Sibling Selector
Description: Selects an element that is immediately preceded by a specific sibling element.
Adjacent Sibling Selector: previous + next
Example:
h1 + p {
  margin-top: 0;
}
This will select the first <p> element immediately after an  element and remove its top margin.

1.  General Sibling Selector
Description: Selects all sibling elements that follow a specific element.
General Sibling Selector: previous ~ next
Example:
h1 ~ p {
  font-style: italic;
}
This will select all <p> elements that are siblings of an element and make the text italic.

1.  Group Selector
Description: Allows you to apply the same styles to multiple selectors.
Group Selector: selector1, selector2, selector3
Example:
h1, h2, h3 {
  font-family: Arial, sans-serif;
}
This will apply the Arial font to all elements.

<hr>

Q-3:-Discuss the CSS box model and its components

1:-Content:

Description: This is the actual content of the element, such as text, images, or other media. It is the innermost part of the box.

Property: The content area width and height can be using the width and height properties in CSS.

Example:
div {
  width: 300px;
  height: 200px;
}
In this example, the div element will have a content area that is 300px wide and 200px high.

2:-Padding:

Description: Padding is the space between the content and the border. 

Property: You can control padding on all four sides (top, right, bottom, left) using the padding property.
Example:

div {
  padding: 20px;
}
in This example the div element willadd 20px of space around the content inside the div element.

3:-Border:

Description: The border surrounds the padding (if any) and content. It can have a specified width, style, and color.

Property: The border is defined using the border property. You can set individual sides (border-top, border-right, border-bottom, border-left) or a shorthand version.

Example:
div {
  border: 2px solid black;
}
in This example the div element will add a solid black border, 2px wide, around the padding and content.

4:-Margin:

Description: The margin is the out space surrounding the border. It separates the element from other elements around it. Margins do not effect the size of the element but control the spacing between elements.

Property: Similar to padding, you can control margins on all four sides of the element using the margin property.

Example:
div {
  margin: 10px;
}
This will add a 10px space outside the border, creating a gap between the div element and its neighboring elements.