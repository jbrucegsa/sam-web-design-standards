---
permalink: /components/other/alerts/
layout: styleguide
type: component
title: Alerts
lead: See <a href="https://standards.usa.gov/alerts/">US Web Design Standards</a> for design description.
---

<div class="preview">

  <div class="usa-alert usa-alert-success">
    <div class="usa-alert-body">
      <h3 class="usa-alert-heading">Success Status</h3>
      <p class="usa-alert-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod.</p>
    </div>
  </div>

  <div class="usa-alert usa-alert-warning">
    <div class="usa-alert-body">
      <h3 class="usa-alert-heading">Warning Status</h3>
      <p class="usa-alert-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod.</p>
    </div>
  </div>

  <div class="usa-alert usa-alert-error" role="alert">
    <div class="usa-alert-body">
      <h3 class="usa-alert-heading">Error Status</h3>
      <p class="usa-alert-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod.</p>
    </div>
  </div>

  <div class="usa-alert usa-alert-info">
    <div class="usa-alert-body">
      <h3 class="usa-alert-heading">Information Status</h3>
      <p class="usa-alert-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod.</p>
    </div>
  </div>

  <div class="usa-alert usa-alert-info">
    <div class="usa-alert-body">
      <h3 class="usa-alert-heading">Information Status</h3>
      <p class="usa-alert-text">Multi line. Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui atione voluptatem sequi nesciunt. Neque porro quisquam est, qui doloremipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.</p>
    </div>
  </div>

  <div class="usa-alert usa-alert-info">
    <form>
      <button class="usa-button-dismiss"><span class="usa-sr-only">dismiss</span></button>  
    </form>      
    <div class="usa-alert-body">
      <h3 class="usa-alert-heading">Information Status</h3>
      <p class="usa-alert-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod.</p>
    </div>
  </div>  
</div>

<div class="usa-accordion-bordered usa-accordion-docs">
  <button class="usa-button-unstyled usa-accordion-button"
      aria-expanded="false" aria-controls="collapsible-0">
    PHP Usage
  </button>
  <div id="collapsible-0" aria-hidden="true" class="usa-accordion-content">
<pre><code class="language-php">// render unescaped HTML string
echo SAMUIKit\Other::alert($config);</code></pre>
  </div>
</div>

<div class="usa-accordion-bordered usa-accordion-docs">
  <button class="usa-button-unstyled usa-accordion-button"
      aria-expanded="true" aria-controls="collapsible-0">
    Documentation
  </button>
  <div id="collapsible-0" aria-hidden="false" class="usa-accordion-content">
    <h4 class="usa-heading">Alerts</h4>
  <h5>Required keys</h5>
  <ul>
    <li><strong>title:</strong> The text in bold at the beginning of the alert.</li>
    <li><strong>message:</strong> The text under the alert heading.</li>
  </ul>

  <h5>Optional keys</h5>
  <ul>
    <li><strong>type:</strong> error|warning|success|info (default is info).</li>
    <li><strong>dismissPath:</strong> When set, a form with method POST and action target of value will be created. Note: you will want to process the POST request as the view will not.</li>
    <li><strong>csrfField:</strong> To support Cross-Site Request Forgery (CSRF), you may pass a token to be applied within the dismiss alert form.</li> 
  </ul>
  </div>
</div>
