# Responsive Web Design Reference

- [Responsive Web Design Reference](#responsive-web-design-reference)
	- [HTML](#html)
		- [Basic layout](#basic-layout)
		- [Google fonts and fontawesome icons](#google-fonts-and-fontawesome-icons)
		- [General](#general)
		- [Identifying elements (id class)](#identifying-elements-id-class)
			- [Id](#id)
			- [Class](#class)
		- [Layout elements](#layout-elements)
			- [Heading h1](#heading-h1)
			- [Paragraph p](#paragraph-p)
			- [List ul](#list-ul)
			- [Div](#div)
			- [Span](#span)
			- [Section](#section)
			- [Article](#article)
			- [Divider hr](#divider-hr)
			- [Line break br](#line-break-br)
			- [Table](#table)
		- [Inputs](#inputs)
			- [Form](#form)
			- [Fieldset](#fieldset)
			- [Legend](#legend)
			- [Label](#label)
			- [Input](#input)
			- [Select](#select)
			- [Textarea](#textarea)
			- [Button](#button)
		- [Images, links, icons](#images-links-icons)
			- [Image](#image)
			- [Anchor](#anchor)
			- [Icon](#icon)
		- [Other topics](#other-topics)
			- [HTML formatting](#html-formatting)
	- [CSS](#css)
		- [General](#general-1)
		- [Selectors](#selectors)
		- [Psuedo selectors](#psuedo-selectors)
		- [Layout](#layout)
			- [Initial page setup](#initial-page-setup)
			- [CSS box model](#css-box-model)
			- [Box sizing](#box-sizing)
			- [Grid](#grid)
			- [Flexbox](#flexbox)
			- [Columns with column-width](#columns-with-column-width)
			- [Position, top right left bottom, z-index](#position-top-right-left-bottom-z-index)
			- [Float](#float)
			- [Display](#display)
			- [Divider](#divider)
			- [Margin](#margin)
			- [Padding](#padding)
			- [Accessibility (@media)](#accessibility-media)
			- [Overflow](#overflow)
		- [Element properties](#element-properties)
			- [Variables](#variables)
			- [Font, text, list](#font-text-list)
				- [Font](#font)
				- [Text](#text)
				- [Letters](#letters)
				- [List styles](#list-styles)
			- [Dimensions \& shapes](#dimensions--shapes)
				- [Width/height](#widthheight)
				- [Aspect ratio](#aspect-ratio)
				- [Gap](#gap)
				- [Object-fit](#object-fit)
				- [Shapes](#shapes)
			- [Borders \& backgrounds](#borders--backgrounds)
				- [Borders](#borders)
				- [Border radius](#border-radius)
				- [Box shadow](#box-shadow)
				- [Background-image](#background-image)
			- [Color](#color)
				- [Basics](#basics)
				- [Linear gradient](#linear-gradient)
				- [Repeating linear gradient](#repeating-linear-gradient)
				- [Radial gradient](#radial-gradient)
				- [Opacity:](#opacity)
			- [Other topics (filter, transform, content)](#other-topics-filter-transform-content)
				- [Filter](#filter)
				- [Transform](#transform)
				- [Content](#content)
			- [Tables](#tables)
			- [Functions (minmax, calc, repeat)](#functions-minmax-calc-repeat)
		- [User interface](#user-interface)
			- [Cursor](#cursor)
			- [scroll behaviour](#scroll-behaviour)
		- [Animation](#animation)
				- [Basic settings with @keyframes](#basic-settings-with-keyframes)
			- [Motion based animations @media rule](#motion-based-animations-media-rule)
		- [Accessibility](#accessibility)
			- [General notes](#general-notes)
			- [Screen readers](#screen-readers)
			- [Navigation key shortcuts](#navigation-key-shortcuts)
			- [HTML and CSS to reverse heading order](#html-and-css-to-reverse-heading-order)
		- [Useful formats](#useful-formats)
			- [Draw a cat eye (drawing shapes)](#draw-a-cat-eye-drawing-shapes)
			- [Quotation format](#quotation-format)
		- [Design theory](#design-theory)
			- [Colours](#colours)


## HTML

### Basic layout

The basic layout of an html document includes several key tags which provide information about the document and provide the structure for the page. The basic order is:

- !DOCTYPE: declares the document as html
- html: starts html and specify language
- head `<head></head>` - contains the title, meta information and link information
	- Title contains the page title `<title>page title</title>`
		- This determines what is shown in the title bar
		- Also determines what is shown when hovering on a browser tab
	- Meta declare key characteristics for the page
		- These are self closing `<meta... >`
		- Multiple meta elements can exist for a page 
	- Link declares external information utilised by the html
		- These are self closing `<link... >`
		- Multiple link elements can exist for a page
		- Examples include CSS stylesheets and google fonts
- body `<body></body>`
	- header `<header></header>`
		- In general this section is used to Introduce the page & provide a menu
		- The main navigation menu should be placed inside `<nav></nav>`
	- Main `<main></main>`
		- In general contains the core content of the page
	- Footer `<footer></footer>`
		- May include information such as author and address
		- For example may include address with `<address></address>`

```html
<!DOCTYPE html>
<html lang="en"></html>
<head>
	<title>Example page title</title>
	<meta name="description" content="example description text" />
	<meta charset="UTF-8" />
	<meta name="viewport" content="width=device-width, initial-scale=1.0" />
	<link href="styles.css" rel="stylesheet" />
</head>
<body>
<header></header>
<main></main>
<footer></footer>
</body>
```

### Google fonts and fontawesome icons

During the exercises additional links were added to the html head to access additional fonts from google fonts and icons from fontawesome. Detailed instructions are available at:

- [Get started with google fonts](https://developers.google.com/fonts/docs/getting_started)
- [fontawesome](https://fontawesome.com/)

```html
<head>
	<!-- example to get Open Sans font family from google -->
	<link href="https//fonts.googleapis.com/css?family=Open+Sans:400,700,800" rel="stylesheet"/>

	<!-- register at fontawesome to get a personalised url -->
	<link href="url from fontawesome" rel="stylesheet"/>
</head>
```

### General

- In general 2 spaces are used for html code indentation
- Comments are placed using the following syntax:  `<!-- comment here -->`
- All html elements have borders, but the border property is normally set to none by default
- Basic styling can be done directly in CSS with the <style></style> tags

### Identifying elements (id class)

#### Id

In general id is used to identify specific html elements. In CSS a hashtag is used to refer to an id e.g. `#exampleID`

```html
<input type="radio" id="exampleID">
```

#### Class

In general class is used to identify html elements. One class can be applied to many elements. In CSS a full stop is used to refer to a class e.g. `.exampleClass`

```html
<div class="exampleClass1"></div>
<!-- More than one class can be used separated by a space -->
<div class="exampleClass1 exampleClass2"></div>
```

### Layout elements

#### Heading h1

- Headings are defined with the `<h1>` to `<h6>` tags
- In general limit the use of `<h1>` to once per page
- These are block-level by default (use `display: inline-block;` to change)

#### Paragraph p

- Paragraph is the main element to mark text
- These are block-level by default (use `display: inline-block;` to change)

#### List ul

An unordered list starts with the `<ul>` tag. Each list item starts with the `<li>` tag. While an ordered list starts with `<ol>`

- Tips 
	- List items can have header elements and paragraph elements embedded within

```html
<ul>  
  <li>list item 1</li>  
  <li>list item 2</li>  
  <li>list item 3</li>  
</ul>
```

#### Div

Div is an element that is primarily used to provide structure and formatting to a page where other more specific elements are not available

- This is a block level container
- Often used for formatting
- For design it can group elements so that formatting can be applied to a number together
- Multiple div elements can be stacked together. To separate them out use margin-top and margin-bottom values
- CSS height width values can be used to give them size  
- CSS properties such as `background-color` can be used to add formatting
- Div can also be used to push or move other elements (see the marker cap exercise)

```html
<div class="classOne classTwo"> </div> <!-- attaching multiple classes -->
<div id="id"> </div> <!-- using id to connect items to CSS -->
```

#### Span

Span is typically used to mark text or part of a document for formatting

- This is an inline-element 
- Similar usage to div as in terms of a formatting tool, but on an inline basis

#### Section

Section is used to mark generic standalone section of a document, it should always have a heading. As it can be tricky to know whether to use a section or more specific CSS element here are some guidelines found on Mozilla:

- Section examples: A list of search results, a map element
- Each section should have a heading `<h1>` -  `<h6>` as the child of the section (note that headings are key for screen readers and SEO)
- Only use when there isn’t a more specific element.
	- A menu should be wrapped in `<nav>`
	- For standalone atomic units of content that make sense e.g. blog post, comment, newspaper article use `<article>`
	- For useful tangential information alongise main content e.g. related links, author bio use `<aside>`
	- For main contents use `<main>`
	- If you are using only for styling purposes use a `<div>` instead
- Sections without a heading may occur:
	- In web application/UI rather than traditional content structures
	- If global menu already utilises `<nav>` you could use section for an alternate menu e.g.  previous / next button bars for controlling apps

[Developers Mozilla - section](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/section)

#### Article

Article is commonly used to group multiple elements with related information. For example in the exercises an article with a class attribute is used to style all nested elements of a particular type:

- html: `<article class=”item”>` 
- css: `CSS .item p* {}`

#### Divider hr

W3 schools defines the purpose of hr to make a thematic break or shift of topic.

- This is a self closing element
- Default thickness is 1px
- For design, it's common to adjust height, border colour, background colour, thickness
- Tip: this can be used with CSS to add margin space e.g. `margin-top`

#### Line break br

The br element inserts a single line break.

#### Table

Tables can be created in CSS with a set structure of elements.

- `<thead></thead>` - is used to identify the header
- `<tr></tr>` - is used for table rows, initially for the header row
- `<td></td>` - is used for table data cell:
	- One is also added to the header to ensure correct layout data association
- `<th></th>` - is used for header cell i.e column lables 
	- Add one per column. Use `<span></span>` to add column labels
- `<tbody></tbody>` - is used to identify table data
- `<tr></tr>` - table row - add one per row of data (and total if relevant)
- `<th></th>` - row labels - add one per row with the row title
- `<td></td>` - data - add one per number of columns
- Tips:
	- Add a class to each `<td>` in a specific column to apply a format to that column
	- Grouping several tables into a `<div>` and using CSS can help screen readers understand document flow
	- Use caption `<caption></caption>` with tables to describe the table. Caption should be placed as the first child of a table

```html
<!-- to illustrate, here is a table from the exercises -->
<table>
	<caption>Assets</caption>
	<thead>
		<tr>
			<td></td>
			<th><span class="sr-only year">2019</span></th>
			<th><span class="sr-only year">2020</span></th>
			<th class="current"><span class="sr-only year">2021</span></th>
		</tr>
	</thead>
	<tbody>
	<!-- repeat following for each row, only 1 row shown -->
		<tr class="data">
			<th>Cash <span class="description">Current cash on hand.</span></th>
			<td>$25</td>
			<td>$30</td>
			<td class="current">$28</td>
		</tr>
	</tbody>
</table>
```

### Inputs

#### Form

The form element is used to create an HTML form for user input. It can contain various input elements.
Form attributes:

	- action: the url for the page that form-data is sent to
	- method: how to send form-data. =”GET”` or `“POST”` 
		- Use `GET` to append form-data into the URL as name/value pairs (data is visible)
		- Use `POST` to append form-data inside the body of the http request (data is not shown in the url)

When a form element contains a button element and the button attribute type is set to submit the button will trigger sending the nearest parent form. Form data for a button is based on it’s name and value attributes.

```html
<form action="https://freecodecamp.org/practice-project/accessibility-quiz" method="POST">
<button type="submit">Submit</Submit>
</form>
```

#### Fieldset

Fieldset is used to group various form elements. It draws a box around them. It is block level by default.

```html
<fieldset></fieldset>
```

#### Legend

 - Legend is used inside of a fieldset and defines a caption for the fieldset

```html
<legend></legend>
```

#### Label

Label associates text with an input element. These are inline by default. Add display: block to CSS to change

- Attributes: 
	- for: use to associate with input element by common id

```html
<label for="id"></label>
```

#### Input

The input element is used to get user-input. It has a wide range of types with specific formats and behaviours.

- Input can be nested in label, in this case `for="id"` is not required, but it's good practice to include
- Input is self closing
- Attributes: 
	-  id: element id
	- name: A name is required to make data accessible by submit-url defined in form action
		- Make name the same for groups of radiobox to make only one selectable
		- Use attribute to link radio buttons and make only one selectable
		- Adding name for checkboxes makes it easier for a server to process web form, especially with multiple checkboxes
	- types
		- type ="text": The default type if not specified is a text box
		- type="email": Only allows emails with a @ and a . in the domain
		- type="password": Obscures the input and warns if site does not use https
		-  type="submit": Adds a submit button where the first added is automatically set to submit nearest parent form
		- type="radio": For radiobox
		- type="checkbox": For checkbox
			- Note for checkbox value is optional, but good practice is to include, can be set to same as id
			- Use attribute "checked" to set as default checkbox
		- type="file": Collect an input file
	- value: This must be specified to identify value of submitted forms
	- placeholder="example text": Not necessarily good practice as may confuse. Suggested to use labels instead
	- required: Used to identify an input as required
	- min="" max="": Min and max can be used with numbers to specify min / max values
	- minlength=”8”: Add a minimum length requirement e.g. for a password field
	- pattern=”[a-z0-5]{8,}”: Specify allowable format for passwords e.g. in the example 8 or more lowercase letters or digits 0-5

```html
<label for="id"></label>
<input id="id" name="name" />
<label><input id="id" name="name"></label>
```

#### Select

Select is a container for a group of option elements. Think of a dropdown list. The option element acts as a label for each possible dropdown selection

- Attributes:
	- id:  in forms id is used to link input elements to labels (with label attribute 'for')
	- value: specifies the value to be sent to the server. If missing text will be sent
	- required: make the select a required entry
	- selected: define the default option to show in the select dropdown

```html
<select required>
<option value="1">option text</option>
<option value="2" selected>option text 2</option>
</select>
```

#### Textarea

Textarea provides a sinple text entry box

- Attributes: 
    - rows: define size in rows
    - cols: define size in cols
	- placeholder: specify default initial text

```html
<textarea></textarea>
```

#### Button

- In addition to submitting forms buttons can be added and used to trigger other actions. 
- Attributes
	- type="button": use this to prevent automatic form submission

```html
<button type="button">text</button>
```

### Images, links, icons

#### Image

Image is used to insert an image based on a url

- This is a self closing tag
- Width can be specified directly in HTML as well as in CSS
- Image acts as an ‘inline’ element
- Attributes:
	- alt: used to specify accessibility text (description of the picture)
	- loading=”lazy”: This can be used to tell the browser not to fetch the image resource until it is needed (when the user scrolls the image into view). Lazy loaded elements will not load until the non-lazy elements are loaded
	- path="": use with scalable vector graphics (SVG) to scale without affecting resolution
- Tips
	- Use margin-top with negative numbers in CSS to pull images closer to headings

```html
<img src="https://address.jpg" alt="accessibility text">
<img src="https://cdn.freecodecamp.org/platform/universal/fcc_meta_1920X1080-indigo.png"
alt="freecodecamp logo"
class="hero-img"
loading="lazy"
width="400">

<a href="https://link.com"><img src="https://address.jpg"></a> // img with link
```

#### Anchor

Anchor is used for links 

- Attributes:
	- href=”url-link”
	- href=”#id”: An id can be used in place of a url to link to another element on a page
	- target=”blank”: Use to open link in a new tab/page
	- rel:"noreferrer”: Use to omit referrer information from the HTTP request

```html
<a href="https://link.com">link text</a>
<a href=#student-info>INFO</a> <!-- link within a page by id -->
<p class="author-name"><a href="https://freecodecamp.org" target="_blank">By freeCodeCamp</a></p>
```

#### Icon

In the exercises icons are used, these can be sourced from fontawesome

- Get a `<link>` reference to include in the html head from [fontawesome](https://fontawesome.com/)
- Then search for icons at [fontawesome](https://fontawesome.com/) and
- Insert the provided `<i></i>` html code

```html
<!-- a few examples from the course exercises -->
<i class="fab fa-facebook-f"></i>
<i class="fab fa-twitter"></i>
<i class="fab fa-instagram"></i>
<i class="fab fa-linkedin-in"></i>
<i class="fab fa-youtube"></i>
<i class="fa fa-github" aria-hidden="true"></i>
```

### Other topics

#### HTML formatting

While the focus is on formatting with CSS the exercises include a number of examples of formatting directly in HTML

```html
<em>text</em> // emphasis
<strong>text</strong> // bold
<ul><li>text</li></ul> // unordered list
<ol><li>text</li></ol> // ordered list
<blockquote>text</blockquote> // blockquote
```

## CSS

### General

- Comments
	- To add comments in CSS: /* This is a single-line comment */
- Relative units
	- CSS supports units that are relative to something else. The following are used in the exercises
		- em: relative to size of parent
		- rem: relative to size of root element
		- vw / vh: % of the viewport width and height respectively
	- With rem note that by default, most browsers use a font size value of 16px. So, if the root element is 16px, an element with the value 1 rem will also equal 16px
- Browser defaults
	- Every browser has it's default HTML formatting
	- Examples
		- Default padding and margins
		- Heading element  typography
	- A number of CSS settings can be made at the outself to 'normalise' or 'reset' the display
- Keyword `Inherit: `: allows you to apply properties from parent items
- Keyword `!important`: can be added to properties that you want to ensure are not overwritten

### Selectors

These are used to target html and apply CSS.  The `:root` (root), and `*` (global) selectors are higher level and apply across the html document. Below that individual html elements can be selected by directly using html tags; `h1`, `header`, `main`, `nav`, `p` etc.

More control can be achieved by using **id** and **class**

- id: unique and should only be used with one element. These are denoted with hashtags `#idName`.
- class: not unique and can be used on one or more html elements. Class is denoted by full stop `.className`
- Within html id and class are added within html tags `<p id="id" class=”class”></p>`

```css
* {
	border: 1px solid black;	
}

:root { } /* root selector is the highest level in CSS */
* { } /* global selector */
element1, element2, element3 { } /* select multiple elements */
header h1 { } /* select elements based on hierarchy */
.name { } /* class selector */
#name { } /* id selector */
.className1, .className2 { } /* multiple class selector */
.gallery img { } /* select element within a class */
.className1 * {} /* all descendent selectors in a class */
nav > ul { } /* child combinator selector: target elements that match the second selector and are a direct child of the first */
.info > input, .info > label { } /* selecting two with child combinator */
element[class="className"] {} /* select specific elements with a specific class name */
element.className {} /* the above will select element where the only class is className, this will select those that include */
span[class~="sr-only"] {} /* select any <span> whose class includes sr-only */
#id span[class] { } /* target any <span> within #id that has a class */
```

### Psuedo selectors

Pseudo selectors provide additional control. These can be used to affect an item relative to an element (e.g. before), they can also be used to apply CSS to links, and also to set rules based on language. Tips:

- ::before and ::after are often used to create cosmetic content
- when using :first-letter it can shift text out of place. This can be fixed using float and margin settings e.g. Set `float: left` and `margin-right: 1rem`
- ‘:after’ can be used to add an empty elements after the last child item in a gallery or grid to force the last visible item to move from center to left

```css
p::before {} /* insert content before every <p> element */
p::after {} /* insert content after every <p> element */
p::first-letter {} /* select the first letter of every <p> element */
p:first-of-type {} /* Selects every <p> element that is the first <p> element of its parent */
p:first-child {} /* selects every <p> element that is the first child of its parent */
p:nth-of-type(2) {} /* select every <p> element that is the 2nd <p> element of it's parent */*
p:last-of-type {} /* Selects every <p> element that is the last <p> element of its parent */

.class1 p:not(.class2) {} /* select all elements (class1) that do no match a given CSS rule (class2) */

:lang {} /* different rules for different languages */

a:link {}
a:visited {}
a:hover {} /* must come after a:link */
a:active {} /* must come after a:hover */
```

### Layout

#### Initial page setup

Browsers apply some default settings to a page. The following settings remove default margin, padding, scrollbars and help to normalise the window. 

```css
body {
	margin: 0;
	padding: 0;
	width: 100%;
	height: 100vh;
	overflow: hidden;
}
```

Layout tip: Add border: 1px solid black to everything to aid with design process as you can see all your element shapes `* {border: 1px solid black;}`

#### CSS box model

- Content: an area with height and width 
Every html element is treated as a box with 4 areas:

- Padding: an area of space surrounding the content 
- Border: the outside edges of an element
- Margin:  an area of space outside the borders

#### Box sizing

Box sizing controls whether padding and borders are added on top of content width or if content is shrunk to include them.

- Browsers apply default margin and padding values to specific elements. To make sure things look correct set box-sizing to border-box
- Set for html, then use inherit with ::before, ::after to apply to all

```css
html {
box-sizing: border-box;　/* Elements include padding & borders in dimensions. */
box-sizing: content-box; 
}

*, ::before, ::after {
box-sizing: inherit
}
```

#### Grid

Grid provides the ability to define a grid-container using `display: grid;`. The number of columns and rows of the grid can be specified with `grid-template-columns` & `grid-template-rows`. Child elements can then be placed inside the grid with `grid-colum` and `grid-row`.

```css
/* set up grid */
display: grid;

/* examples of defining grid dimensions */
grid-template-columns: 200px 600px; /* 2 columns */

/* example of gap */
row-gap: 3rem;
gap: 2rem; /* sets row and column gap. With 2 values sets row, then column */

/* item placement */
align-items: center; /* align on vertical */
justify-content: center; /* align on horizontal */
place-items: center; /* align-items & justify-content at same time. If two values 1st is used for align-items */

/* properties for child-items */
grid-column: 2 / 3; /* Determines which column an element starts and ends in */
grid-auto-flow: column; /* autoplacement based on content */
grid-auto-columns: 1fr; /* overide grid-auto-flow */

/* sizing examples */
grid-template-columns: 1fr 94rem 1fr; /* 3 columns using fractions */
grid-template-columns: repeat(3, 1fr); /* 3 columns using a fracation */
grid-template-columns: minmax(2rem, 1fr) minmax(min-content, 94rem) minmax(2rem, 1fr); /* 3 columns using minmax */
grid-template-rows: repeat(3, min-content); /* rows that size based on content */
```

Terminology:

- Grid container: the element that contains or holds the grid
- Grid item: the elements that sit in the grid
- Grid line: vertical and horizontal lines that separate columns and rows
- Grid cell: a single unit of the grid
- Grid track: individual columns or rows of the grid
- Grid area: a number of grid cells

Parent properties:

- display: set to either grid (block level) or inline grid (inline level)
- grid-template-rows: define rows with space separated values representing track size
- grid-template-columns: define columns with space separated values representing track size
- column-gap: specifies size of grid lines
- row-gap: specifies size of grid lines
- gap: shorthand to specify column and row gap together
- justify-items: align grid items on the horizontal / row (start, end, center, stretch)
- align-items: align grid items on the vertical / column (stretch, start, end, center, baseline)
- place-items: sets both justify-items and align-items
- In the case where the grid is smaller than the container:
	- justify-content: align the grid within the container on horizontal / row (start, end, center, stretch, space-around, space-between, space-evenly)
	- align-content: align the grid within the container on vertical / column (start, end, center, stretch, space-around, space-between, space-evenly)
	- place-content: set both align-content and justify-content

Child properties:

- grid-column-start & grid-column-end:  refer to grid lines where item starts and ends
	- grid-column: shorthand for the above
- grid-row-start & grid-row-end: refer to grid lines where item starts and ends
	- grid-row: shorthand for the above
- justify-self: aligns an item inside a cell on horizontal / row (start, end, center, stretch)
- align-self: aligns an item inside a cell on the vertical / column (start, end, center, stretch)
- place-self: sets justify-self and align-self

Special units & sizing

- fr units: fractional units, means portion of the remaining space
- sizing: you can use all usual lengths px, rem, % etc.
- min-content: minimum size of content
- max-content: maximum size of content
- auto: a lot like fr except fr take precedence over auto
- fit-content(): uses space available, never less than min-content, never more than max-content
- minmax(): sets minimum and maximum value for length
- min()
- max()
- repeat(): allows to repeat values
- subgrid(): allows grid items to have a grid of their own

#### Flexbox

Flexbox provides the ability to define an element as a flex container. Direct children of the container are then known as flex items. The children can then be arranged in a row or column direction. Alignment and wrapping can also be controlled. Alignment options are similar to those described in grid

- To perfectly centre an item: set both justify-content and align-items to center
- When using flexbox with the `space-evenly` use empty `<div>` elements to move visible `<div>` elements around e.g. (at start and end to move middle elements closer together)

```css
display: flex;
flex-direction: row; /* stack items in a row */
flex-direction: column; /* stack items in a column */
flex-wrap: wrap; /* specify if items should wrap */
flex-flow: row wrap; /* shorthand for direction + wrap */
justify-content: center; /* options: flex-start, flex-end, space-around, space-evenly, space-between */
align-items: center; /* options: flex-start, flex-end, stretch, baseline */
align-content: space-between; /* options: space-around, stretch, center, flex-start, flex-end */
```

#### Columns with column-width

As an alternative to using grid columns can be created by specifying width.

```css
column-width: 25rem;
```

#### Position, top right left bottom, z-index

**Position**

There are a choice of position properties for elements within CSS. Depending on the proprty selected the top, right, left and bottom values can be set to move elements around.

- **Static** (default): elements are positioned according to the normal document flow. top, right, left and bottom values have no effect
- **Relative**: elements are positioned according to the normal document flow. The element can be offset relative to its normal position using top, right, left and bottom values
- **Absolute**: elements are removed from the normal document flow. No space is created in the doc layout. The position is determined by top, right, left and bottom values
- **Sticky**: elements are positioned according to the normal document flow. The element sticks to a specific position within the containing element or viewport based on the scroll position. Sticky moves the element into its own stack. To ensure the element does not get hidden by different stacks, add a `z-index` property set to `999`
- **Fixed**: fixed to the page no matter where the user scrolls

**Top, right, left, bottom**

- Specified using % or px values

**Z-Index**

- Used to define the order of overlapping HTML elements. Any element with a higher z-index will always be positioned over an element with a lower z-index

```css
position: fixed;
top: 0; // fix to the top of a container
z-index: 999;

/* center an item with CSS */
position: absolute;
right: 0;
left: 0;
top: 0;
bottom: 0;
margin: auto;
```

#### Float

Places an element on the left or right side of its container, allowing text and inline elements to wrap around it.

```css
float: left; /* 
```

#### Display

Display options:

- `inline-block` 
	- Allows for height and width, top/bottom margins/paddings are respected, does not add line break after element
	- Causes items to group up. To separate them out you give them separate classes & then assign the classes width e.g. 49 / 50% (depending on added space)
- `inline`
	- cannot set width, height, top/bottom margins/paddings not respected
- `block`
	- compared to inline-block, adds a line break after so can’t sit next to other elements

#### Divider

An easy way to create dividers is to use `<div>` elements, and assign them to a specific class with border values

```html
<div class="divider"></div>
```

```css
.divider {
bottom-border: 1px solid #888989;
margin: 2px 0;
}
```

#### Margin

The space surrounding an element.
- Top, bottom, left and right values can be set in a variety of ways.
- Add a `<p>` selector and set margins to 0 to remove default whitespace
- Setting margin to 0 will remove scrollbars (added by default by some browsers)

```css
margin: 0; /* remove all margins */
margin: auto; /* set all to auto */
margin: 10px 20px 10px 15px; /* top, right, bottom, left */
margin: 0 auto 20; /* top, left and right, bottom 20 */
margin: 0 auto; /* top and bottom, left and right */
margin-top: 20px; /* specify top, right, bottom or left */
```

#### Padding

The space between an elements content and border. Top, bottom, left and right values can be set in a variety of ways.

- Adding padding changes the size of a `<div>` element
- Padding is useful in positioning captions
- To replace a top margin with top padding remember to first set the `margin: 0;`

```css
padding: auto; /* set all to autio */
padding: 10px 0; /* top and bottom, left and right */
padding-left: 20px; /* specify top, right, bottom or left */
padding: 0.5rem calc(1.25rem +2px) 0.5rem 0; /* top, right, bottom, left */
```

#### Accessibility (@media)

The @media query can be used to conditionally apply CSS. Commonly used with viewport width by setting max-width and min-width values. This provides the ability to adjust layout/format for small screens, mobile etc.

```css
/* examples from exercises */
@media (max-width: 960px) {
	.card {
		padding: 2rem;
	}
}

@media (min-width: 500px) and (max-width: 1000px){
}

@media only screen and (max-width: 720px) {
	.image-wrapper {
		grid-template-columns: 1fr;
	}
}
```

#### Overflow

Can be used with `hidden` to stop scrollbars from appearing

```css
overflow: hidden; 
```

### Element properties

#### Variables

CSS supports variables. These should be defined in the `:root` selector. These are then available to all following selectors.

```css
/* set variable */
root: {
--building-color1: #999; /* '--' variable name ':' value */
}

/* use variable */
building-color: var(--building-color1); /* var(variableName) */
background-color: var(--building-color2, green); /* fall-back value */
```

#### Font, text, list

##### Font

Font properties that can be set include family, size, weight etc.

Each browser has some common font families available to it. Fall back fonts can be added after the first separated by commas. Fonts with open space in the name must be surrounded with quotes (“Open Sans”).

Additional fonts are available by linking to external sources such as google. [Google fonts guide](https://developers.google.com/fonts/docs/getting_started).

Font tips:

- `Font-size: 62.5%;` will set font to 10px (browser default is 16px)
- If font-size  = 62.5%, it is easy to work with rem as 2rem will equal 20px

```css
font-family: "Open Sans", sans-serif; /* fall back font follows the first after a ',' */
font-size: 16px;
font-size: **min(5vw, 1.2em);**
font-weight: 800; /* increases 'boldness' of font */
font-weight: bold;
```

```html
/* link to google to get Open Sans font */
<link href="https://fonts.googleapis.com/css?family=Open+Sans:400,700,800" rel="stylesheet">
```

##### Text

Text properties that can be set include alignment, indentation, decoration (e.g. underline). CSS also has properties for letters and list styling.

```css
text-align: center;
text-indent: -4px;
text-decoration: none; /* remove underline from anchor */
vertical-align: top;
```

##### Letters

```css
letter-spacing: 0.15px;
```

##### List styles

```css
list-style-type: none;
list-style: none;
```

#### Dimensions & shapes

##### Width/height

Width and height of elements can be set using in a fixed way using px. They can also be set relative to parent elements using %. Another options is to use vw (viewport width) and vh (viewport height)

Tip:

- Use `width: 100vw; min-width: 4rem; max-width: 4rem;` to ensure that the width is fixed, whereas setting width specifically would allow  elements to shrink to the container

```css
width: 80% /* sets to % of parent element */
**max-width: 500px; /* use e.g. 40rem for responsive */
min-width: 300px;
min-height: 2em;
width: 60vw; /* vh/vw: set height relative to viewport 1vw = 1% */
width: max(250px, 25vw); /* return largest of comma separated values */
width: unset; /* remove earlier specified rules */**
```

##### Aspect ratio

```css
aspect-ratio: 35 / 4;
```

##### Gap

Sets gaps (gutters) between rows and columns. For flex, grid and multi-column layouts. Apply the property to the container element. Row-gap and column-gap sub properties

```css
gap: 16px;
row-gap: 10px;
column-gap: 10px;
```

##### Object-fit

Maintains aspect ratio and crops images to fit in containers

```css
object-fit: cover; // 
```

##### Shapes

Shapes can be created in CSS usually by using a combination of width, height, top, right, left, border, bottom and transform properties along with pseudo :before and :after selectors.

Examples:

- Squares & rectanges: use a `<div>` with width, height and background-color
- Circles: create a square then set border-radius to 50%
- Ovals: create a rectangle then set border-readius to 50%
- Triangles:
	- The CSS method is to use a `<div>` and manipulate width, height and borders to create a triangle
	- This works based on border edges being at a 45 degree angle
	- Watchout: text will not flow around the ‘shape’, but the `<div>` which remains square despite the visual changes
	- Method
		- First set the width and height of the `<div>` to 0;
		- Next make the borders thickers and set one border edge to a colour and the others to transparant

#### Borders & backgrounds

##### Borders

Elements border properties include width, color, style.   Black is used by default, however if setting borders it is best practice to set black explicitly.
Tips:

- Use border-bottom with elements such as `<div>`, `<fieldset>` to create a horizontal divider
- Temporary set borders globally `*` during design to visualise all elements 

```css
border: 0; /* remove all borders */

border-left-width: 10px; /* specify border on one side */
border-left-style: solid; /* or dashed or dotted or double */

border-left-color: black;
border-color: #000000 #0000ff #00ff00 #ff0000 /* set colours individually */

border-bottom: 4px solid #fdb347; /* quick format width, style and colour */
```

##### Border radius

Border radius can be used to round corners of elements such as `div`

- Tip: use a high radius e.g. 46% on a `<div>` with width of 250px and height of 100px to create an oval

```css
border-radius: 9px; /* set all corners based on px */
border-radius: 46%; /* set all corners based on % */
border-top-left-radius: 90px; /* set one corner only */
border-radius: 40% 50%; /* set top & bottom vs. left & right */
border-radius: 190% 150px 0 0; /* set 4 corners individually */
```

##### Box shadow

Add a shadow to an element. The height and width of the shadow is based on the height and width of the element it's applied to, but optional spreadRadius can be used to adjust this.

Syntax: `box-shadow: offsetX offsetY blurRadius spreadRadius color;` where:

- `offsetX` and `offsetY` accept number values in px and other CSS units
	- Positive offsetX moves shadow right, negative left, 
	- Positive offsetY moves shadow up, negative down
- `blurRadius` is optional and specified in px (or other units?) like offsetY and offsetY
- `spreadRadius` is optional
- For zero values units do not need to be specified

```css
box-shadow: 0 0 3px 3px #efb762;
```

##### Background-image

Specify an image by url to use as the background of an element

- By default repeated so it covers the entire element
- Images are drawn on stacking context layers on top of each other. 1st layer drawn as if it is closest to user. Borders are drawn on top. Background-colour is drawn below

```css
/* from url */*
background-image: url(https//weburl.jpg);
```

#### Color

##### Basics

Color can be defined in several ways. This includes keywords: `red`, rgb values: `rgb(0,255, 0)`, hsl values:  `hsl(240, 100%, 50%` and hex values: `f7f7f7`

```css
color: f7f7f7; /* change font color */
background-color: burlywood; /* change background color by keyword */
background-color: rgb(0,255,0); /* change background color by RGB */
background-color: #00FF00; /* change background color by hex */
background-color: hsl(240,100%,50%) /* change background color by hsl */
```

##### Linear gradient

These are used to create a transition of specified colors along a line. This method creates an image element and usually paired with a background element which can take an image as a value. It requires a minumum of two colours, but can accept many.
Syntax: `linear-gradient(gradientDirection, color1 colourstop%, color2 colourstop%, color3, colourstop%)` 
where:

- GradientDirection: Specified in degrees. Defaults top to bottom
- Colour: The colour specified in rgb, hex, hsl
- Colorstop: As a % places the point where the specified color is 100% pure

```css
background: linear-gradient(90deg, 
rgb(255,0,0) 10%, 
rbg(0,255,0) 30%, 
rgb(0,0,255 90%)
);

/* example from cityskylines */
background: linear-gradient(
orange,
var(--building-color1) 80%,
var(--window-color1)
);

/* to make gradient change a solid line repeat % for 2 colors */
background: linear-gradient(
var(--building-color2) 0%,
var(--building-color2) 6%,
var(--window-color2) 6%,
var(--window-color2) 9%,
)
```

##### Repeating linear gradient

A repeating linear gradient causes the specified gradient to repeat until reaching the end of the element. This can be used to create a stripe effect. 
 
```css
/* examples from cityskylines */
background: repeating-linear-gradient(
var(--building-color2),
var(--building-color2) 6%,
var(--window-color2) 6%,
var(--window-color2) 9%
);

background:
repeating-linear-gradient(
90deg,
var(--building-color4),
var(--building-color4) 10%,
transparent 10%,
transparent 15%
);
```

##### Radial gradient

These are defined at their centre and require at least two color stops.
Syntax: background-image: radial-gradient(_shape size_ at _position, start-color, ..., last-color_);

- The shape parameter defines the shape: circle or elipse
- The size parameter defines size: closest side, farthest side, closest corner, farthest corner

```css
/* sun example from cityskylines */
background: radial-gradient(
circle closest-corner at 15% 15%,
#ffcf33 0%,
#ffcf33 20%,
#ffff66 21%,
#bbeeff 100%
);
```

##### Opacity:

A value for opacity can be added to color properties. The value of 100% or 1.0 represents opaque as in a solid wall. At 0% it represents completely transparant. With the `rgb()` color property opacity can be added by using `rgba()` and specifying a value between 0 and 1.

```css
background-color: rgba(255,255,255,0.5); /* white with 50% opacity
```

#### Other topics (filter, transform, content)

##### Filter

Filter was used to create a blur effect during one of the exercises.

```css
filter: blur(2px);
```

##### Transform

Transform can be used to modify a shape, it's position and size etc. by changing layout or affecting surrounding elements. The `transform-origin` can be specified which sets the point around which a CSS transformation is applied. This takes two values representing the top and left offset.

```css
/* selection of transform examples */
transform-origin: 0% 0%; /* point to transform around. top & left offsets.*/
transform: rotate(-0.6deg);
transform: rotate(130deg)scaleX(-1); /* rotate and retain scale */
transform: translate();
transform: scale();
transform: matrix;
transform: uppercase;
transform: skew(0deg, 44deg); /* two values - where to shear on x & y axis */
```

##### Content

Content can be used to set or override the content of an element.
Tip: in one of the exercises `content: "";` was used to make empty  `::before` and `::after` pseudo-selectors render to the page.

```css
content: "";
```

#### Tables

One property used in one of the exercises was `border-collapse` to allow cell borders in a table to collapse into a single border.

```css
border-collapse: collapse;
```

#### Functions (minmax, calc, repeat)

Throughout the exercises a few functions were utilised to set CSS values. These included `minmax()`, `calc()` and `repeat()`.

```css
/* minmax can be used with px, %, fr or keyword such as max-content */
grid-template-columns: minmax(2rem, 1fr) minmax(94rem, min-content), minmax(2rem,1fr); 

/* calculate can be used to perform simple calculations when setting values */
padding: 0.5rem calc(1.25rem + 2px) 0.5rem0; /* calculate values */

/* repeat can be used to easily create multiple columns */
grid-template-columns: repeat(2, 1fr); 
```

### User interface

#### Cursor

Cursor can be used to control how the mouse pointer displays. During the exercises this is commonly set to a pointer when hovering over buttons

```css
.btn:hover {
cursor: pointer;
}
```

#### scroll behaviour

This sets the behavior for a scrolling box when scrolling is triggered by the navigation. This can be set to auto (for instant scrolling) or smooth

```css
scroll-behavior: smooth;
```

### Animation 

##### Basic settings with @keyframes

The @keyframes at-rule is used to define the flow of a CSS animation. Within the @keyframes rule, you can create selectors for specific points in the animation sequence, such as 0% or 25%, or you can use `from` and `to` to define the start and end of the sequence.

```css
/* keyframes example showing a change of position */*
@keyframes wheel {
	0% {
	    top: 0;
	    left: 0;
	}
	30% {
		top: 50px;
	}
}
```

The animation settings are then set using full stop followed by the keyframe name:

```css
/* example from wheel exercise */

.wheel {
animation-name: wheel;    /* link keyframe animation to CSS object */
animation-duration: 10s;    /* Time in seconds (s) or milliseconds (ms) */
animation-iteration-count: infinite;
animation-timing-function: linear; /* `ease-in-out` start/end at a slower pace */  
}

.wheel {
animation: cabins 10s linear infinite; /* quick-format */
}
```

#### Motion based animations @media rule

Certain types of motion-based animations can cause discomfort for some users. In particular, people with vestibular disorders have sensitivity to certain motion triggers. The `@media` at-rule has a media feature called `prefers-reduced-motion` to set CSS based on the user's preferences. It can take one of the following values:

- `reduce`
- `no-preference`

```css
@media (feature: value) {
	selector {
		styles
	}
}
```

### Accessibility

#### General notes

- Use @media to ensure design works on target devices
- Follow color theory principles particularly around contrast for readability
- Take care with justify text which can present an issue on the web for readers with dyslexia

#### Screen readers

- To hide content from screen readers use `aria-hidden="true"`
- To make content visible to screen readers only put the text in a span or other element with `class=”sr-only”`. Then add standard CSS as follows:

```css
.sr-only {
position: absolute; /* take out of document flow */
width: 1px;
height: 1px;
padding: 0; /* take out of document flow */
margin: -1px; /* take out of document flow */
overflow: hidden; /* prevent overflow */
clip: rect(0, 0, 0, 0); /* define visible portions of an element */
clip-path: inset(50%); /* determine shape clip property should take */
white-space: nowrap; /* prevent overflow */
border: 0;
}
```

#### Navigation key shortcuts

Navigation accessibility can be improved by providing keyboard shortcuts. The `accesskey` attribute accepts a space-separated list of access keys

```html
<button type="submit" accesskey="s">Submit</button>
```

#### HTML and CSS to reverse heading order

For visual display vs. screen reader (from the exercises)

```html
<h1>
<span class="flex">
<span>AcmeWidgetCorp</span>
<span>Balance Sheet</span>
</span>
</h1>
```

```css
h1 .flex {
display: flex;
flex-direction: column-reverse;
gap: 1rem;
}
```

### Useful formats

#### Draw a cat eye (drawing shapes)

```html
<div class="cat-left-eye">
<div class="cat-left-inner-eye"></div>
</div>
```

```css
.cat-left-eye {
position: absolute;
top: 54px;
left: 39px;
border-radius: 60%;
transform: rotate(25deg);
width: 30px;
height: 40px;
background-color: #000;
}
.cat-left-inner-eye {
position: absolute;
top: 8px;
left: 2px;
width: 10px;
height: 20px;
transform: rotate(10deg);
background-color: #fff;
border-radius: 60%;
}
```

#### Quotation format

```css
.quote {
color: #00beef;
font-size: 2.4rem;
text-align: center;
font-family: "Raleway", sans-serif;
}
.quote:before {
content: '" ';
}
.quote:after {
content: ' "';
}
```

### Design theory

#### Colours

Key notes taken from the crayon exercise that went into details on colour theory for html and css: 

- Primary colours: In the RGB colour model primary colours are those that when combined create pure white (e.g. Red, Blue, Green)
- Color can be specified in CSS using the RGB function which accepts values, or arguments, for red, green, blue: 
	- `RGB(red, green, blue)`
	- Values are specified between 0 and 255 where 0 represents 0 of that color and 255  represents 100% of that colour
	- For example red  = `rgb(255,0,0)`
- Secondary colors occur when 2 primary colors are combiend. The CYMK color model is used for secondary colors. For example:
	- Cyan = RGB(0,255,255)
	- Yellow = RGB(255,255,0)
	- Magenta = RGB(255,0,255)
- Tertiary colours occure when one primary colour is combined with a nearby secondary colour. For example:
	- Orange = RGB(255, 127, 0) // decrease green because orange is a mix of red and yellow (where yellow is red and green)
	- Spring green = RGB(0,255,127) // decrease blue
	- Voilet = RGB(127,0,255) // decrease red
	- Chartreuse green = RGB(127, 255, 0)
	- Azure = RGB(0, 127, 255)
	- Rose = RGB(255, 0, 127)
- The **colour wheel** shows colors with similar hues near to each other, different hues further apart. For example pure red is between rose and orange
	- **Complimentary colours** are opposite each other. If combined they produce grey. Side by side they produce strong visual contrast & appear brighter
- Red (255,0,0) & Cyan (0,255,255) next to each other look very bright. This can be distracting if overused. It can make text hard to read if on a complimentary-coloured background
- Best practice is to choose one colour as dominant and use its complimentary colour as an accent.
- Colors can also be represented by hex values. Hex colour values start with # and take six characters (0-9 then A-F). Hex is a base-16 counting system. Two hex digits ff are the equivelant of 255 in base-10
	- Hex values for `rgb()` are written as red, green, blue e.g. green is `#00FF00`
- Colors can also be represented with HSL: hue, saturation, and lightness, where:
	- Hue: 0 to 360
	- Saturation 0 to 100% 
	- Lightness 0 to 100%
- Hue wheel: red at 0 degrees, green at 120 degrees, blue at 240 degrees
- Saturation: intensity from 0% (grey) to 100% (pure colour) - must use a % sign
- Lightness: brightness from 0% (complete black) to 100% (complete white), with 50% being neutral
- The contrast between the text and the background of a heading should be at least 4.5:1

[A useful article on color contrast](https://medium.muz.li/the-science-of-color-contrast-an-expert-designers-guide-33e84c41d156)
