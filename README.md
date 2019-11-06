# ca-coast-poll

California coastal poll analysis and introduction to R for Coastal and Marine Management class at CSUCI 2019-11.

## Objectives 2019-11-06

1. Become acquainted with **programming basics** and **reproducible research**.
1. Make your own **R Markdown** (aka Rmarkdown, Rmd) document.
1. Learn some **R basics* by working on `inflammation.Rmd`. And time permitting...
1. Make **interactive plots** using `plotly::ggplot()`.
1. Perform some quality control (**QC**) on the [MASTER DATA-Opinion Poll F2019 - Google Sheets](https://docs.google.com/spreadsheets/d/1hH68SqNsvAASFn25-X9ssJPkcGSS-SfS6n3zui9hYOQ/edit#gid=1739121823) by reviewing answers having responses > 1:  [ca-coast-poll/poll_log.csv at master · bbest/ca-coast-poll](https://github.com/bbest/ca-coast-poll/blob/master/data/poll_log.csv).
1. Have **fun** with data science :) ...

## Resources

- slides: [Data Science for Marine Conservation](https://docs.google.com/presentation/d/1yHQir_zgYqRIDuADHnVTsbhXLO3nEzL3OfHU3oCbUNE/edit?usp=sharing)
- video: [What is R Markdown?](https://vimeo.com/178485416) (1 minute)
- `poll.Rmd`: poll analysis
  - [MASTER DATA-Opinion Poll F2019 - Google Sheets](https://docs.google.com/spreadsheets/d/1hH68SqNsvAASFn25-X9ssJPkcGSS-SfS6n3zui9hYOQ/edit#gid=1739121823)
  - [`poll.html`](./poll.html)
- `inflammation.Rmd`: Software Carpentry lesson
  - [`inflammation.html`](./inflammation.html)
  - [Programming with R: Analyzing Patient Data](http://swcarpentry.github.io/r-novice-inflammation/01-starting-with-data/index.html)

## Instructions

1. Launch Rstudio in your web browser by clicking on the following:
  [![Launch Rstudio Binder](http://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/bbest/ca-coast-poll/master?urlpath=rstudio)
1. Make your first **Rmd**. In RStudio, File > New File > R Markdown... Name the file **first** and Save, which will get saved as `file.Rmd`. Click on the **Knit**.
1. Open `inflammation.Rmd` and click cursor line by line on R code and execute by entering `Control + Enter` keys.

## Further Resources

1. [R for Data Science](https://r4ds.had.co.nz/): the "bible" book free online
1. [DataCamp.com](https://www.datacamp.com/home): learn R, Python & Data Science Online with badges (some free, most paid)

## Old Resources

These resources were created when previously looking at this opinion poll 2019-02:

- [calcoastpoll](http://benbestphd.com/calcoastpoll/index.html): R package
  - [Analyze Poll Data](http://benbestphd.com/calcoastpoll/articles/analyze.html): vignette
- [calcoastpoll-tutorial](http://benbestphd.com/calcoastpoll-tutorial/index.html): bookdown


### Binder Setup

Here's how the necessary files were created in this repository for the "Launch Rstudio Binder" link to work:

```r
library(holepunch)
write_compendium_description(
  package     = "ca-coast-poll", 
  description = "California coastal poll analysis and introduction to R")
# to write a description, with dependencies. Be sure to fill in placeholder text

write_dockerfile(maintainer = "Ben Best") 
# To write a Dockerfile. It will automatically pick the date of the last 
# modified file, match it to that version of R and add it here. You can 
# override this by passing r_date to some arbitrary date
# (but one for which a R version exists).

generate_badge() # This generates a badge for your readme.

# ----------------------------------------------
# At this time 🙌 push the code to GitHub 🙌
# ----------------------------------------------

# And click on the badge or use the function below to get the build 
# ready ahead of time.
build_binder()
```