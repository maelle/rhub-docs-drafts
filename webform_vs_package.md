# Submit your package with the webform or the package?

You can submit a package using either the **webform**'s [simple interface](https://builder.r-hub.io/) or [with advanced options](https://builder.r-hub.io/advanced); or via the **R package `rhub`**. We strongly recommend using the package for a smoother workflow and more customization. 

In more details, why rather use `rhub`?

- Using the package is quite natural whilst you're developing an R package in your favorite IDE. You might be used to `devtools::check()` to run checks locally, and `devtools::check_win_devel()` to bundle and send the package to Winbuilder. `rhub::check()` works very similarly: it can take the path to your package folder as argument (by default the current directory!), and will build and upload it. You can then watch the live log from your console, or wait until you get an email after the build.

- When using the web interface you can set neither extra arguments for the `R CMD check` command nor environment variables to set on the builder machine, which you might actually need for finer control of the check, or e.g. to provide your secret web API key.

- While you _can_ select several platforms to build your package on via the web interface, you need to choose those by hand, whereas the package has handy shortcuts (even handier when using an editor with autocompletion like RStudio) such as `rhub::check_on_windows()` and the very useful `rhub::check_on_cran()`.