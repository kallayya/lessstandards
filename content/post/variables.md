+++
title = "Variables"
date = "2017-09-08"
sidemenu = "true"
+++
<div class="content-section">
	<p class="custom-heading">What is this?</p>
	<p>Less variables can be declared and used with the @ symbol. You give them a name and a value, and then you can refer to the name of the variable anywhere in your Less file.</p>

	<p class="custom-sub-heading">Naming</p>
	<p>
		All variable names must be lowercase.
	</p>

	<p class="custom-sub-heading">Value variables</p>
	<p>General model is the following:</p>
	<highlight>@property-name</highlight>
<pre>
	<code>
Examples:
@color-phoenix: #4D926F;

@primary__color: @color-phoenix;

@indent__base: 2rem;

@border-radius-round: 100%;
	</code> 
</pre>

		<p class="custom-sub-heading">Parameter variables</p>
		<p>Component name must meaningful. It can contain the primary, secondary, tertiary names. The base is a modifier.</p>
		<p>General model is the following:</p>
		<highlight>@component-element__state__property__modifier</highlight>
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