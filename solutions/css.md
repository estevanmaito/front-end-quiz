### Explain the difference between ```visibility:hidden``` and ```display:none```

```visibility: hidden``` makes the element invisible, but the element still occupies space in the layout (that is, it's rendered as an empty box), whereas the latter (```display: none```) removes the element entirely from the render tree such that the element is invisible and is not part of the layout.

Read more: https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-tree-construction