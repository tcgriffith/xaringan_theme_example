---
author: TC
categories:
- theme
date: "2015-07-26"
tags:
- xaringan
thumbnail: https://user-images.githubusercontent.com/163582/45438104-ea200600-b67b-11e8-80fa-d9f2a99a03b0.png
title: xaringan_example_theme
description: a theme example
---

![](https://user-images.githubusercontent.com/163582/45438104-ea200600-b67b-11e8-80fa-d9f2a99a03b0.png)


## A example xaringan theme example

## How to use this theme

Add the following chunk in your xaringan slide.



        ```{r echo=TRUE}
        use_theme_github = function(theme = "tcgriffith/xaringan_theme_example", ref =
                                      "master") {
          bn = basename(theme)
          
          css_remote = paste0("https://raw.githubusercontent.com/",
                              theme,
                              "/",
                              ref,
                              "/",
                              bn,
                              ".css")
          
          css_name = basename(css_remote)
          xfun::download_file(css_remote)
          
          htmltools::includeCSS(css_name)
        }
        use_theme_github("tcgriffith/xaringan_theme_example", "83908f")
        ```

<style>
.resp-container {
    position: relative;
    overflow: hidden;
    padding-top: 56.25%;
}

.testiframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: 0;
}
</style>



## Demo

[slide](https://tcgriffith.github.io/xaringan_theme_example/)
[source](https://github.com/tcgriffith/xaringan_theme_example/blob/master/index.Rmd)


<div class="resp-container">

<iframe class="testiframe" src="https://tcgriffith.github.io/xaringan_theme_example/use_master.html">
  Fallback text here for unsupporting browsers, of which there are scant few.
</iframe>

</div>

[link](use_master.html)

[csslink](xaringan_theme_example.css)
