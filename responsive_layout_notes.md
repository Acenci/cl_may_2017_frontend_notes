# Responsive Layouts
Will be using basic CSS to create responsive layouts.

## Thinking in Relative Units
-We have to think in terms of ratios and not fixed units.
-Relative units, percentages (ex. Column 1 get 70% and Column 2 gets 30% and the parent takes up 80%)

## Media Queries
-Sets CSS rules when certain parameters are met by whatever device is being used.
-Most common use is `min-width` and on mobile  `orientation`.

```
@media only screen and (min-width: 768px),
       only screen and (min-width: 700px) and (orientation: landscape)
```
## Breakpoints
-A width in which the current layout no longer works, it requires a media query to change the layout.
-The size you set on your media queries

*When to create Breakpoints*
-Create a breakpoint based on the content. When does it look best?

[7 Habits of  Highly Effective Media Queries](http://bradfrost.com/blog/post/7-habits-of-highly-effective-media-queries/)

## Responsive Design Patterns
-
