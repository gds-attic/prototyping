---
layout: design-pattern
title: Form example - Contact form
status: draft
---

This example incorporates most of the basic form elements and lets you play wth different label alignments.
For a detailed breakdown of each element and how to markup and style it, see our [anatomy of a form](form-anatomy.html).

# Contact form example

Click the label alignment options in the Sass snippet below to see how they affect the layout.

<div class="pattern-example">
  <pre><code class="class-toggle" data-for="form-example-2" >.form-example-2 { @include form(<span class="option selected">top</span>|<span class="option">left</span>|<span class="option">right</span>, 7.5em, $green) }</code></pre>

  <div class="inner">
    <div id="form-example-2" class="top">
      <div class="validation-summary">
        <h1>Please check the form</h1>
        <ul>
          <li><a href="#error1">Confirm your email address</a></li>
          <li><a href="#error2">Select at least one area of interest</a></li>
        </ul>
      </div>
      <form>
        <fieldset>
          <legend>Name</legend>
          <p class="group">
            <label for="title">Title</label>
            <select id="title">
              <option value="Mr">Mr.</option>
              <option value="Mrs">Mrs.</option>
              <option value="Miss">Miss</option>
              <option value="Ms.">Ms.</option>
              <option value="Dr.">Dr.</option>
              <option value="Other">Other</option>
            </select>
          </p>
          <p class="group">
            <label for="first-name">First name <abbr title="Mandatory">*</abbr></label>
            <input id="first-name" type="text" class="name">
          </p>
          <p class="group">
            <label for="last-name">Last name <abbr title="Mandatory">*</abbr></label>
            <input id="last-name" type="text" class="name">
          </p>
        </fieldset>
        <fieldset>
          <legend>Email address</legend>
          <p class="group">
            <label for="email">Enter email <abbr title="Mandatory">*</abbr></label>
            <input id="email" type="text" class="email">
          </p>
          <p class="group validation">
            <span class="validation-message" id="error1">Confirm your email address</span>
            <label for="email-confirm">Confirm email <abbr title="Mandatory">*</abbr></label>
            <input id="email-confirm" type="text" class="email">
          </p>
        </fieldset>
        <fieldset>
          <legend>Telephone number</legend>
          <p class="group">
            <label for="telephone">Telephone</label>
            <input id="telephone" type="text" class="telephone">
            <span class="help">Include your country code</span>
          </p>
        </fieldset>
        <fieldset>
          <legend>Postal address</legend>
          <p class="group">
            <label for="street1">Street</label>
            <input id="street1" type="text" class="street">
          </p>
          <p class="group">
            <label for="street2" class="visuallyhidden">Street line two</label>
            <input id="street2" type="text" class="street">
          </p>
          <p class="group">
            <label for="town">Town/City</label>
            <input id="town" type="text" class="town">
          </p>
          <p class="group">
            <label for="postcode">Postcode</label>
            <input id="postcode" type="text" class="postcode">
          </p>
        </fieldset>
        <fieldset>
          <legend>Biography</legend>
          <p class="group">
            <label for="biography">Write a few short words about yourself</label>
            <textarea id="biography" class="big"></textarea>
          </p>
          <p class="option group">
            <label for="public"><input id="public" type="checkbox"> Make this biography public</label>
          </p>
        </fieldset>
        <fieldset>
          <legend>I am interested in</legend>
          <p class="option group validation">
            <span class="validation-message" id="error2">Select at least one area of interest</span>
            <label><input type="checkbox"> Job offers</label>
            <label><input type="checkbox"> Networking</label>
            <label><input type="checkbox"> Business opportunities</label>
          </p>
        </fieldset>  
        <fieldset>
          <legend>I prefer to be contacted by</legend>
          <ul class="option group">
            <li><label><input type="radio" name="preferred-contact" checked> Email</label></li>
            <li><label><input type="radio" name="preferred-contact"> Telephone</label></li>
            <li><label><input type="radio" name="preferred-contact"> Post</label></li>
          </ul>
        </fieldset>
        <p class="action group">
          <button class="button" type="submit">Submit form</button>
        </p>
      </form>
    </div>
  </div>
