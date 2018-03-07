+++
title = "LESS/CSS Best Practices"
date = "2017-09-08"
sidemenu = "true"

+++

<div class="wrapper" id="wrapper">
	<div class="content-section">
		<p>
			Creating a well-managed set of CSS codes can be a challenge.Through practice, you should be able to avoid CSS errors. So, to give you a guide on the dos and dont’s when writing CSS codes, we listed below the CSS practices to follow as well as the bad habits to avoid. So, get ready and let’s get started.
		</p>
	</div>
	<div class="content-section">
		<h2>Use CSS Reset</h2>
		<p>
			Browser inconsistencies are one of the biggest problems of front-end development nowadays. Resets essentially eliminate browser inconsistencies such as heights, font sizes, margins, headings, etc. The reset allows your layout look consistent in all browsers. The goal of a reset style sheet is to reduce browser inconsistencies by providing general styles that can be edited and extended.
		</p>
	<p>	
		One of the great examples for a reset CSS stylesheet is <a href="https://necolas.github.io/normalize.css/" target="_blank">normalize.css</a>, a modern HTML5 CSS reset. All you have to do is include it before your own style definitions in your HTML file under the Head section. Otherwise, these styles will override your own style definitions.
	</p>
	</div>
	<div class="content-section">
		<h2>Provide Style Sheet Information</h2>
		<p>
			Put a Title, Author, Tags, Description, URL  information and so on on your stylesheet. This will give the user/developer a reference person to contact whenever they need support regarding your creation.
		</p>
<pre>
	<code>
/*
Theme Name: Simple Example Website 
Description: Simple Example Scrolling Effect 
Author: Author 
Author URI: https://examplesite.com/ 
Tags: Example, Website
*/
	</code>
</pre>
	</div>	
	<div class="content-section">
		<h2>Organize Elements on the Stylesheet from Top to Bottom</h2>
		<p>
			Usually for beginners, they put the elements on the stylesheet according to what they want to put first. But this is not a good practice for CSS code structure as it will give you a hard time finding CSS code elements on the stylesheet. Ordering them from inclusive styles (such as body, H1, p, a and the likes) followed by a header to a footer will make a lot of sense.<br/>
			As an example consider the code structure below.
		</p>
<pre>
	<code>
/****** General Styles *********/
body {…}
h1, h2, h3 {..} 
p {…} 
a {…} 

/****** Header Style *********/ 
#header {…} 

/****** Navigation Style *********/ 
#nav {…} 

/****** Body Style *********/ 
#content {...} 

/****** Footer Style *********/ 
#footer {…}
	</code>
</pre>			
	</div>
	<div class="content-section">
		<h2>Use Comments to Identify a Set of CSS</h2>
		<p>
			Another best practice for CSS coding is putting a comment on each group of CSS. This will make it easy for you to look for specific groups of CSS once you got in to some CSS errors.
		</p>
<pre>
	<code>
	/*** General Styles ***/
	/*** Header Style ***/
	</code>
</pre>		
	</div>	
	<div class="content-section">
		<h2>Structure Naming Convention</h2>
		<p>
			Another best practice for CSS coding is putting a comment on each group of CSS. This will make it easy for you to look for specific groups of CSS once you got in to some CSS errors.
		</p>
		<p>
			Using proper naming conventions on IDs and classes will make a lot of sense to your work. This will help your work easier and faster in case you need to add elements or redesign a website.

			For instance, putting a class of title-red will not make sense when you change the color of the title so why not just put title instead. Always name your elements properly based on their use not on their properties such as what color or font size the element have.
		</p>
	</div>
	<div class="content-section">
		<h2>Use Hex Code instead of Name Color</h2>
		<p>
			According to a performance test, hex codes seems to be just barely faster. We recommend using hex codes rather than name colors.
		</p>
	</div>	
	<div class="content-section">
		<h2>Use CSS Vendor Prefixed</h2>
		<p>
			Each browser has its own specification when it comes to a specific style. That’s why browser prefixes are being used to make sure that the browser supports the specific features/style you want to use.
		</p>
		<p>
			Many designers and developers are having an error with this simple matter because they forgot to add vendor prefixes to target specific browsers.
		</p>
