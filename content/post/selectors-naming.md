+++
title = "Selectors Naming"
date = "2017-09-08"
sidemenu = "true"
+++
<div class="content-section">
	<p class="custom-heading">What is this?</p>
	<p class="custom-sub-heading">Type selectors</p>
	<p>
		Avoid qualifying class names with type selectors.Unless necessary, do not use element names in conjunction with IDs or classes.
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

		<p class="custom-sub-heading">Formatting</p>
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

		<p class="custom-sub-heading">Nesting</p>
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