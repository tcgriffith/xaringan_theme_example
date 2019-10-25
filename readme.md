
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


[Demo](https://tcgriffith.github.io/xaringan_theme_example/)