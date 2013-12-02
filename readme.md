# Project Boilerplate

Here is the new project boilerplate. This repo is to be used for all future frontend projects and to improve how we structure our project documents and also how we structure our frontend HTML, CSS and JS.


<br><br><br>

##Front-end Guidelines

**Created by Richard McCartney & Aisling Brock**

_____

This document outlines rules and directions a developer / designer should undertake when starting a new project at Message. These rules are not set in stone but would be greatly helpful to stick close to them to help your fellow front end devs. 


## Design & project files
_____
- All projects will need a folder which is up-to-date with all the required resources. This includes fonts, images, branding documents, a completed UI document and all site designs.

- All PSD files should try and follow [Photoshop Etiquette](http://photoshopetiquette.com/) ..Be friendly to your fellow designer.

- When creating your new beautiful designs either start or do in tandum the UI Document. This gives a boilerplate for other designers to reference also means you will create a consistant designs and, by that extension, a consistant website. This UI document will also be used for the guidelines template, the first thing to develop before any other front end work.

- Design in a modular fashion, where possible. If you know you're going to use social icons in 3 or 4 places why design them twice? Each block should be able to move from one main area to another and work seamlessly. This will obviously extend to your front end work meaning you will build a website a lot quicker.

## General guidelines
_____

These rules are here to make 1) your code semantic, 2) readable and 3) easy for other developers to jump into your work and be able to make any changes. 

#### Indentation 
All elements should be indented using soft tabs. Hitting tab will create the equivalent of four spaces. You should be able to set this in your chosen IDE.

Markup should be indented to make your markup easy to understand.
<br>

<font color="green">
*Correct example of markup intentation and elements*
</font>
<pre>
&lt;div class="container"&gt; 
	&lt;header class="header"&gt; 
		&lt;h1 class="logo"&gt; 
			&lt;a href="/"&gt; Logo&lt;/a&gt; 
		&lt;/h1&gt; 
		&lt;nav class="navigation" role="navigation"&gt; 
			&lt;ul&gt; 
				&lt;li&gt; 
					&lt;a href="/"&gt; Home&lt;/a&gt; 
				&lt;/li&gt; 
				&lt;li&gt; 
					&lt;a href="/work"&gt; Work&lt;/a&gt; 
				&lt;/li&gt; 
				&lt;li&gt; 
					&lt;a href="/about"&gt; About&lt;/a&gt; 
				&lt;/li&gt; 
				&lt;li&gt; 
					&lt;a href="/contact"&gt; Contact&lt;/a&gt; 
				&lt;/li&gt; 
			&lt;/ul&gt; 
		&lt;/nav&gt; 
	&lt;/header&gt; 
&lt;/div&gt;  
</pre>
<font color="red">
*Incorrect example of markup intentation and elements*
</font>
<pre>
&lt;div class="container"&gt;
&lt;div class="header"&gt;
		
	&lt;header&gt;
		&lt;div class="logo"&gt;
		&lt;h1&gt;&lt;a href="/"&gt;Logo&lt;/a&gt;&lt;/h1&gt;
		&lt;/div&gt;	
	&lt;/header&gt;
	

	&lt;nav id="main-site-navigation"&gt;
			&lt;ul&gt;
			&lt;li&gt;&lt;a href="/"&gt;Home&lt;/a&gt;&lt;/li&gt;&lt;li&gt;&lt;a href="/work"&gt;Work&lt;/a&gt;&lt;/li&gt;&lt;li&gt;&lt;a href="/about"&gt;About&lt;/a&gt;&lt;/li&gt;&lt;li&gt;&lt;a href="/contact"&gt;Contact&lt;/a&gt;&lt;/li&gt;
		&lt;/ul&gt;
	&lt;/nav&gt;
&lt;/div&gt;
&lt;/div&gt;  
</pre>

#### Readability vs Compression
We will always prefer readable markup and CSS over file saving. Use of whitespace or ASCII art to break up documents is okay, when appropriate. We will use server-side compression to automatically minify or gzip any client-side files like CSS and JS.