</div>

# HTML

The example above is marked up as follows:

    <div id="form-example-2">
      <div class="validation-summary">
        <h1>Please check the form</h1>
        <ul>
          <li><a href="#error1">Confirm your email address</a></li>
          <li><a href="#error2">Select at least one area of interest</a></li>
        </ul>
      </div>
      <form>
        <fieldset>
          <legend>Name</legend>
          <p class="group">
            <label for="title">Title</label>
            <select id="title">
              <option value="Mr">Mr.</option>
              <option value="Mrs">Mrs.</option>
              <option value="Miss">Miss</option>
              <option value="Ms.">Ms.</option>
              <option value="Dr.">Dr.</option>
              <option value="Other">Other</option>
            </select>
          </p>
          <p class="group">
            <label for="first-name">First name <abbr title="Mandatory">*</abbr></label>
            <input id="first-name" type="text" class="name">
          </p>
          <p class="group">
            <label for="last-name">Last name <abbr title="Mandatory">*</abbr></label>
            <input id="last-name" type="text" class="name">
          </p>
        </fieldset>
        <fieldset>
          <legend>Email address</legend>
          <p class="group">
            <label for="email">Enter email <abbr title="Mandatory">*</abbr></label>
            <input id="email" type="text" class="email">
          </p>
          <p class="group validation">
            <span class="validation-message" id="error1">Confirm your email address</span>
            <label for="email-confirm">Confirm email <abbr title="Mandatory">*</abbr></label>
            <input id="email-confirm" type="text" class="email">
          </p>
        </fieldset>
        <fieldset>
          <legend>Telephone number</legend>
          <p class="group">
            <label for="telephone">Telephone</label>
            <input id="telephone" type="text" class="telephone">
            <span class="help">Include your country code</span>
          </p>
        </fieldset>
        <fieldset>
          <legend>Postal address</legend>
          <p class="group">
            <label for="street1">Street</label>
            <input id="street1" type="text" class="street">
          </p>
          <p class="group">
            <label for="street2" class="visuallyhidden">Street line two</label>
            <input id="street2" type="text" class="street">
          </p>
          <p class="group">
            <label for="town">Town/City</label>
            <input id="town" type="text" class="town">
          </p>
          <p class="group">
            <label for="postcode">Postcode</label>
            <input id="postcode" type="text" class="postcode">
          </p>
        </fieldset>
        <fieldset>
          <legend>Biography</legend>
          <p class="group">
            <label for="biography">Write a few short words about yourself</label>
            <textarea id="biography" class="big"></textarea>
          </p>
          <p class="option group">
            <label for="public"><input id="public" type="checkbox"> Make this biography public</label>
          </p>
        </fieldset>
        <fieldset>
          <legend>I am interested in</legend>
          <p class="option group validation">
            <span class="validation-message" id="error2">Select at least one area of interest</span>
            <label><input type="checkbox"> Job offers</label>
            <label><input type="checkbox"> Networking</label>
            <label><input type="checkbox"> Business opportunities</label>
          </p>
        </fieldset>  
        <fieldset>
          <legend>I prefer to be contacted by</legend>
          <ul class="option group">
            <li><label><input type="radio" name="preferred-contact" checked> Email</label></li>
            <li><label><input type="radio" name="preferred-contact"> Telephone</label></li>
            <li><label><input type="radio" name="preferred-contact"> Post</label></li>
          </ul>
        </fieldset>
        <p class="action group">
          <button class="button" type="submit">Submit form</button>
        </p>
      </form>
    </div>

<script>
  $(function() {

    // Style toggle for pattern examples
    // Takes the text of the clicked 'option' and assigns it as
    // a class to the element named in the 'data-for' attribute
    $('.class-toggle .option').click(function(){
      $('.class-toggle .option').removeClass('selected');
      $(this).addClass('selected');
      var selectedClass = $(this).text();
      var selectedElement = "#" + $(this).parents('.class-toggle').data("for");
      $(selectedElement).removeClass().addClass(selectedClass);
      return false;
    });



  });
</script>