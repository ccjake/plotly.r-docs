---
name: WebGL vs SVG in R
permalink: r/webgl-vs-svg/
redirect_from: r/webgl-vs-svg-line-chart/
description: How to create plots using WebGL
layout: base
thumbnail: thumbnail/webgl.jpg
language: r
display_as: basic
order: 7
output:
  html_document:
    highlight: null
    keep_md: true
    theme: null
---


# WebGL vs SVG in R

Recent versions of the R package include the `toWebGL()` function, which converts any eligible SVG graph into a WebGL plot. With WebGL, we can render way more elements in the browser.

## WebGL with 50,000 points


```r
library(plotly)
p <- ggplot(data = diamonds, aes(x = carat, y = price, color = cut)) +
  geom_point(alpha = 0.01)
fig <- ggplotly(p)
fig <- fig %>% toWebGL()

fig
```

<div id="htmlwidget-f726480497eda42e71b3" style="width:672px;height:480px;" class="plotly html-widget"></div>

## More examples

* [Compare SVG performance to WebGL](https://plot.ly/r/webgl-vs-svg/)
* [WebGL with 1 million points](https://plot.ly/r/webgl-vs-svg-million-points/)
* [WebGL for time series](https://plot.ly/r/webgl-vs-svg-time-series/)