<pre>
	<code>
The CSS browser prefixes are:
Chrome: -webkit- 
Firefox: -moz- 
iOS: -webkit- 
Opera: -o- 
Safari: -webkit-
	</code>
</pre>		
	</div>
	<div class="content-section">
		<h2>Avoid Redundant CSS</h2>
		<p>
			Using styles again and again for specific elements is not a good practice. It’s very important that you clean your code and remove redundant styles. For example, if you have a paragraph tag and span tag that has the same font size and color, you might just group them using a comma.<br/>

			Take a look at the code below.
		</p>
<pre>
	<code>
BAD PRACTICE:
span {font-size: 12px; color: red;}
p {font-size: 12px; color: red;}

BEST PRACTICE:
span, p {font-size: 12px; color: red;}
	</code>
</pre>
	</div>
	<div class="content-section">
		<h2>Avoid mixing Tag Names with ID or Class Name</h2>
		<p>
			Adding tag name to an ID or Class Name is not a good practice since it would slow down the matching process unnecessarily.<br/>

			Check out the code below.
		</p>
<pre>
	<code>
BAD PRACTICE:
p#container {
	color: red;
	font-size: 8px;
}

BEST PRACTICE:
span, p {
	font-size: 12px;
	color: red;
}
	</code>
</pre>
	</div>
	<div class="content-section">
		<h2>Avoid using Underscores on ID or Class Name</h2>
		<p>
			Using underscores might give you unnecessary results on old browsers. It is highly recommended to use hyphens.<br/>

			Take a look at the example below.
		</p>
<pre>
	<code>
BAD PRACTICE:
left_col {
	margin: 0;
	padding: 0;
}

BEST PRACTICE:
left-col {
	margin: 0;
	padding: 0;
}
	</code>
</pre>
	</div>	
	<div class="content-section">
		<h2>Use Multiple Classes</h2>
		<p>
			Sometimes it's beneficial to add multiple classes to an element. Let's say that you have a <div> "box" that you want to float right, and you've already got a class .right in your CSS that floats everything to the right. You can simply add an extra class in the declaration, like so:
		</p>
<pre>
	<code>
class="box right"
	</code>
</pre>		
	</div>
	<div class="content-section">
		<h2>Understand the Difference Between Block vs. Inline Elements</h2>
		<p>
			Block elements are elements that naturally clear each line after they're declared, spanning the whole width of the available space. Inline elements take only as much space as they need, and don't force a new line after they're used.
		</p>
<pre>
	<code>
	Here are the lists of elements that are either inline or block:
	span, a, strong, em, img, br, input, abbr, acronym

	And the block elements:
	div, h1...h6, p, ul, li, table, blockquote, pre, form
	</code>
</pre>		
		<div class="well">
			
		</div>
	</div>
	<div class="content-section">
		<h2>Don’t use too many web fonts</h2>
		<p>
			Using too many web fonts is clearly bad technique, not only from a design perspective, but also from an accessibility and usability point of view. A web page that has to load more than one (maximum two) web fonts at every refresh is going to load very slowly and we know how this affects the user experience on a site.
		</p>
	</div>
	<div class="content-section">
		<h2>Don’t use too many font-size declarations</h2>
		<p>
			If your website is well-organized, then it probably has a small set of font sizes. However, many designers prefer to use a clearly visible hierarchy and do this by playing with the font sizes. Well, this would not be a problem either if developers would code it properly. Instead of using font-size 15 times, define three classes and use each one of them five times. This is known to be much faster and to improve the loading speed of your web page. To better illustrate, take a look at the code below:
		</p>
				</ul>
<pre>
	<code>
.small { font-size: 10px; }

.medium { font-size: 13px; }

.big { font-size: 16px; }
	</code>
