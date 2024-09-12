# CSS Intro
[CSS - Setting Up Projects](https://login.codingdojo.com/m/283/8967/60792)
 HTML provides a rough layout(bones), it doesn't provide a way to efficiently change the styling. 
 Enter CSS (Cascading Style Sheets) 

 If you've been creating free floating files for assignments not is the time to use a folder for each. Each folder will house both your `.html` and `.css` files
```html
<link rel="stylesheet" href="style.css">
```
## [Selectors](https://login.codingdojo.com/m/283/8967/60793) 
How we will access html elements from our `.css` file.
HTML elements in our code can be selected via h1, a, table, button, body, classes and ids
Custom selectors are defined using 
### ids 
**What an something is**
- `id=""` in html
- `#id{}` in css
- id should be unique

**USE**
- `div#idName` => generates => `<div id='idName'></div>`
### classes 
**What something does**
- `class=""` in html
- `.class{}` in css
- use class for reusable styling

**USE**
- `h2.className` => generates => `<h2 class='className'></h2>`
- `h2.className*3` => generates => 
```html
<h2 class="className"></h2>
<h2 class="className"></h2>
<h2 class="className"></h2>
```

## Properties
Provides control of various aspects of the visual presentation of web pages, such as colors, fonts, margins, borders, backgrounds, and more.
### Syntax
CSS properties consist of two parts: 
- a property name 
- a value

separated by a colon. 
Multiple properties are separated by semicolons. For example:
```css
selector {     
	property1: value1;     
	property2: value1 value2;     
	/* Additional properties */ 
}
```
**Property Name**: 

Each CSS property has a specific name that corresponds to the aspect of an element's appearance or behavior it controls. Examples of property names include color, font-size, margin, padding, background-color, border, display, etc.

**Value**: 

The value assigned to a CSS property specifies how the property should be applied to the selected element.
Values can be chained  by separating with spaces
## Box Model
Total area: the space an element occupies and *affects*.<br>
Includes
- margin
- border
- padding
- content
## Display Properties 
**Block, Inline & Inline-Block**

**Block**: Elements that take all horizontal space of the parent container regardless of content
- forces a line break before and after the element

**Inline**: Elements that share horizontal space(FORGET INLINE)
- flow within the parent container
- does not force line breaks
- only take up as much width as necessary
- generally cannot have width, height, margin, padding, or border properties applied to them directly

**Inline-Block**: combine features of both block and inline elements
- flow within the parent container
- have block-like properties such as width, height, margin, padding, and border.
- essentially more versatile than Inline or block(though block is often necessary for page layout.)

## Cascading and Specificity: 
The term "Cascading" in CSS refers to the process by which multiple style rules are applied to an element, and the conflicts between them are resolved. The cascade operates based on the *specificity of selectors* and the *order in which they are defined*. 

***Basically more specific selectors override less specific ones, and later rules override earlier ones.***

**Inheritance**: 
Some CSS properties are inherited by child elements from their parent elements. Inheritance means that if a parent element has a specific property value, its child elements will inherit that value unless overridden by a more specific rule.

**Combining Selectors**:
h1, a, table, button, body etc type of elements
- should be used for descendant/child selector
- `.class p` selects ALL p elements inside the parent element
- `.class > span` selects only the direct descendants of parent element

**CSS**
```css
#display_example{
    border: 3px solid;
}

#display_example p{
    border: thin red solid;
    /* display: none; */
    /* display: inline; */
    display: inline-block;
}
```
### Cascading and Specificity: 
The term "Cascading" in CSS refers to the process by which multiple style rules are applied to an element, and the conflicts between them are resolved. The cascade operates based on the *specificity of selectors* and the *order in which they are defined*. 
**Basically more specific selectors override less specific ones, and later rules override earlier ones.**
#### Inheritance: 
Some CSS properties are inherited by child elements from their parent elements. Inheritance means that if a parent element has a specific property value, its child elements will inherit that value unless overridden by a more specific rule.

