# Diamonds Case Study

**Objective**: Find the best-value diamond under $3,000 based on cut, color, and clarity.

**Tools**: R (`dplyr`, `ggplot2`), R Markdown.

**Approach**:
- Analyzed cut, color, and clarity with `dplyr` and visualized with `ggplot2`.
- Filtered diamond dataset for prices under $3,000.
- Generated a report recommending optimal diamond choices to maximize money value.

**Key Insight**: Recommended Premium cut, I color, VS2 clarity diamonds to maximize quality within $3,000.

**Files**:
- [Diamonds_Analysis.Rmd](Diamonds_under_3000.Rmd): R Markdown with code.
- [Diamonds_Report.pdf](Diamonds_under_3000.pdf): Full report.

**How to View**: Open `.Rmd` in RStudio or view the PDF.

## Key Code Example
```{r echo=FALSE, fig.align="center", message=FALSE, warning=FALSE}
library(dplyr)
library(scales)
library(knitr)
library(kableExtra)

# Create display version of top picks
best_diamonds_display <- best_diamonds %>%
  mutate(
    Price = dollar(price),
    `Price per Carat` = dollar(price_per_carat),
    Carat = round(carat, 2),
```

## Key Visualization
![Diamond Price vs. Carat](price_vs_carat.jpeg)
