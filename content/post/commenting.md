+++
title = "Comments"
date = "2017-09-08"
sidemenu = "true"
+++
<div class="content-section">
	<p class="custom-heading">What is this?</p>
	<p>
		Comments make the code clear and understandable for the users. You can use both the block style and the inline comments in the code.<br/>
		First and second level comments must be surrounded by empty lines. First, second and third level comments should have two spaces after “//”. Inline comments should have one space after “//”.
	</p>
	<p class="custom-heading">How to use it?</p>
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