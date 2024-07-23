---
title: "Introduction"
teaching: 10
exercises: 0
---

:::::::::::::::::::::::::::::::::::::: questions 

- What have we learned in the pre-exercises and how can we apply it?
- What is the structure and content of the nanoAOD format?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Apply what we have learned in the pre-exercises
- Learn about the structure and content of nanoAOD

::::::::::::::::::::::::::::::::::::::::::::::::

## Dataformats in CMS

Most previous releases of CMS open data have been in the Analysis Object Data (AOD) format. 
This is a complex format and specific CMS software (CMSSW) is required in order to read and analyze it.

From 2015 data releases have been a slimmed-down format called MiniAOD, which has the same essential structure and software requirements for analysis as AOD. Essentially there are few 
physics object collections and often the physics objects themselves are different. 

For data released in 2016 and beyond a new format called NanoAOD is used. NanoAOD is not just simply slimmed-down MiniAOD. In contrast to AOD and MiniAOD which is stored in CMSSW C++ objects, NanoAOD is stored using ROOT TTree objects. You therefore do not need to use the CMS Virtual Machine or docker container to analyze NanoAOD data. NanoAOD can be analyzed using the ROOT program and/or python libraries capable of interpreting the ROOT's TTree structure.

TO-DO we can "borrow" information from below:

miniAOD links for use: [Getting started with miniAOD](https://opendata.cern.ch/docs/cms-getting-started-miniaod), [miniAOD in Workbook](https://twiki.cern.ch/twiki/bin/view/CMSPublic/WorkBookMiniAOD2016#High_level_physics_objects)

nanoAOD links for use: [Getting started with nanoAOD](https://opendata.cern.ch/docs/cms-getting-started-nanoaod)



::::::::::::::::::::::::::::::::::::: keypoints 

- Use `.md` files for episodes when you want static content
- Use `.Rmd` files for episodes when you need to generate output
- Run `sandpaper::check_lesson()` to identify any issues with your lesson
- Run `sandpaper::build_lesson()` to preview your lesson locally

::::::::::::::::::::::::::::::::::::::::::::::::

[r-markdown]: https://rmarkdown.rstudio.com/
