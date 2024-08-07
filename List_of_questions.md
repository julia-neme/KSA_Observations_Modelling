# Questions and exercises

Summary of the questions and exercises embedded within the course notebooks. Click to expand.

<details>
<summary> Class 1: Ship based in situ observations </summary>

#### Introduction to CTDs

 - **Question 1**: <br> _Use [CoPilot](https://copilot.microsoft.com/) to understand what each of the functions we used to plot does. You can ask what `plt.subplots(1, 2, figsize = (10, 5))` does, and how can you modify the code to have a figure with four panels (2 rows and 2 columns)._
 - **Question 2**: <br> _a. Discuss how "potential density" is different from "density", and what are the differences between absolute and practical salinity, and in situ and conservative temperature. Would it have been a big source of error to use the wrong types of temperature and salinity to calculate potential density?_ <br> _b. Can you identify the mixed layer, thermocline and pycnocline depths in this profile? Try changing the limits of the `yaxis` to help you visualize these regions better._
 - **Question 3**: <br> _If we only have 36 bottles, we need to be thoughtful about the depths we collect samples for. Keeping in mind that the main goal is to calibrate our conductivity and oxygen sensors, and looking at the profiles we plotted above, where would you have chose to sample this CTD?_
 - **Question 4**: <br> _Some depths are very important, so we close 2 bottles just in case one fails and doesn't close properly, and/or we have enough litres for all the lab analysis we want. Take a look at the depths we closed bottles at. Can you identify at what regions of the water column we duplicated bottles?_
 - **Question 5**: <br> _Looking at the plot above, you can see that the difference between sensor and bottle data seems larger at the surface. Can you think of a reason why?_
 - **Question 6**: <br> _You can see in the CTD file that we have data from 2 sensors for each variable. Make a plot comparing both sensors._ <br>  _Tip: this can either be profiles with both sensors on the same axis, a plot of the difference between sensors, a plot of sensor 1 vs sensor 2, etc._ <br> _Don't be afraid of using CoPilot!_

#### Multiple CTDs

 - **Question 1**: <br> _Try [other projections](https://scitools.org.uk/cartopy/docs/v0.15/crs/projections.html) from `cartopy`, see if you can change the colour of the land, etc. Which one do you think is more appropriate to use in this case?_
 - **Question 2**: <br> _In the figure below, we have replaced `pcolormesh` by `contourf`. What is the difference? Which one do you think is better and why?_
 - **Question 3**: <br> _Looking at the profiles above, can you figure out which ones correspond to each of the three regions on the map we made? Plot the figure but with a different color for each profile's time, like we did for the locations in the map._
 - **Question 4**: <br> _Can you identify the following regions in the T-S diagram?_ <br> -_Stably vs unstably stratified areas_ <br> - _Thermocline/pycnocline_ <br> _Using the above considerations, can you describe in a few words the differences in the water column between the three CTD regions?_
 - **Question 5**: <br> _Instead of colouring by pressure, look at what other variables our CTD profiles have, and choose another (i.e. oxygen, nutrients). Play around with `vmin`, `vmax` to get the most out of your plot, choose different colormaps (the ones we've used so far are not that exciting), etc._
</details>

<details>
<summary> Class 2: Ship based in situ observations (continued) </summary>

#### Building a cross section

 - **Question 1**: <br> _a. Plot cross sections of salinity and oxygen using appropriate colormaps. You can choose from `cmocean`'s [colormaps](https://matplotlib.org/cmocean/) if you'd like. Describe the features you see in these cross sections._ <br> _b. Can you identify any changes between occupations?_ <br> _Suggestion: try plotting the difference between 2012 and 2004, or 2004 and 1995. Is this of any help?_ <br> _Spoiler: the plot above is not easy to understand! There will be a number of small scale features, specially at the surface and some "stripey" patterns throughout the water column. Remember that these hydrographic surveys represent a snapshot in time. These snapshots include eddies, meanders and other types of high frequency variability in the ocean that would average out if we were taking a long enough period._
 - **Question 2:** <br> _Repeat the interpolation for practical salinity and oxygen, and make a figure with three panels (one for temperature, one for salinity and one for oxygen)._
 - **Question 3**: <br> _a. Using gsw calculate conservative temperature and absolute salinity for I09S. You can look at the 2_Multiple_CTDs.ipynb for guidance. Plot them in a figure with two panels._ <br> _b. Merge the temperature, practical salinity, conservative temperature, absolute salinity and oxygen dataarrays into one dataset, and save using the `.to_netcdf(path_to_save/name.nc)` function. You can compare your saved file to `data/I09S_2024.nc` to verify it was done correctly. Don't forget the attributes and metadata! It is good practice to document your datasets thoroughly._

#### Antarctic Bottom Water contraction

 - **Question 1**: <br> _How would you calculate a distance between two longitude points instead?_
 - **Question 2**: <br> _Notice how the areas decrease with depth. Why do you think that's the case? Remember that in the original dataset, we have a uniform pressure dimension, with data every 10 dBar._
 - **Question 3**: <br> _Use the code above, specifically the `AABW_layer_mask` to calculate the average temperature, salinity and oxygen in the AABW layer. Plot these three together with the area of the layer in the same figure, with four different panels._ <br> _You can use [CoPilot](https://copilot.microsoft.com/) to help you!_ <br> _Try to get the following figure._
 - **Question 4**: <br> _Repeat the calculations for the basin north of the ridge (our `I09S_north_basin`). This time, you are going to have to create a different mask. Think about the following questions:_ <br> _How are the changes different from the southern basin? Look at the magnitudes!_ <br> _What do you think these differences are attributed to?_
</details>


<details>
<summary> Class 3: Gridded data (EN422) </summary>

#### Introduction to EN422

 - **Question 1**: <br> _a. What are the little wiggles in the data?_ <br> _b. What's behind the big increase around 2005?_
 - **Question 2**: <br> _a. Using the number of profiles per month since 1970, can you find out which month of the year has the most observations and which the least?_ <br> _b. Discuss what preccautions you would take when using the EN4.2.2. dataset._ <br> _c. What other important information/dimension of the observations assimilated we have we not explored?_
 - **Question 3**: <br> _There's something strange happening in the land in the plots above. Can you see what it is? Fix it!_
 - **Question 4**: <br> _Can you make this plot a bit nicer? Shrink the colorbars, add labels and a title? Choose appropriate ranges for the colorbar to better visualize the changes._
 - **Question 5**: <br> _Now plot the zonal average of the change between the last and first decade of the product, like when we plotted our `temp_zonal_ave`._ <br> _Use an appropriate colorbar - usually when plotting a difference or an anomaly, we choose a "diverging" colorbar, where the zero tends to white, and positive and negative values have different colors._
 - **Question 6**: <br> _Describe the changes that you can see in the spatial maps and the depth vs year plots._ <br> _Can you think of other ways of visualising changes?_
 - **Question 7**: <br> _Can you calculate density using the gsw library? Repeat the plots we have done with temperature and salinity and describe the changes you observe._

#### Calculating trends

 - **Question 1**: <br> _There is significant cooling of the temperatures at the surface in the Southern Ocean around the Antarctic continental margin. Does this surprise you? Do you have any ideas as to what might be happening?_ <br> _Compute surface salinity trends as well to complement your discussion._
 - **Question 2**: <br> _Look at the Antarctic margins. They look very patchy! Why do you think that is?_
 - **Question 3**: <br> _Calculate bottom salinity trends and discuss the results._ <br> _Tip: you can use the same bottom_level we used for temperature._
 - **Question 4**: <br> _Repeat the analysis for salinity and discuss the observed trends._
</details>
