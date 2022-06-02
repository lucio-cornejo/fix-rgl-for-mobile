# Mobile fix for the rgl widget

The [rgl](https://cran.r-project.org/web/packages/rgl/vignettes/WebGL.html)
package allows the **R** user to create WebGL graphics in the browser.

Such package is actually one the 
[htmlwidgets](https://www.htmlwidgets.org/showcase_rglwidget.html)
with the most commands already defined for dealing with
`JavaScript` and **R** integration / communication.

Therefore, a deep front-end integretion is to be expected of the
`rgl` package. Despite this, even in the `rgl`'s official documentation
website (already linkedd above) the `rgl` graphics **fail** to
work properly when the interaction occurs via a mobile phone
or tablet. 
**In mobile, the `rgl` graphics can be zoomed in and out,**
**but can not be manully rotated.**

## A solution

A working example of a `rgl` graphic in mobile
can be found [here](https://rgl-graphic-mobile-fix.netlify.app/) .

## How to use such fix for your rgl graphics

This 
[file](https://github.com/lucio-cornejo/fix-rgl-for-mobile/blob/main/rgl-mobile-fix.html) 
contains the sufficient JavaScript code for fixing the
mentioned `rgl` mobile issue. Simply insert such code in the end of the body HTML element of your page with one or more rgl graphics.

In R Markdown, that insertion can be performed via the YAML section,
as in this example:

```yaml
---
title: rgl mobile fix
output: 
  html_document:
    includes:
      after_body: "rgl-mobile-fix.html"
---
```
