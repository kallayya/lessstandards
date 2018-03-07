+++
title = "Selectors"
date = "2017-09-08"
sidemenu = "true"
+++
<div class="content-section">
	<p class="custom-heading">What is this?</p>
	<p>Selectors are patterns used to select the element(s) you want to style.You can use almost all CSS3 selectors: descendants, attributes, pseudo-classes, structural, pseudo-elements, and so on.</p>
	<p>
		Exception: Avoid the id selector.
	</p>
	<p class="custom-heading">How to use it?</p>
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