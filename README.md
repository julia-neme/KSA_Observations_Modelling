## To-dos (after meeting)
 - Find out what they are learning at KIT 101
 - Talk with Sophie how they are using python (nectar, google collab, etc)
 - Mylo page (sandpit) build page
 - Talk to Lawrence Sambrooks (Paul)

# Content

The tables below summarize the content created (and to be created) for the ocean's component of this course. The jupyter notebooks for each class can be run interactively, and require a conda environment with specific libraries installed (see [Requirements to run these notebooks](#requirements-to-run-these-notebooks))

Embedded within the notebooks are questions and exercises for the students to answer. These are summarised in the [List of questions](https://github.com/julia-neme/KSA_Observations_Modelling/blob/main/List_of_questions.md).

The [Working with CoPilot](https://github.com/julia-neme/KSA_Observations_Modelling/blob/main/Working_with_CoPilot.ipynb) notebook provides some recommendations and showcases an example in which we start with absolutely nothing, and with the adequate prompts we get CoPilot to plot us a climatology of NSIDC, a time series annual averages of sea ice extent, and monthly cycle for each year. It shows how bad prompting returns funky results, and how you can iterate to finally get what you where asking.

## Observations

| Class # | Topic                    | Learning goals/activities                                                                                                                                                                                                                                                               | Resources                                                                                        |
| ------- | ------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ |
| 1       | CTDs             | - Introducing MISO voyage and how to sample CTD<br>- Opening a CTD profile and reading the metadata (location, time, sensors). Comparison with bottle data.<br>- Make a TS diagram from multiple CTDs. Try colouring the TS with different variables and try water mass identification. | `1_Introduction_to_CTDs.ipynb`<br><br>`2_Multiple_CTDs.ipynb`<br><br>Interview with Becki<br><br>Videos of the voyage, interview with Annie |
| 2       | CTDs (continued) | - Build I09S cross section from interpolation of CTDs and plot (t, s, oxygen). Compare with past occupations downloaded from EasyOcean. <br>- Identify the AABW layer and look at contraction across ocupations. Calculate average temperature, salinity and oxygen content in the AABW layer.                                                         | `1_Building_a_cross_section.ipynb`<br><br>`2_Antarctic_Bottom_Water_contraction.ipynb`<br><br>Interview Kathy/Kaihe                                                                            |
| 3       | EN.4.2.2<br><br>              | - Look at number of observations per year and seasonal distribution<br /> - Plot surface variables/zonal mean/Hovmoller of depth/time<br /> - Calculate trends at the surface, at the bottom, and in the zonal mean                                                                                                                                                                       |  `1_Introduction_to_EN422.ipynb`<br><br>`2_Calculating_trends.ipynb`                                                                                                |
| 4       | Satellite observations        | - Calculating geostrophic currents from altimetry, identifying ACC or eddies.                                                                                                                                                                                                                                                                                        |                                                                                                  |

Note: RV Investigator tour? 

## Modelling

| Class # | Topic                                                     | Learning goals/activities                                                                                                                                                         | Resources                                              |
| ------- | --------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------ |
| 1       | COSIMA intro; xarray basic and not so basic functionality | - How to access experiments and load data<br>- Showcase the recipes<br>- Open a random data set and go crazy slicing, dicing, weighted and unweighted averages, interpolating (?) | Links to COSIMA stuff, interview myself (and/or Navid) |
| 2       | (c) ACCESS-OM2 simulations                                | - Reproduce a comparison with observations from Kiss et al. 2020<br>- Show fun experiments we can do/not-so-fun experiments we have done?                                         | Interview with Andrew Kiss, Andy Hogg, Adele?          |
| 3       | (d) ACCESS-OM2 future projections (?)                     |                                                                                                                                                                                   |                                                        |
| 4       | (e) Regional MOM6 configurations with Ashley's setup      | - Get a regional configuration and do a fun little experiment? Go crazy, I'm thinking something like splitting Tassie in two, or joining it to the mainland.                      | Ashley's documentation and interview                   |


# Requirements to run these notebooks

You can find this repository, with all the data necessary to run the notebooks in `/g/data/jk72/jn8053/KSA_Observations_Modelling`.

If running in a local environment, the following libraries need to be installed: `cartopy`, `cmocean`, `glob`, `gsw`, `matplotlib`, `metpy`, `numpy`, `scipy`, `xarray` and `xarrayMannKendall`. 
