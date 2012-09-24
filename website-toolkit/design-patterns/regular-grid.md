---
layout: design-pattern
title: Regular grid
status: draft
---

A mixin for creating a regular grid of elements. The mixin accepts an argument for the number of columns in the grid. All widths are expressed as percentages of the parent element.

# Dependencies

Include the following in your SCSS to pull in styles for this pattern:

    @import "mixins.scss";
    @include regular-grid(N);

Where 'N' is the number of columns the grid should have.

## Four column example

<ul class="regular-grid example-1">
  <li><p>Item 1</p></li>
  <li><p>Item 2</p></li>
  <li><p>Item 3</p></li>
  <li><p>Item 4</p></li>
  <li><p>Item 5</p></li>
  <li><p>Item 6</p></li>
  <li><p>Item 7</p></li>
  <li><p>Item 8</p></li>
</ul>

<div class="html-and-sass">
  <div>
    <h3>HTML</h3>
<pre><code>&lt;ul class="regular-grid example-1"&gt;
  &lt;li&gt;&lt;p&gt;Item 1&lt;/p&gt;&lt;/li&gt;
  &lt;li&gt;&lt;p&gt;Item 2&lt;/p&gt;&lt;/li&gt;
  &lt;li&gt;&lt;p&gt;Item 3&lt;/p&gt;&lt;/li&gt;
  &lt;li&gt;&lt;p&gt;Item 4&lt;/p&gt;&lt;/li&gt;
  &lt;li&gt;&lt;p&gt;Item 5&lt;/p&gt;&lt;/li&gt;
  &lt;li&gt;&lt;p&gt;Item 6&lt;/p&gt;&lt;/li&gt;
  &lt;li&gt;&lt;p&gt;Item 7&lt;/p&gt;&lt;/li&gt;
  &lt;li&gt;&lt;p&gt;Item 8&lt;/p&gt;&lt;/li&gt;
&lt;/ul&gt;
</code></pre>
  </div>
  <div>
    <h3>Sass</h3>
    <pre><code>.regular-grid p{
    background-color: $cool-grey;
    border: 1px solid $light-blue-grey;
    text-align: center;
    padding: 1em;
}

.example-1{
  @include regular-grid(4);
}
</code></pre>
  </div>
</div>

## Varying columns

As you can see below, you can vary the number of columns and the margin widths will be maintained. The margin width approximates to the standard GOV.UK margin when the grid is placed in a 'wide' GOV.UK page template.

<ul class="regular-grid example-4">
  <li><p>Item 1</p></li>
  <li><p>Item 2</p></li>
</ul>

<ul class="regular-grid example-1">
  <li><p>Item 1</p></li>
  <li><p>Item 2</p></li>
  <li><p>Item 3</p></li>
  <li><p>Item 4</p></li>
</ul>

<ul class="regular-grid example-2">
  <li><p>Item 1</p></li>
  <li><p>Item 2</p></li>
  <li><p>Item 3</p></li>
  <li><p>Item 4</p></li>
  <li><p>Item 5</p></li>
</ul>

<ul class="regular-grid example-3">
  <li><p>Item 1</p></li>
  <li><p>Item 2</p></li>
  <li><p>Item 3</p></li>
  <li><p>Item 4</p></li>
  <li><p>Item 5</p></li>
  <li><p>Item 6</p></li>
  <li><p>Item 7</p></li>
  <li><p>Item 8</p></li>
</ul>

# Guidance

The mixin is tag-agnostic, so the elements can be list items, divs, paragraphs etc.
Avoid applying border effects to the item elements as this will throw out the widths.
Instead, style the contents of those elements.

# When to use

* When you want to split part of the page into equal columns
* When you want a grid of equally sized elements - for example, an image gallery

* * * 

# Discussion

Once the parent element width shrinks below a certain size the layout should probably switch to a reduced number of columns rather than continue to shrink down.