#### 320 and up
All mobile sites designed should start from 320px and up. We follow the [320 and up](http://stuffandnonsense.co.uk/projects/320andup/) mantra.
## Markup
_____

##### HTML5 

All sites we develop are to use HTML5 and CSS3 standards. For backward compatability we are to use [HTML5 Shiv](https://code.google.com/p/html5shiv/) and cover all HTML5 selectors in a reset stylesheet. CSS will gracefully degrade through all browser versions.

We will test our markup against the [W3C validator](http://validator.w3.org/), to ensure that the markup is well formed. 100% valid code is not necessary, but validation certainly helps to write more maintainable sites as well as debugging code. 

##### Boilerplate 

We have a standardised way of setting up our files and naming conventions. This is modifiled for our project needs. ~~Fork the GitHub Repo~~.

##### Doctype
A proper Doctype is always needed and triggers standards mode in your browser, Quirks mode is evil and should be avoided. 
The HTML5 Doctype -
<code>
&lt;!DOCTYPE html&gt; 
</code>

##### Character encoding
Character encoding all markup should be set as UTF-8, most common and internationally friendly. This should be designated in the <code>&lt;head&gt;</code> of the document.

<font color="green">
*Setting the meta tags*
</font>
<pre>
&lt;meta http-equiv="Content-Type" content="text/html; charset=UTF-8" /&gt; 
</pre>

<font color="green">
*In HTML5*
</font>
<pre>
&lt;meta charset="UTF-8"&gt; 
</pre>

##### General markup guidelines

The following points are guidelines for structuring your HTML markup. Developers should always use markup which is semantic.

- Use actual <code>&lt;p&gt;</code> elements for paragraph delimiters as opposed to multiple <code>&lt;br/&gt;</code> tags.

- Make use of <code>&lt;dl&gt;</code> defintion lists and <code>&lt;blockquote&gt;</code> when appropriate.

- Always try to use <code>&lt;ul&gt;</code> for navigation lists in all <code>&lt;nav&gt;</code> elements.

- Use <code>&lt;label&gt;</code> fields for all input fields. The <code>for</code> attribute should be associated with itself and the input. Plus put <code>cursor:pointer;</code> on the label as well.

- Use comments where appropriate to indicate if there are specific needs for particular markup elements. 

- Tables shouldn't be used for page layout, only holding types of information.

- A logo of a site should generally be a styled <code>&lt;h1&gt;</code>.

- Try to use <code>&lt;div class="container"&gt;</code> as the main wrap around the whole site. 

- Use [microformates](http://en.wikipedia.org/wiki/Microformat) or microdata where appropriate, specifically <code>hCard</code> or <code>adr</code>.

- Use [HTML5 Outliner](http://gsnedders.html5.org/outliner/) to check the document structure is correct and the appropriate landmarks map out the document.

- Lists, text elements, tables, forms everything should never have a class which explains what it is. Example: a paragraph tag should never have a class of <code>.para</code>, <code>.paragraph</code> or <code>.text</code>.

- When creating tables make use of <code>&lt;thead&gt;</code> ,<code>&lt;tbody&gt;</code> and <code>&lt;th&gt;</code> tags.

<font color="green">
*Table markup with correct syntax*
</font>
<pre>
&lt;table summary="Example table"&gt;
	&lt;thead&gt;
		&lt;tr&gt;
			&lt;th&gt;Table header 1&lt;/th&gt;
			&lt;th&gt;Table header 2&lt;/th&gt;
		&lt;/tr&gt;
	&lt;/thead&gt;
	&lt;tbody&gt;
		&lt;tr&gt;
			&lt;td&gt;Table data 1&lt;/td&gt;
			&lt;td&gt;Table data 2&lt;/td&gt;
		&lt;/tr&gt;
	&lt;/tbody&gt;
&lt;/table&gt;
</pre>

- Always use title-case for headers and titles. Do not use all caps or all lowercase titles in markup, instead apply the CSS property <code>text-transform: uppercase/lowercase</code>.

## CSS
_____

#### General principles

- Never use <code>@import</code> to link CSS to a HTML document, always use the <code>link</code> tag. It should always be in the <code>head</code> of the document.

- Don't include inline styles in your document, either style tags or on the elements. This is evil and will be hard to track what styling has been done.
- Keep your CSS in order, if using Sublime Text, Coda, Esspresso or TextMate try and use [CSSComb](http://csscomb.com/) to keep all your CSS definitions in order and making them easier to read.

<font color="red">
*Don't use inline styling*
</font>
<pre>
&lt;p style="font-size: 12px; color: #FFFFFF"&gt;This is poor form, I say&lt;/p&gt;
</pre>

- Write selectors that are optimised for speed and readability. Avoid extensive CSS classes and chaining. For example keep your class chaining to a minimum of two plus 1 selector, if required. Writing long class selectors can get confusing.

#### CSS Formatting

At a minimum, format CSS with selectors on one line each and each styling property on its own line. Indent declarations. Please never do any sort of class nesting or indenting this makes any stylesheet hard to read.

<font color="green">
*Correct class name formatting and indenting*
</font>
<pre>
.navigation {
	float: left;
	width: 100%;
}

.navigation li {
	float: left;
	width: 100px;
	margin: 0 20px 0 0;
}
</pre>
<font color="red">
*Incorrect class name formatting and indenting*
</font>
<pre>
header.header div.container nav#navigation {
float: left;
width: 100%;
}

header.header div.container nav#navigation ul li {
float: left;
width: 100px;
margin: 0 20px 0 0;
}
</pre>

#### Classes Vs ID's
Only give elements an ID attribute if they are unique. HOWEVER, these should not be styled in CSS; we use ID's mainly for JavaScript purposes or for anchoring to sections of a document. 

Classes can also be unique but for modular purposes, we aim that all HTML and CSS could be used anywhere. If you pull a selection of HTML from one page and move it to another, the markup and styling should work as intended.

#### Naming conventions
It is preferable to always name the class or ID by the nature of **what it is** rather than **what it looks like**. For example, a button to cancel a form that will be the colour red should have the class <code>.cancel</code> rather than the class <code>.red-button</code>. Incorrectly naming elements or creating long winded names should be avoided. Example: the main navigation should have a class of <code>.navigation</code> instead of <code>.main-side-header-navigation</code>. Think before you name an element.

#### Selectors
With CSS3 we have a wide range of new selectors we can use. [Selectors list](http://www.w3schools.com/cssref/css_selectors.asp) Some are not backward compatibile; check [Can I use](http://caniuse.com/) for browser support.

#### Pseudo-Classes
These enable you to dynamically style content. Some pseudo-classes are CSS levels 1 and 2. ( <code>:visited, :hover, :first-child</code> etc). Please use for styling purposes rather than functional or content reasons. [Learn how to use pseudo-classes here](http://coding.smashingmagazine.com/2011/03/30/how-to-use-css3-pseudo-classes/).

#### Combinators & Attribute Selectors

**Combinators**

Combinators provide shortcuts for selecting that are descendant elements, a child element or a sibling. Use these when appropriate.

*Examples*

The following selector represents a p element that is child of body:
<pre>
body > p
</pre>

The following example combines descendant combinators and child combinators.
<pre>
div ol > li p
</pre>

**Attribute**

Attribute selectors find specific attribute or values. Knowledge of regular expressions helps with attribute selectors. 

*Examples*

The following attribute selector represents an h1 element that carries the title attribute, whatever its value:
<pre>
h1[title]
</pre>

In the following example, the selector represents a span element whose class attribute has exactly the value "example":

<pre>
span[class="example"]
</pre>

#### Specificity

When working with a complex stylesheet it helps to know how to calculate the value of a selector's specificity, to save you time and to make your selectors more efficient. 

Using <code>!important</code> overrides any styling regardless of how high it is. We don't see **any reason** to use this tag. If you're resorting to this there might be something wrong with your CSS. Avoid at all costs.

#### Px vs Ems

- All fonts should use EMs for font size and line height. Using [px to em calculator](http://pxtoem.com/) can help.

- Pixels should be used for fixed widths. Try to not set heights on elements; allow the content to determine height.

#### Images 

- All images should be put through [ImageOptim](http://imageoptim.com/) before being used.  This reduces the file size to improve loading speed. It removes unrequired comments or colour profiles.

- Use correct image types:
	- Graphics are **.gif**
	- Photos are **.jpg**
	- Complex graphics (often with transparency) are **.png**
- Use sprites for rollovers to save on load time.

#### Shorthand

We love short hand CSS, try to use it as much as possible. Adding a quick value to margin or padding that is already present is a lot quicker than writing out a whole new line. 

<font color="green">
*Correct use of CSS shorthand*
</font>
<pre>
.navigation {
	margin: 20px 0;
	padding: 0 15px;
	background: #FFF url(../images/image.jpg) no-repeat top left scroll;
	font: bold 1em/1.2em Georgia, 'Times New Roman', Serif;
}

.navigation li {
	list-style: square inside url(../images/list-image.png);
}
</pre>

<font color="red">
*Incorrect use of CSS shorthand*
</font>
<pre>
.container .header #main-site-navigation {
	margin-top: 20px;
	margin-bottom: 20px;
	background-color: #FFF;
	background-image: url(../images/image.jpg);
	background-repeat: no-repeat;
	margin-left: 0;
	margin-right: 0;
	line-height: 1.2em;
	padding-left: 15px;
	padding-right: 15px;
	background-position: top left;
	padding-bottom: 0;
	padding-top: 0;
	background-attachment: scroll;
	font-weight: bold;
	font-size: 1em;
	font-family: Georgia, 'Times New Roman', Serif;
}

.container .header #main-site-navigation ul li {
	list-style-type: square;
	list-style-position: inside;
	list-style-image: url(../images/list-image.png);
}
</pre>

#### Font Styling

- All fonts should be styled with the main basic.css file and should follow the designs from the UI document. 

- Links, by default, should show an underline either all the time or on hover. Hover states should also change colour. 

- Hover states should never **remove an underline**.

- Try to avoid styling underlines with <code>border-bottom</code> issues can arise with broken words. Try to stick with <code>text-decoration</code>.

#### Web Typography

We will always use <code>@font-face</code> to supply our fonts. Avoid using <code>Cufon</code> completely. All font formats must be included in a project. We do not accept converting fonts or downloading fonts illegally. 

Font formats:

- **woff:** WOFF (Web Open Font Format)

- ** ttf:** TrueType

- ** ttf, otf: **OpenType

- ** eot: **Embedded OpenType

- **svg, svgz:** SVG Font

All fonts if possible should be hosted locally; try to avoid hosted options from Google, TypeKit, MyFonts and Fonts.com. All these providers should provide a hosted version of the font files and this will improve load/request times for these assets.

Use iconfonts when appropriate, [Fontello](http://fontello.com/) and [Font Awesome](http://fontawesome.com/) are great examples of icon fonts.

Remember all font CSS should be calling in a file called fonts.css.

## JavaScript
_____

Primarily we develop all javascript plugins and needs in [jQuery](http://jquery.com/), although plain JavaScript experience can also be an advantage. For Mothership we currently use v2.0.0+ and for frontend site work we will use v1.10.2+. *The boilerplate repo will always be updated with the latest version of jQuery*.

#### General rules and practices
- All javascript files should be well documented. Over documenting a file can be very adventagous for more novice developers to the more experienced. 

- Explain what the plugin is for, any classes or elements it would affect and any pages it's used on. Adding a concise description of where it's being used will greatly help your fellow front end devs.

- When creating a new bit of functionality, small or big, it should be completely placed in its own file and named appropriately. This should make it easier to find and to understand what it is for. 

Example a plugin called <code>carousel.js</code> will be obvious what it is doing from the name and follow the guidelines. 

A different file called <code>site-rotator.js</code> would be confusing and not apt to the overall function of the script.

- No inline JavaScript, apart from calling in jQuery files from the <code>head</code>. *This obviously extends to CSS which was said earlier in the document* 

- Never leave rogue <code>console.log</code>'s in your JS. These should be used for testing and can cause issues for earlier versions of Internet Explorer.

- Don't manually minify your JS documents.

- Strive to create functions which can be generalized, take parameters, and return values. This allows for substantial code reuse and, when combined with includes or external scripts, can reduce the overhead when scripts need to change. For example, instead of hard coding a pop-window with window size, options, and url, consider creating a function which takes size, url, and options as variables.

- Name variables and functions logically: For example: <code>popUpWindowForAd</code> rather than <code>myWindow</code>.

## Testing & QA
_____

Currently, we test all modern browsers. What we support are; Chrome, FireFox, Safari, Opera and Internet Explorer.

#### How we test

Comprehensive browser testing is a must on every web project. Great effort must be made to test across all browsers during and at the end of a development. This will ensure quality and consistent UX across all browsers.

#### IE testing

Currently we use virtualised versions of Windows through Parallels. Latest versions of Internet Explorer can be found at [Modern IE](http://www.modern.ie/en-US). Unless otherwise stated, IE testing is to start from version 8 and up; we will always support and test the most latest version of IE.

#### Other browsers

Chrome, Firefox, Safari and Opera are all to be tested on OSX and on either Windows 7 / 8.

#### Mobile testing

We have a device library for mobile testing. All responsive / adapative websites we build must be tested on iOS as a standard and must follow any designs or functionality. All other platforms (Android / Windows) will be tested on the latest version and with the most popular browser for that OS.

#### QA

Frontend QA will stand on two pilars: 

- Visual perfection: Does the website you have build fully represent the design for the website?

- Code quality: Is the HTML semantic? Are all CSS classes named appropriately and modular? Do any of the JS plugins break functionality or cause any UX issues?

Thorough testing will need to be done by the individual QAing any work. Visual testing should always be carried out on the latest browsers. Older versions of IE we know will not be perfect, but the site should still visually look correct and not have any problems. If required apply fixes using an IE stylesheet for that version.
<br><br><br>
_____
*Document created 27/11/2013 by Richard McCartney. Edited by Aisling Brock. &copy; Message 2013.*