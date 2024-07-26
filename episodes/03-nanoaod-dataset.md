---
title: "NanoAOD datasets"
teaching: 10
exercises: 5
---

:::::::::::::::::::::::::::::::::::::: questions 

- How do we find a specific nanoAOD dataset?
- How to we explore the content of our nanoAOD dataset?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Know how to find nanoAOD datasets
- Know how to explore the content of nanoAOD 

::::::::::::::::::::::::::::::::::::::::::::::::

## Find and explore a nanoAOD dataset

Let's find and explore a particular which we will get even further into
later: simulated Z' events in which the Z' decays to a top and antitop quark pair.

:::::: callout
A Z' ("Z-prime") is a hypothetical heavy gauge boson that could come from
extensions of the Standard Model. A review of searches for the Z' 
can be found [here](https://pdg.lbl.gov/2024/reviews/rpp2024-rev-zprime-searches.pdf)
::::::

### Find the dataset

All data can be found via the [CERN Open Data Portal](https://opendata.cern.ch).
Let's go to the website and search the simulated Z' datasets. 

Dataset naming in CMS can seem obscure but let's do something simple and search for "Zprime*":

![](fig/ZprimeODP.png){alt='Search for Zprime* at the CODP'}

The query results are [here](https://opendata.cern.ch/search?q=Zprime%2A&l=list&order=asc&p=1&s=10&sort=bestmatch) and you can see that there are many (over 1000) records returned:

![](fig/ZprimeODP-results.png){alt='Search results for Zprime*'}

Let's narrow down the results and select **Dataset** under Type, **CMS** under Experiment, **2016** under "Year", **nanoaodsim** under File type, and **Heavy Gauge Bosons** under Category. We've now reduced the number of [matches](https://opendata.cern.ch/search?q=Zprime%2A&f=experiment%3ACMS&f=year%3A2016&f=file_type%3Ananoaodsim&f=category%3AExotica%2Bsubcategory%3AHeavy%20Gauge%20Bosons&f=type%3ADataset&l=list&order=asc&p=1&s=10&sort=bestmatch) from over 1000 down to 210:

![](fig/ZprimeODP-results2.png){alt='Narrowed search results for Zprime*'}

We can discern some of the logic behind the simulated dataset naming. "Zprime" is the particle produced and it decays to various products. We want $Z^{'} \rightarrow t\bar{t}$ which shows up as the third result so let's [narrow the search](https://opendata.cern.ch/search?q=ZprimeToTT%2A&f=experiment%3ACMS&f=year%3A2016&f=file_type%3Ananoaodsim&f=category%3AExotica%2Bsubcategory%3AHeavy%20Gauge%20Bosons&f=type%3ADataset&l=list&order=asc&p=1&s=10&sort=bestmatch) further and search with "ZprimeToTT*":

![](fig/ZprimeToTT-results.png){alt='Narrowed search results for Zprime*'}

We can also discern that the dataset names also include the mass (in GeV) of the hypothetical Z' (e.g. "_M2000"). 

:::::::::::::::::: callout 

### Why such long dataset names?

CMS open data are the same files that have been used in the data analysis by CMS members. The names come from naming conventions for the production system.

Go back to the [pre-exercise](https://cms-opendata-workshop.github.io/workshop2024-lesson-dataset-scouting/instructor/03-what-data-is-available.html#monte-carlo) for a brief explanation of the simulated dataset names.

::::::::::::::::::

::::::::::::::::::::: challenge

### Exercise 1: Select a Z' mass and find the corresponding dataset

:::::::::::::: solution

Search with "ZprimeToTT_M<mass>" where <mass> is the value you selected.

::::::::::::::

::::::::::::::::::::


Next, let's use the `cernopendata-client` command-line tool to find the datasets
and fetch a file.

::::::::::::::::::::: challenge

### Exercise 2: Find a file name in the dataset

:::::::::::::: solution

Go back to the [pre-exercise](https://cms-opendata-workshop.github.io/workshop2024-lesson-dataset-scouting/instructor/04-cli-through-cernopendata-client.html) to see how to get the file names with the command-line tool.

::::::::::::::

::::::::::::::::::::

### Explore a file

We will now have a look at the file contents.

:::::::::::::::::: callout 

### How to see the variable names?

Remember that each NanoAOD/NanoAODSIM dataset has the variable list linked to the record:

![](fig/ZprimeVariableList.png){alt='Link to the variable list in the record'}

::::::::::::::::::

Now let us plot the value of some these variables. Open the `my_python` container 

```bash
docker start -i my_python
```

If you want to use jupyter notebooks, start jupyter-lab with

```bash
jupyter-lab --ip=0.0.0.0 --no-browser
```

Open the link given in the message on your browser. Choose the icon under “Notebook”.


### Exercise 3: Explore the file with the Python tools

:::::::::::::: solution

Go back to the [pre-exercise](https://cms-opendata-workshop.github.io/workshop2024-lesson-cpp-root-python/instructor/06-uproot.html) to see how to open the file names using uproot.

::::::::::::::

::::::::::::::::::::


::::::::::::::::::::::::::::::::::::: keypoints 

- Use search facets and text search with wildcards to narrow your search. 

::::::::::::::::::::::::::::::::::::::::::::::::

[r-markdown]: https://rmarkdown.rstudio.com/
