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

## Glaciers

| Week | Topic |Learning goals/activites|
| ------- | ---------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|1| Introduction | - Installing VSCode/Miniconda/environment in personal computer <br> - Setting up ARE <br> - Going through introduction to jupyter notebooks (code/markdown cells), python syntax, built-in functions, etc. <br> - Introduction to main libraries used in the course (`numpy`, `xarray`, `matplotlib`, 'cartopy`, etc) |
|2| | | |


## Ocean


| Week  | Topic                  | Learning goals/activities                                                                                                                                                                                                                                                                      |
| ------- | ---------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 4       | CTDs                   | - Introducing MISO voyage and how to sample CTD<br>- Opening a CTD profile and reading the metadata (location, time, sensors). Comparison with bottle data.<br>- Make a TS diagram from multiple CTDs. Try colouring the TS with different variables and try water mass identification.  - Build I09S cross section from interpolation of CTDs and plot (t, s, oxygen). Compare with past occupations downloaded from EasyOcean. <br>- Identify the AABW layer and look at contraction across ocupations. Calculate average temperature, salinity and oxygen content in the AABW layer.      |
| 5       | EN.4.2.2<br><br>Satellite observations      | - Look at number of observations per year and seasonal distribution<br /> - Plot surface variables/zonal mean/Hovmoller of depth/time<br /> - Calculate trends at the surface, at the bottom, and in the zonal mean                      <br> - Understanding satellite altimetry and the geoid, plotting absolute dynamic topography and seasonal anomalies, compare with a snapshot <br> - Introducing geostrophic balance, calculating surface currents, interpret what the balance is through visualising SSH contours + current vectors                                                      |
| 6       | Introduction to ACCESS-OM2 | - Overview of ACCESS-OM2 (components, forcing, etc)<br> - Compare ACCESS-OM2 against I09S (interpolating obs to model grid)<br>-Caculating a transport streamfunction and interpreting it. Drake Passage transport, gyre transport. <br> - Meridional Overturning Circulation |
| 7       | Future projections experiment                | - Overview of a simulation of EOF changes in SSP585 scenario<br>- Look at the forcing fields used<br>- Changes in the open ocean: surface temperatures and salinity, bottom temperatures and salinity, changes to the circulation. <br> Changes on the shelf: cross sections at some locations, look at the Antarctic Slope Current. |                                                                                                                                              

## Sea ice 

| Week  | Topic                  | Learning goals/activities                                                                                                                                                                                                                                                                      |
| ------- | ---------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 8 | | |

##  Notes
 - KIT101 (after zoom with Lawrence): this is a programming course the students will have done before KSA206. It is a course in `python` focused on students acquiring the programming logic, understanding algorithms, code structure, functions, etc. They don't use any libraries or conda - it is core python skills.
