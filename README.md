# KSA206 course development

This repository contains the Jupyter Notebooks created for the ocean component of the KSA 206 course. Embedded within the notebooks are questions and exercises for the students to answer. 

The [Working with CoPilot](https://github.com/julia-neme/KSA_Observations_Modelling/blob/main/Working_with_CoPilot.ipynb) notebook provides some recommendations and showcases an example in which we start with absolutely nothing, and with the adequate prompts we get CoPilot to plot us a climatology of NSIDC, a time series annual averages of sea ice extent, and monthly cycle for each year. It shows how bad prompting returns funky results, and how you can iterate to finally get what you where asking.

# Requirements to run these notebooks

I think the best way to work in class will be with personal computers. In order to do so, students need to set up a python working environment, which is easily done in three steps:
1. Install and editor - I've chose VS Code which is the same thing they use in KIT 101 and I like it a lot.
2. Install miniconda 
3. Install an environment already prepared that you can download from this repository (`ksa206.yml`). Not to fear, this is done by copy pasting one line of code. 

**Complete instructions for setting up a python working environment in a computer (Mac, Linux and Windows) can be found in the [Wiki](https://github.com/julia-neme/KSA_Observations_Modelling/wiki)**

# Content

The tables below summarize the content created for the ocean's component of this course. The jupyter notebooks for each class can be downloaded by each student and ran interactively. Note that they require a conda environment with specific libraries installed (see [Requirements to run these notebooks](#requirements-to-run-these-notebooks)).

## First week

Introduction to `python`. 

1. Class 1: getting set up with the working environment following instructions in [Wiki](https://github.com/julia-neme/KSA_Observations_Modelling/wiki). Basics of Jupyter Notebooks.

2. Class 2: introduction to libraries that we will use in the course: `numpy`, `xarray`, (any others?)/

## Ocean

### Observations

In these four classes students will learn:

1. What is a netcdf file, how to open it using `xarray` and how to explore the file structure and metadata (including dimensions, coordinates and attributes)
2. Work with ungridded data (CTDs) and interpolate onto a grid
3. Perform operations in gridded data products (selection, slicing, averages in different dimensions, integration, calculation of trends)
4. The concept of gradients and geostrophic balance
5. Lots of different ways to plot: scalars, timeseries, maps with `cartopy`, using colormaps (including `cmocean`), calculate trends and significance hatching, etc.

| Week # | Topic                  | Learning goals/activities                                                                                                                                                                                                                                                                      |
| ------- | ---------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 4       | CTDs                   | - Introducing MISO voyage and how to sample CTD<br>- Opening a CTD profile and reading the metadata (location, time, sensors). Comparison with bottle data.<br>- Make a TS diagram from multiple CTDs. Try colouring the TS with different variables and try water mass identification.        |
| 4       | CTDs (continued)       | - Build I09S cross section from interpolation of CTDs and plot (t, s, oxygen). Compare with past occupations downloaded from EasyOcean. <br>- Identify the AABW layer and look at contraction across ocupations. Calculate average temperature, salinity and oxygen content in the AABW layer. |
| 5       | EN.4.2.2<br><br>       | - Look at number of observations per year and seasonal distribution<br /> - Plot surface variables/zonal mean/Hovmoller of depth/time<br /> - Calculate trends at the surface, at the bottom, and in the zonal mean                                                                            |
| 5       | Satellite observations | - Understanding satellite altimetry and the geoid, plotting absolute dynamic topography and seasonal anomalies, compare with a snapshot <br> - Introducing geostrophic balance, calculating surface currents, interpret what the balance is through visualising SSH contours + current vectors |

Note: RV Investigator tour? 

### Modelling

**To be replaced (hopefully) by oceananigans**

| Week # | Topic                                        | Learning goals/activities                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| ------- | -------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 6       | Introduction to ACCESS-OM2 and creative time | - Overview of ACCESS-OM2 (components, forcing, etc)<br><br>Provide a mini dataset of the SO from ACCESS-OM2 IAF (temperature, salinity, oxygen, sea level, surface currents), divide into working groups, and have an attempt at using the code from the Observations part to do analysis of their choice on the model data. This will (a) provide a bit of a change of pace, (b) make them practice using CoPilot to help, (c) allow for interactions between students and (d) give the lecturer an idea of how much they are understanding and how hard can the assessment be.<br><br>We will provide suggestions of a couple different investigations they can carry out.<br><br>**If this is too much for this class it can either be moved forward or used as assessments** |
| 6       | Transport streamfunction                     | - Use model's transport to calculate a streamfunction for the horizontal transport<br>- Develop interpretation skills: what is the circulation depicted by the streamfunction. Calculate Drake Passage strength and subpolar gyre's strength.<br>- Building up from the horizontal transport streamfunction, calculate the MOC streamfunction. Identify the cells of circulation.<br>- Compare depth space to density space                                                                                                                                                                                                                                                                                                                                                      |
| 7       | Future projections experiment                | - Overview of a simulation of EOF changes in SSP585 scenario<br>- Look at the forcing fields used<br>- Initial look at a couple of Southern Ocean changes in the simulation without meltwater                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 8       | Future projections experiment (continued)    | - Expand on previous class by looking at the experiment with meltwater changes included.<br>- Look at how, by looking at the difference between this class and last's simulations we can isolate the effect of meltwater.<br>- If there is time, questions + creative time. Use the output to look at what they want.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |


##  Notes
 - KIT101 (after zoom with Lawrence): this is a programming course the students will have done before KSA206. It is a course in `python` focused on students acquiring the programming logic, understanding algorithms, code structure, functions, etc. They don't use any libraries or conda - it is core python skills.
