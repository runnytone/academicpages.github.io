---
title: "Hari Design"
excerpt: "That's why you get fat.<br/><img src='/portfolio/images/art4.jpg'>"
collection: portfolio
---

```{r, include=FALSE}
library(dygraphs)
```

You can customize the display of axes using the `dyOptions` function (for global options) and `dyAxis` function (for per-axis options). Here's an example that uses both:

```{r}
dygraph(nhtemp, main = "New Haven Temperatures") %>%
  dyAxis("y", label = "Temp (F)", valueRange = c(40, 60)) %>%
  dyOptions(axisLineWidth = 1.5, fillGraph = TRUE, drawGrid = FALSE)
```