</pre>
	</div>	
	<div class="content-section">
		<h2>Use absolute position only when you have to</h2>
		<p>
			When you’re starting out, you can easily become addicted to the use of absolute positioning. This is because it is an easy way of placing elements, however, this property should not be used excessively. Since elements with absolute position lose their normal flow, it is almost impossible to align them with other sections on the page.<br/>
			Use absolute position only when you need to, and not because it is easier.
		</p>
	</div>		
	<div class="content-section" id="lessExtension">
		<h1>LESS extension</h1>
		<p>LESS is a CSS pre-processor that enables customizable, manageable and reusable style sheet for website. LESS is a dynamic style sheet language that extends the capability of CSS. LESS is also cross browser friendly.</p>

		<p>CSS Preprocessor is a scripting language that extends CSS and gets compiled into regular CSS syntax, so that it can be read by your web browser. It provides functionalities like variables, functions, mixins and operations that allow you to build dynamic CSS.</p>

		<h2>Why LESS?</h2>
			<ul>
			<li>Let us now understand why do we use LESS.</li>
			<li>LESS supports creating cleaner, cross-browser friendly CSS faster and easier.</li>
			<li>LESS is designed in JavaScript and also created to be used in live, which compiles faster than other CSS pre-processors.</li>
			<li>LESS keeps your code in modular way which is really important by making it readable and easily changeable.</li>
			<li>Faster maintenance can be achieved by the use of LESS variables.</li>
			</ul>
		<ul>
			<li>Global variables MUST be declared first.</li>
			<li>Inclusions of LESS files with mixins and/or variables only MUST be declared after variables.</li>
			<li>Mixins MUST be declared after variables and, if applicable, included LEES files with mixins and/or
				variables, before other declarations.</li>
			<li>Nested rules MUST be indented. Each nested rule MUST be in new line, closing braces of rules MUST NOT.</li>
		</ul>
	
		<p>Please go through <a target="_blank" href="http://lesscss.org/">lesscss.org</a> for more details on installation.</p>			
	</div>

	<div class="content-section">
		<h2>LESS CODING STANDARDS</h2>
		<h2>Indentation</h2>
		<p>
			Use only spaces for indentation:
		</p>
		<ul>
			<li>Tab size: 4 spaces</li>
			<li>Indent size: 4 spaces</li>
		</ul>
<pre>
	<code>		
.nav {
    .nav-item {
        ...
    }
}
	</code>
</pre>	
	</div> 

	<div class="content-section">
		<h2>Formatting</h2>
		<h3>Braces</h3>
		<p>
			Add one space before opening braces and a line break after. Add a line break before closing braces.
		</p>
<pre>
	<code>		
Correct:
.nav {
    color: @nav__color;
}

Incorrect:
.nav{color: @nav__color;}
	</code>
</pre>	

		<h3>Selector delimiters</h3>
		<p>
			Add a line break after each selector delimiter. Do not add spaces before or after delimiters.
		</p>
<pre>
	<code>		
Correct:
.nav,
.bar {
    color: @color__base;
}

Incorrect:
.nav, .bar {
    color: @color__base;
}
	</code>
</pre>
		<h3>Quotes</h3>
		<p>
			Use single quotes.
		</p>
<pre>
	<code>		
Correct:
.nav {
    content: 'lorem ipsum';
}

Incorrect:
.nav {
    content: "lorem ipsum";
}
	</code>
</pre>

		<h3>Combinator indents</h3>
		<p>
			Add spaces before and after combinators.
		</p>
<pre>
	<code>		
Correct:
.nav + .bar {
    color: @bar__color;
}

Incorrect:
.nav+.bar {
    color: @bar__color;
}

.nav +.bar {
    color: @bar__color;
}

.nav+ .bar {
    color: @bar__color;
}
	</code>
</pre>

		<h3>Properties line break</h3>
		<p>
			Start each property declaration in a new line.
		</p>
<pre>
	<code>		
Correct:
.nav {
    background-color: @nav__background-color;
    color: @nav__color;
}

