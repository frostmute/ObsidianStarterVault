## Metadata

* URL: [https://appsilon.com/r-markdown-reporting-best-practices/](https://appsilon.com/r-markdown-reporting-best-practices/)
* Author: *Eduardo*
* Publisher: *appsilon.com*
* Published Date: 2022-02-08

## Highlights

* Working with R Markdown allows you to create different types of reports, from static websites to PDFs and slides in R. Many of them come with templates, but also let you adjust for specific user needs. This makes R Markdown easy to use and an efficient way to turn data analyses into cohesive, high-quality reports.
* R Markdown Reporting – Documents The steps required to create R Markdown reports are set primarily by knitr and pandoc, but also other extensions such as latex with tinytex. How many file formats can R Markdown render? R Markdown can render formats from HTML docs, Notebooks, PDFs, Word docs, OpenDocument text, Rich text, Markdown variants, vignettes – and that’s just covering documents some more include: It is worth mentioning that R Markdown knitr can execute code in other languages besides R, including: * Python * SQL * Julia * JavaScript * CSS
* YAML and R Markdown In order to define which type of document the report will result in, knitr requires metadata that states the output format. This is done in the YAML header of the R Markdown file: YAML contains a set of arguments that each document can have. Even different packages can have their own set of rules that can be adjusted through the YAML component It usually is set on the header of the R Markdown document but can also be used as a separate file. YAML is an extensible approach to metadata. That means that any metadata that is incorrect will fail silently. This may cause issues in passing the correct information or what is available by the package.
* ymlthis is a package that gathers the most common approaches when setting YAML for R markdown documents. It contains a yaml fieldguide that shares the most common sources of YAML. The ymlthis addon saves a lot of time when setting up the YAML configuration. This is possible because it has a set of the most common configuration for many types of well-known documents:
* Read the documentation first This may seem straightforward, but the truth is: There is no better place to understand the appropriate metadata and design of the markdown document than with the maintainer. For packages that are so well adopted like R Markdown, most common issues and expected behavior are already documented. Save time and headaches by going to the source.
* Leverage Rstudio UI and package templates When rendering new R Markdown documents, you can use templates from Rstudio UI and leverage the options that new packages can have.
* Create your own templates for R Markdown Making your own templates will boost your productivity and keep you with steady-state documents. This can be used through many types of documents such as word documents or even HMTL documents, including slides, by setting your own HTML and/or CSS template. Bslibs is a great resource when setting the UI design since it allows you to dynamically set the CSS components:
* Separate the document into different pieces This is not only important to make your code cleaner but also reusable. Let’s take the {xaringan} package as an example:
