---
title: "Introduction"
teaching: 10
exercises: 5
---

:::::::::::::::::::::::::::::::::::::: questions 

- What have we learned in the pre-leaning lessons and how can we apply it?
- Where do we find information about physics objects in the CMS NanoAOD format?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Apply what we have learned in the pre-learning lessons about CMS physics objects
- Learn about the documentation of the NanoAOD format

::::::::::::::::::::::::::::::::::::::::::::::::

## Dataformats in CMS

Most previous releases of CMS open data have been in the Analysis Object Data (AOD) format. 
This is a complex format and specific CMS software (CMSSW) is required in order to read and analyze it.

From 2015 data releases have been a slimmed-down format called MiniAOD, which has the same essential structure and software requirements for analysis as AOD. Essentially there are few 
physics object collections and often the physics objects themselves are different. 

For data released in 2016 and beyond a new format called NanoAOD is used. NanoAOD is not just simply slimmed-down MiniAOD. In contrast to AOD and MiniAOD which is stored in CMSSW C++ objects, NanoAOD is stored using ROOT TTree objects. You therefore do not need to use the CMS Virtual Machine or docker container to analyze NanoAOD data. NanoAOD can be analyzed using the ROOT program and/or python libraries capable of interpreting the ROOT's TTree structure.

In this workshop we will focus on working with open data in the NanoAOD format.

## Physics objects in CMS data

The recommended [CMS Physics Objects prelearning lesson](https://cms-opendata-workshop.github.io/workshop2024-lesson-physics-objects/instructor/index.html) guides you through different physics objects and explains what information is available for them in the CMS NanoAOD format.

Let us now make sure that you can find that information.

::::::::::::::::::::: challenge

## Exercise 1: Find the NanoAOD variable description for a physics object

Select a physics objects of your choice in the [CMS Physics Objects lesson](https://cms-opendata-workshop.github.io/workshop2024-lesson-physics-objects/instructor/index.html) and find the corresponding variable listing from a CMS dataset record on the [CERN Open Data portal](https://opendata.cern.ch/).

:::::::::::::: solution

Find the NanoAOD variable listing for example for the [SingleElectron collision dataset from 2016 RunG](https://opendata.cern.ch/record/30529). Scroll down to "Dataset semantics" and open the [variable list](https://opendata.cern.ch/eos/opendata/cms/dataset-semantics/NanoAOD/30529/SingleElectron_doc.html).

Find the links to the physics object collections under "Events Content" and find the object of your choice.

::::::::::::::

::::::::::::::::::::

::::::::::::::::::::: challenge

## Exercise 2: Compare variable lists in different collision datasets.

Find all collision datasets from 2016 in NanoAOD format. Compare the variable list. Do Muon datasets contain an electron collection? Do Electron datasets contain a muon collection? Why?

:::::::::::::: solution

Use the search facets of the [search page](https://opendata.cern.ch/search?q=&l=list&order=desc&p=1&s=10&sort=mostrecent). 

Select **Collision** under Dataset, **CMS** under Experiment, **2016** under "Year", and **nanoaod** under File type.

Open two different collision datasets and check their variable lists.

::::::::::::::

::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: keypoints 

- The variable list with a variable brief description is linked to all CMS NanoAOD datasets. 
- CMS Physics Objects pre-learning lesson describes different physics object variables in more detail.

::::::::::::::::::::::::::::::::::::::::::::::::

