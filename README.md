# ca-coast-poll

California coastal poll analysis and introduction to R for Coastal and Marine Management class at CSUCI 2019-11

# Binder

Click on the following "launch binder" link to launch RStudio with the necessary packages installed:

[![Launch Rstudio Binder](http://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/bbest/ca-coast-poll/master?urlpath=rstudio)

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