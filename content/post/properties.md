+++
title = "Properties"
date = "2017-09-08"
sidemenu = "true"
+++
<div class="content-section">
	<p class="custom-heading">What is this?</p>
	<p>A CSS rule-set consists of a selector and a declaration block: The selector points to the HTML element you want to style. The declaration block contains one or more declarations separated by semicolons. Each declaration includes a CSS property name and a value, separated by a colon.</p>

	<p class="custom-sub-heading">Sorting</p>
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

		<p class="custom-sub-heading">Shorthand</p>
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

		<p class="custom-sub-heading">Floating values</p>
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

		<p class="custom-sub-heading">Hexadecimal notation</p>
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