+++
title = "Code Formatting"
date = "2017-09-08"
sidemenu = "true"
+++

<div class="content-section">
	<p class="custom-heading">Formatting</p>
		<p class="custom-sub-heading">Indentation</p>
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
    color: @nav__color;
	.nav-item {
		color: @navitem__color
	}    
}
	</code>
</pre>

	<p class="custom-sub-heading">Braces</p>
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

		<p class="custom-sub-heading">Selector delimiters</p>
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
		<p class="custom-sub-heading">Quotes</p>
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

		<p class="custom-sub-heading">Combinator indents</p>
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

		<p class="custom-sub-heading">Properties line break</p>
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


		<p class="custom-sub-heading">Properties colon indents</p>
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

		<p class="custom-sub-heading">End of file</p>
		<p>
			Add a blank line at the end of file.
		</p>

		<p class="custom-sub-heading">End of selector</p>
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

		<p class="custom-sub-heading">End of the property line</p>
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

		<p class="custom-sub-heading">!important property</p>
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