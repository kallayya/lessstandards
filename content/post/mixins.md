+++
title = "Mixins"
date = "2017-09-08"
sidemenu = "true"
+++
<div class="content-section">
	<p class="custom-heading">What is this?</p>
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
	
		<p class="custom-heading">Parametric Mixins</p>	
		<p>Parametric mixins use one or more parameters that extend the functionality of LESS by taking arguments and its properties to customize the mixins output when mixed into another block.</p>
<pre>
<code>
.Rounded-corners (@radius: 5px 10px 8px 2px) {
  -webkit-border-radius: @radius;
  -moz-border-radius: @radius;
  border-radius: @radius;
}

.header {
  .Rounded-corners;
}
.footer {
  .Rounded-corners(10px 25px 35px 0px);
}
</code>
</pre>

		<div class="info">Best practice: You probably noticed that we have used a capitalized letter for the mixin name. Well since CSS class selectors also use the symbol, there is no way to differentiate it from a Less mixin name. That's why we always use capitalized letters. That also mimics Object-Oriented Programming, which uses capitalized letters for classes.</div>
		<ul>
		<li>For mixins grouping use the double underscore “__” prefix.</li>
		</ul>
		<h4>Value variables</h4>
		<p>General model is the following:</p>
		<highlight>@component-element__state__property__modifier</highlight>
	
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