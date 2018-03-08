---
title: "Hari Design"
excerpt: "That's why you get fat.<br/><img src='/portfolio/images/art4.jpg'>"
collection: portfolio
---

That's why you get fat.
<br/><img src='/portfolio/images/art4.jpg'>


library(dygraphs)

shinyUI(fluidPage(
  
  titlePanel("Predicted Deaths from Lung Disease (UK)"),
  
  sidebarLayout(
    sidebarPanel(
      numericInput("months", label = "Months to Predict", 
                   value = 72, min = 12, max = 144, step = 12),
      selectInput("interval", label = "Prediction Interval",
                  choices = c("0.80", "0.90", "0.95", "0.99"),
                  selected = "0.95"),
      checkboxInput("showgrid", label = "Show Grid", value = TRUE)
    ),
    mainPanel(
      dygraphOutput("dygraph")
    )
  )
))