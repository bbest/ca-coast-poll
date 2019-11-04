# ca-coast-poll

California coastal poll analysis and introduction to R for Coastal and Marine Management class at CSUCI 2019-11.


- slides: [Data Science for Marine Conservation](https://docs.google.com/presentation/d/1yHQir_zgYqRIDuADHnVTsbhXLO3nEzL3OfHU3oCbUNE/edit?usp=sharing)
- `poll.Rmd`: poll analysis
  - [MASTER DATA-Opinion Poll F2019 - Google Sheets](https://docs.google.com/spreadsheets/d/1hH68SqNsvAASFn25-X9ssJPkcGSS-SfS6n3zui9hYOQ/edit#gid=1739121823)
  - [`poll.html`](./poll.html)
- `inflammation.Rmd`: Software Carpentry lesson
  - [`inflammation.html`](./inflammation.html)
  - [Programming with R: Analyzing Patient Data](http://swcarpentry.github.io/r-novice-inflammation/01-starting-with-data/index.html)

**Old:**

- [calcoastpoll](http://benbestphd.com/calcoastpoll/index.html): R package
  - [Analyze Poll Data](http://benbestphd.com/calcoastpoll/articles/analyze.html): vignette
- [calcoastpoll-tutorial](http://benbestphd.com/calcoastpoll-tutorial/index.html): bookdown

## Launch Rstudio using Binder

Click on the following "Launch Rstudio Binder" link to launch RStudio with the necessary packages installed:

[![Launch Rstudio Binder](http://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/bbest/ca-coast-poll/master?urlpath=rstudio)

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