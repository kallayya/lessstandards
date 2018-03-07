+++
title = "@import"
date = "2017-09-08"
sidemenu = "true"
+++
<div class="content-section">
	<p class="custom-heading">What is this?</p>
	<p>The @import directive is used to import the files in the code. It spreads the LESS code over different files and allows to maintain the structure of code easily. You can put the @import statements anywhere in the code.
	For instance, you can import the file by using the @import keyword as @import "file_name.less".</p>
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
</div>