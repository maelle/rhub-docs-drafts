# How to build R packages for distributing them?

Imagine you want to share your package with colleague working on a different operating system, without access to tools for building packages on that platform. How do you create an appropriate binary for your package?

## Once in a while

If you're only doing this sporadically, you can use R-hub builder to build your package on the platform corresponding to your colleague's computer. In the email you'll receive after a (hopefully successful) build, there's a link to _artefacts_ i.e. the built package that you can download and send to your colleague. You can also retrieve the link to _artefacts_ using `rhub`. ADD CODE ONCE THERE IS A METHOD.

## Regularly

If you want to regularly build and deploy your package on different platforms, what you are looking for is _continuous integration_ (LINK TO external thing explaining what CI is?).

* R-hub CI. Not at the moment, but eventually R-hub will offer a CI service, unsurprisingly specific to R packages.

* Appveyor (Windows). Each build has a [tab with artefacts](https://ci.appveyor.com/project/jeroen/gifski/build/job/g3ryly3s833lomlk/artifacts), and you could automate the workflow with scripts. Refer to [Appveyor docs](https://www.appveyor.com/docs/).

* Travis (MacOS, Linux, soon Windows). Refer to [Travis docs](https://docs.travis-ci.com/), for instance [the page about uploading artefacts](https://docs.travis-ci.com/user/uploading-artifacts/).

* Other CI surely have something similar.