Incorrect:
.nav {
    color: @nav__color; background-color: @nav__background-color;
}
	</code>
</pre>


		<h3>Properties colon indents</h3>
		<p>
			Add space after but not before the colon that separates property names from values.
		</p>
<pre>
	<code>		
Correct:
.nav {
    color: @nav__color;
}

Incorrect:
.nav {
    color : @nav__color;
}

.bar {
    color:@bar__color;
}

.item {
    color :@item__color;
}
	</code>
</pre>

		<h3>End of file</h3>
		<p>
			Add a blank line at the end of file.
		</p>

		<h3>End of selector</h3>
		<p>
			Add a blank line after a selector.
		</p>
<pre>
	<code>		
Correct:
.nav {
    background-color: @nav__background-color;
}

.bar {
    background-color: @bar__background-color;
}

Incorrect:
.nav {
    background-color: @nav__background-color;
}
.bar {
    background-color: @bar__background-color;
}
	</code>
</pre>

		<h3>End of the property line</h3>
		<p>
			Add a semicolon after property.
		</p>
<pre>
	<code>		
Correct:
.nav {
    background-color: @nav__background-color;
}

Incorrect:
.nav {
    background-color: @nav__background-color
}
	</code>
</pre>

		<h3>!important property</h3>
		<p>
			Avoid using the !important property if possible. If it is required, add a space before the property.
		</p>
<pre>
	<code>		
Correct
.jquery-ui-calendar-item {
    background-color: @nav__background-color !important;
}

Incorrect:
.jquery-ui-calendar-item {
    background-color: @nav__background-color!important;
}
	</code>
</pre>

	</div> 

	<div class="content-section">
		<h2>Comments</h2>
		<p>
			First and second level comments must be surrounded by empty lines. First, second and third level comments should have two spaces after “//”. Inline comments should have one space after “//”.
		</p>
<pre>
	<code>
Correct
//
//  First level comment
//  _____________________________________________

.nav {
    background-color: @nav__background-color;
}

//
//  Second level comment
//  ---------------------------------------------

.nav {
    background-color: @nav__background-color;
}

//  Comment
.nav {
    //  New line comment
    background-color: @nav__background-color; // ToDo UI: todo inline comment
    color: @nav__color; // inline comment
}
	</code>
</pre>		
	</div>

	<div class="content-section">
		<h2>Selectors</h2>
		<p>
			You can use almost all CSS3 selectors: descendants, attributes, pseudo classes, structural, pseudo elements, and so on.<br/>
			Exception: Avoid the id selector.
		</p>
<pre>
	<code>
Correct:
.nav {
    ...
}

.nav + bar {
    ...
}

.nav:not(.bar) {
    ...
}

Incorrect:
#foo {
    ...
}
	</code>
</pre>		
	</div>

	<div class="content-section">
		<h2>Classes Naming</h2>
		<h3>Standard Classes</h3>
		<p>
			Class names should be lowercase, start with a letter. Words should be separated with dash ‘-‘.
		</p>
<pre>
	<code>
Correct:
.nav-bar {
    ...
}

Incorrect:
.navBar {
   ...
}

Incorrect: underscore separation
.nav_bar {
   ...
}
	</code>
</pre>		
		<h3>Size</h3>
		<p>Use class names that are as short as possible, but as long as necessary. Try to convey what class is about while being as brief as possible.</p>
<pre>
	<code>
Correct:
.nav-bar {
    ...
}

Incorrect: too long
.navigation-panel-in-footer {
   ...
}

Incorrect: too short
.nvpf {
   ...
}
	</code>
</pre>		

		<h3>Meaning</h3>
		<p>Use meaningful, specific class names that reflect the purpose of the element. Class names should not be presentational or cryptic.</p>
<pre>
	<code>
Correct: specific
.category {
    ...
}
.category-title {
    ...
}

Incorrect: cryptic
.foo-1901 {
    ...
}

Incorrect: presentational
.button-green {
   ...
}

