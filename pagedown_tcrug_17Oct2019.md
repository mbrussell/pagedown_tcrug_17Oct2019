Getting down with pagedown: Using R Markdown to create paged HTML documents
========================================================
autosize: true
author: Matt Russell, PhD
date: 17 Oct 2019
Twin Cities R User Group 




About
========================================================
![The University of Minnesota](http://www.drupal.com/sites/default/files/UMN_wordmark.png)
![Arbo Custom Analytics LLC](https://arbor-analytics.com/post/2019-07-14-using-google-forms-to-analyze-confidence-intervals-a-teaching-statistics-activity_files/arbor_horiz.png) 
***

University of Minnesota, Department of Forest Resources
- Associate Professor
- Instruct a graduate class in statstics in natural resources
- Research and outreach on forest health issues


Arbor Custom Analytics LLC
- Consulting for the forest products industry.


The value of R Markdown
========================================================
![R Markdown](https://bookdown.org/yihui/rmarkdown/images/hex-rmarkdown.png)
***

Markdown integrates text and R code.
- Reports are fully reproducible 
- Supports static and dynamic output formats (e.g., HTML, PDF, MS Word)
- Adapted to use R, Python, and SQL languages


R Markdown documents facilitate learning R and statistics
========================================================

![An example of an R Markdown assignment used in a statistics class, page 1.](ESPM3012_Lab8Solutions_Page_1.jpg)

***

![An example of an R Markdown assignment used in a statistics class, page 2.](ESPM3012_Lab8Solutions_Page_2.jpg)

R Markdown: more than just documents
========================================================

- Themed documents 
- Presentations (like this one!)
- Books (bookdown)
- Dashboards (flexdashboard)
- Websites (blogdown)

***

![bookdown](https://bookdown.org/yihui/blogdown/images/cover.png)

What is pagedown?
========================================================
- Contains output formats for paged HTML documents, letters, resumes, posters, business cards, etc.
- Uses Paged.js (Javascript library) to paginate web documents
- Can include headers, footers, and page margins to make elegant documents

The package can be installed from Github:


```r
remotes::install_github('rstudio/pagedown')
```

New pagedown file in RStudio
========================================================
- **File** -> **New File** -> **R Markdown** -> **From Template**
- Several templates available

***

![Creating a new pagedown file in RStudio](newfile.png)



pagedown:: html_paged
========================================================

- Creates a paged HTML document.
- Can include table of contents and numbered sections.
- Example: citizen science project showing data.


```r
output:
  pagedown::html_paged: 
    toc: true
    number_sections: true
```


An example: Cover of a paged HTML document
========================================================


***
![An example HTML report created with pagedown, page 1](Assessing Vegetation Impacts from Deer Citizen Science Project_ 2019 results_Page_01.jpg)

page 1
========================================================
![An example HTML report created with pagedown, page 2](Assessing Vegetation Impacts from Deer Citizen Science Project_ 2019 results_Page_02.jpg)
***
![An example HTML report created with pagedown, page 3](Assessing Vegetation Impacts from Deer Citizen Science Project_ 2019 results_Page_03.jpg)

pages 2-3
========================================================
![An example HTML report created with pagedown, page 5](Assessing Vegetation Impacts from Deer Citizen Science Project_ 2019 results_Page_04.jpg)
***
![An example HTML report created with pagedown, page 6](Assessing Vegetation Impacts from Deer Citizen Science Project_ 2019 results_Page_05.jpg)

pages 4-5
========================================================
![An example HTML report created with pagedown, page 7](Assessing Vegetation Impacts from Deer Citizen Science Project_ 2019 results_Page_06.jpg)
***
![An example HTML report created with pagedown, page 8](Assessing Vegetation Impacts from Deer Citizen Science Project_ 2019 results_Page_07.jpg)

pages 6-7
========================================================
![An example HTML report created with pagedown, page 9](Assessing Vegetation Impacts from Deer Citizen Science Project_ 2019 results_Page_08.jpg)
***
![An example HTML report created with pagedown, page 10](Assessing Vegetation Impacts from Deer Citizen Science Project_ 2019 results_Page_09.jpg)

pagedown::html_resume
========================================================

- Two parts: an **Aside** and **Main** section


```r
---
title: "resume_example"
author: "Matt Russell"
output: pagedown::html_resume
---
```

***

![An example resume created with pagedown](resume.png)


pagedown::business_card
========================================================

- Single card for an individual
- Multiple cards for several employees on the same page

```r
---
name: Matt Russell, PhD
output: pagedown::business_card
---
```

***

![An example business card created with pagedown](card.png)


Other pagedown documents
========================================================

- Letters
- Theses/dissertations
- Posters
- Journal articles

Other features
- Cover pages
- Lists of tables and figures
- Custom running headers
- Page references
- Line numbering

***

![An example journal article created with pagedown](https://user-images.githubusercontent.com/19177171/51005498-5b46cb80-153f-11e9-9026-4b50a9f3d3f1.png)

Pros/cons of pagedown
========================================================
Pros
- Create high-quality PDFs through a web browser
- Flexible if you know CSS and Javascript

***

Cons
- Works best on Chrome or Chromium
- May need to use with `xaringan` to print to web browser (and the "Infinite Moon Reader" function)


```r
xaringan::inf_mr("my_resume.Rmd")
```


Learn more!
========================================================
Pagedown documentation
- [pagedown from Github](https://github.com/rstudio/pagedown)
- [pagedown documentation](https://pagedown.rbind.io/)
- VIDEO: [Yihui Xie presentation at rstudio::conf 2019](https://resources.rstudio.com/rstudio-conf-2019/pagedown-creating-beautiful-pdfs-with-r-markdown-and-css) 
- SLIDES: [Yihui Xie presentation at rstudio::conf 2019](https://slides.yihui.name/2019-rstudio-conf-pagedown.html#1) 

Other applications
- [A quick ride on pagedown](http://www.andreacirillo.com/2019/01/27/a-quick-ride-on-pagedown-create-pdf-from-rmarkdown/). Blog post by Andrea Cirillo.
- [A CV built with pagedown](https://github.com/nstrayer/cv). Code by Nick Strayer.

Thanks to the main authors Yihui Xie and Romain Lesur and other contributors!
