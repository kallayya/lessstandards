+++
title = "Functions and Operations"
date = "2017-09-08"
sidemenu = "true"
+++
<div class="content-section">
	<p class="custom-heading">What is this?</p>
	<p>Less allows operations and functions. Operations allow addition, subtraction, division and multiplication of property values and colors, which can be used to create complex relationships between properties. Functions map one-to-one with JavaScript code, allowing manipulation of values.</p>
<pre>
<code>
@the-border: 1px;
@base-color: #111;
@red:        #842210;

.header {
  color: @base-color * 3;
  border-left: @the-border;
  border-right: @the-border * 3;
}
.footer {
  color: @base-color + #003300;
  border-color: desaturate(@red, 10%);
}
</code>
</pre>
	<p>The above code in Less would compile to the following CSS code:</p>
<pre>
<code>
.header {
  color: #333333;
  border-left: 1px;
  border-right: 3px;
}
.footer {
  color: #114411;
  border-color: #7d2717;
}
</code>
</pre>	

</div>