.clear {
   ...
}
	</code>
</pre>		
	</div>

	<div class="content-section">
		<h2>Selectors naming</h2>
		<h3>Type selectors</h3>
		<p>
			Avoid qualifying class names with type selectors.Unless necessary (for example with helper classes), do not use element names in conjunction with IDs or classes.
		</p>
<pre>
	<code>
Correct:
.error {
    ...
}

Incorrect:
div.error {
   ...
}
	</code> 
</pre>	
	<p>Type selectors must be lowercase.</p>
<pre>
	<code>
Correct:
.nav > li {
    ...
}

Incorrect:
.nav > LI {
   ...
}
	</code> 
</pre>		

		<h3>Formatting</h3>
		<p>
			Write selector in one line, do not use concatenation.
		</p>
<pre>
	<code>
Correct:
.product-list-item {
    ...
}

Incorrect:
.product {
    ...
    &-list {
        ...
        &-item {
            ...
        }
    }
}
	</code>
</pre>

		<h3>Nesting</h3>
		<p>
			Avoid using more than three levels of nesting.Exceptions are pseudo elements and states.
		</p>
<pre>
	<code>
Correct:
.footer {
    ...
    .nav {
        ...
    }
    .nav-list {
        ...
        .nav-list-item {
            ...
        }
    }
}

Incorrect:
.footer {
    ...
    .nav {
        ...
        .nav-list {
            ...
            .nav-list-item {
                ...
            }
        }
    }
}
	</code>
</pre>
	</div>

	<div class="content-section">
		<h2>Properties</h2>
		<h3>Sorting</h3>
		<p>
			Sort all properties in the alphabetical order. Mixins, variables, and so on should go first.
		</p>
<pre>
	<code>
Correct:
.nav {
    background-color: @nav__background-color;
    color: @nav__color;
    text-align: center;
}

Incorrect:
.nav {
    color: @nav__color;
    text-align: center;
    background-color: @nav__background-color;
}
	</code> 
</pre>	

		<h3>Shorthand</h3>
		<p>
			CSS offers a variety of shorthand properties that should be used whenever possible, even in cases where only one value is explicitly set.
		</p>
<pre>
	<code>
Correct:
border-top: 0;
padding: 0 1em 2em;

Incorrect:
border-top-style: none;
padding-bottom: 2rem;
padding-left: 1rem;
padding-right: 1rem;
padding-top: 0;
	</code> 
</pre>	

		<h3>0 and units</h3>
		<p>
			Do not specify units “0” value.
		</p>
<pre>
	<code>
Correct:
border-width: 0;
margin: 0;

Incorrect:
border-width: 0px;
margin: 0rem;
	</code> 
</pre>

		<h3>Floating values</h3>
		<p>
			Omit leading “0”s in values, use dot instead.
		</p>
<pre>
	<code>
Correct:
margin-left: .5rem;

Incorrect:
margin-left: 0.5rem;
	</code> 
</pre>

		<h3>Hexadecimal notation</h3>
		<ul>
			<li>Use lowercase only.</li>
			<li>Use three-character hexadecimal notation where possible.</li>
			<li>Avoid using hexadecimal values for color in properties, use only variables instead.</li>
		</ul>
<pre>
	<code>
Correct:
@nav__color: #fafafa;
@nav-item__color: #f00;
color: @nav-item__color;

Incorrect:
color: #ff0000;
@nav__color: #FAFAFA;
@nav-item__color: red;
	</code> 
</pre>

	</div>

	<div class="content-section">
		<h2>Variables</h2>
		<p>Less variables can be declared and used with the @ symbol. You give them a name and a value, and then you can refer to the name of the variable anywhere in your Less file.</p>
		<h3>Naming</h3>
		<p>
			All variable names must be lowercase.
		</p>
		<h4>Value variables</h4>
		<p>General model is the following:</p>
<pre>
	<code>
@property-name
	</code> 
</pre>
<pre>
	<code>
Examples:

