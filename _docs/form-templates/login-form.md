---
permalink: /components/form-templates/login-form/
layout: styleguide
type: component
title: Sign-in form
lead: See <a href="https://standards.usa.gov/form-templates/#login-form">US Web Design Standards</a> for design and accessibility description.
---

<div class="preview">

  <form class="usa-form-large">
	<fieldset>
		<legend class="usa-drop_text">Sign in</legend>
		<span>or <a href="/path/to/register">create an account</a></span>
		<div>
			<label for="email">Email address</label>
			<span class="usa-form-hint">Your registered email address.</span>
			<input id="email" name="email" type="email">
		</div>
		<div>
			<label for="password">Password</label>
			<input id="password" name="password" type="password">
		</div>

		<p class="usa-form-note">
			<a title="Show password" href="#" class="usa-show_password" aria-controls="password" onclick="ShowPasswordEventHandler(); return false">Show password</a>
		</p>
		<button>Sign in</button>
		<p>
			<a href="/path/to/reset/password" title="Forgot password">Forgot password?</a>
		</p>
	</fieldset>
  </form>

</div>

<div class="usa-accordion-bordered usa-accordion-docs">
  <button class="usa-button-unstyled usa-accordion-button"
      aria-expanded="false" aria-controls="collapsible-0">
    PHP Usage
  </button>
  <div id="collapsible-0" aria-hidden="true" class="usa-accordion-content">
<pre><code class="language-php">// render unescaped HTML string
echo SAMUIKit\FormTemplates::signInForm($config);

// example config
$config = [
    'textInputs' => [
        [
            'label' => 'Email address',
            'type' => 'email',
            'name' => 'email',
            'hint' => 'Your registered email address.'
        ],
        [
            'label' => 'Password',
            'type' => 'password',
            'name' => 'password',
        ]
    ],
    'createPath' => '/path/to/register',
    'forgotLinks' => [
        '/path/to/reset/password' => 'Forgot password'
    ],
    'showPasswordOnClick' => 'ShowPasswordEventHandler'	
];

// render example
echo SAMUIKit\FormTemplates::signInForm($config);</code></pre>
  </div>
</div>

<div class="usa-accordion-bordered">
  <button class="usa-button-unstyled usa-accordion-button"
      aria-expanded="true" aria-controls="collapsible-0">
    Documentation
  </button>
  <div id="collapsible-0" aria-hidden="false" class="usa-accordion-content">
  	<h4 class="usa-heading">Sign-in form</h4>
  	<h5>Required keys</h5>
  	<ul>
  		<li><strong>textInputs:</strong> Array of <a href="{{ site.baseurl }}/form-controls/text-input">Text Input</a> configurations.</li>
	</ul>
  	<h5>Optional keys</h5>
  	<ul>
  		<li><strong>createPath:</strong> The URL for creating an account.</li>
  		<li><strong>forgotLinks:</strong> An array of key-value pairs, where the "key" is the URL for the link, and the "value" is the text to display for the link (without punctuation).</li>
  		<li><strong>showPasswordOnClick:</strong> The name of a JavaScript event handler method - placed within "onclick" attribute.</li>
	</ul>
  </div>
</div>
	
