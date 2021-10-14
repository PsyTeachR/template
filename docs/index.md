--- 
title: "Template" # edit
#subtitle: "optional" 
author: "psyTeachR Team" # edit
date: "2021-10-14"
site: bookdown::bookdown_site
documentclass: book
classoption: oneside # for PDFs
geometry: margin=1in # for PDFs
bibliography: [book.bib, packages.bib]
csl: include/apa.csl
link-citations: yes
description: | # edit
  The book template for the psyTeachR books.
url: https://psyteachr.github.io/template # edit
github-repo: psyteachr/template # edit
cover-image: images/logos/logo.png # replace with your logo
apple-touch-icon: images/logos/apple-touch-icon.png # replace with your logo
apple-touch-icon-size: 180
favicon: images/logos/favicon.ico # replace with your logo
---



# Overview {-}

<div class="small_right"><img src="images/logos/logo.png" 
     alt="ADS Hex Logo" /></div>



* [PDF version](template.pdf)
* [ePub version](template.epub)
* [Kindle version](template.mobi)

After copying this template to your project, you will need to change the information in the `CITATION` and `DESCRIPTION` files, as well as update the YAML header of `book/index.Rmd` and `book/_output.yml`. Update site-specific logos in `book/images/logos/`.

If you are not part of the psyTeachR group, please edit the Google Analytics ID in `include/google-analytics.html` or comment out the relevant line in `book/_output.yml`. 

Render the book using the code in `_render.R`.

## Changes

### Version 2.1 2021-10-14

* Updated webexercises styles to include a green check and red X for correct and incorrect responses.
    - `book/include/webex.css` (replace)
    - `book/include/webex.js` (replace)
* Changed the name of `book/include/header.html` to `book/include/google-analytics.html` to better reflect its purpose. 
    - `book/include/header.html` (delete)
    - `book/include/google-analytics.html` (add)
    - `book/_output.yml` (change line 10)
* Updated rendering functions to not render pdf epub or mobi by default
    - `_render.R` (replace)
    - `Makefile` (add)