@primary__color: @color-phoenix;
@indent__base: 2rem;
@border-radius-round: 100%;
	</code> 
</pre>

		<h4>Parameter variables</h4>
		<p>General model is the following:</p>
<pre>
	<code>
@component-element__state__property__modifier
	</code> 
</pre>
	<p>Component name must meaningful. It can contain the primary, secondary, tertiary names. Base is a modifier.</p>
<pre>
	<code>
Examples:

@color-orange: '';

@link__hover__color: '';

@nav-element__background-color: '';

@secondary__color: '';

@side-nav__indent__s: '';

@side-nav-el__background-color: '';

@side-nav-el__active__background-color: '';

@side-nav-el__active-focus__background-color: '';

@side-nav-el__active-focus__font-size__xl: '';

@text__color__base: '';
	</code> 
</pre>	
	</div>

	<div class="content-section">
		<h2>Mixins</h2>
		<p>Mixins are something comparable to functions in other programming languages. In Less they're used to group CSS instructions. We'll use a mixin to handle the boring repetition of code.</p>
		<p>Mixins are a group of CSS properties that allow you to use properties of one class for another class and includes class name as its properties</p>
<pre>
<code>
.P1 {
   color:#fefefe;
}

.p2 {
   background : #64d9c0;
   .P1();
}

.p3 {
   background : #LESS520;
  .P1;
}
</code>
</pre>
	
		<h3>Naming</h3>
		<p>Best practice: You probably noticed that we have used a capitalized letter for the mixin name. Well since CSS class selectors also use the . symbol, there is no way to differentiate it from a Less mixin name. That's why we always use capitalized letters. That also mimics Object Oriented Programming, which uses capitalized letters for classes.</p>
		<ul>
		<li>For mixins grouping use the double underscore “__” prefix.</li>
		</ul>
		<h4>Value variables</h4>
		<p>General model is the following:</p>
<pre>
	<code>
	@component-element__state__property__modifier
	</code>
</pre>		
<pre>
	<code>
Example:
.extend__clearfix (...) {
    ...
}

.vendor-prefix__flex-direction (...) {
    ...
}
	</code> 
</pre>
	</div>

	<div class="content-section">
		<h2>@import directive</h2>
		<p>The @import directive is used to import the files in the code. It spreads the LESS code over different files and allows to maintain the structure of code easily. You can put the @import statements anywhere in the code.
		For instance, you can import the file by using @import keyword as @import "file_name.less".</p>
		<p>Always add the file extension of the imported resource.</p>
<pre>
	<code>
Correct:
@import 'source/lib/_lib.less';
@import (css) 'styles.css';

Incorrect:
@import 'source/lib/_lib';
@import (css) 'styles';

Use single quotes.
Correct:
@import 'source/lib/_lib.less';

Incorrect:
@import "source/lib/_lib.less";
	</code> 
</pre>

	<p>
		So depending on your project, you can split your files in a relevant way.
	</p>
<pre>
	<code>
Final LESS Code:
@import 'reset.less'; // CSS Reset or Normalization
@import 'variables.less'; // Variables
@import 'mixins.less'; // Mixins
@import 'style.less'; // Main Styles of the page	
	</code>
</pre>
<div class="content-section">
<h2>Looping</h2>
<p>“Loop” is a programming method which repeats (or iterates) a function. Typically, it’s used for processing a list of data. One of the advantages of writing less instead of CSS is that you can create loops instead of repeating the same code again and again. Below is an example to explain the concept of looping in less.</p>
</div>
<pre>
	<code>
LESS Code :

@iterations : 4;
.para-loop (@i) when (@i > 0 ) {
.para-@{i} {
width: ~”@{I}%”;
}
.para-loop(@i -1 );
}
.para-loop (@iterations )

Compiled into the following CSS on execution :

.para-4 {
 width: 4%;
}
.para-3 {
 width: 3%;
}
.para-2 {
 width: 2%;
}
.para-1 {
 width: 1%;
}
 </code>
</pre>
	</div>
    