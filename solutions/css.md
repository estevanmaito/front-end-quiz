### 1) What is the difference between classes and IDs in CSS?

ID selectors are more specific than class selectors, so it takes precedence on apllying styles to an element.

Read more: https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity

### 2) What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?

Resets aim to **remove** all built-in browser styling.

Normalizers aim to make all built-in browser styling **consistent** across browsers.

If you would like to implement your own styles for every element from the ground up, including tests and bug fixes, a reset is the way to go.

On the other hand, if you want to begin from a foundation, with inconsistencies across browsers *normalized*, normalizers to the rescue!

I prefer the last.

Read more: https://the-pastry-box-project.net/oli-studholme/2013-june-3

http://nicolasgallagher.com/about-normalize-css/

### 3) Describe Floats and how they work.

Float is a CSS positioning property. The element it's aplied to is taken from the normal flow of the page, though still remaining a part of the flow, contrary to absolute positioning.

Read more: https://css-tricks.com/all-about-floats/

https://developer.mozilla.org/en-US/docs/Web/CSS/float?v=control

### 4) Describe z-index and how stacking context is formed.

The ```z-index``` property controls the stacking of elements that overlap.

Stacking context is the three-dimensional conceptualization of HTML elements along an imaginary z-axis relative to the user who is assumed to be facing the viewport or the webpage.

A stacking context is formed, anywhere in the document, by any element which is either

- the root element (HTML),
- positioned (absolutely or relatively) with a ```z-index``` value other than "auto",
- a flex item with a ```z-index``` value other than "auto",that is the parent element ```display: flex|inline-flex```,
- elements with an ```opacity``` value less than 1,
- elements with a ```transform``` value other than "none",
- elements with a ```mix-blend-mode``` value other than "normal",
- elements with a ```filter``` value other than "none",
- elements with a ```perspective``` value other than "none",
- elements with ```isolation``` set to "isolate",
- position: fixed
- specifying any attribute above in ```will-change``` even if you don't specify values for these attributes directly
- elements with ```-webkit-overflow-scrolling``` set to "touch"

Read more: https://developer.mozilla.org/en-US/docs/Web/CSS/z-index?v=control

https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Positioning/Understanding_z_index/The_stacking_context

### 5) Describe BFC(Block Formatting Context) and how it works.


Read more: https://www.w3.org/TR/CSS21/visuren.html#block-formatting

https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Block_formatting_context

https://www.sitepoint.com/understanding-block-formatting-contexts-in-css/

https://yuiblog.com/blog/2010/05/19/css-101-block-formatting-contexts/


### Explain the difference between ```visibility:hidden``` and ```display:none```

```visibility: hidden``` makes the element invisible, but the element still occupies space in the layout (that is, it's rendered as an empty box), whereas the latter (```display: none```) removes the element entirely from the render tree such that the element is invisible and is not part of the layout.

Read more: https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-tree-construction