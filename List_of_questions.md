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

<details>
<summary> Class 4: Satellite observations </summary>

#### Introduction to satellite altimetry

 - **Question 1**: <br> _Identify in the zonal mean plot above the regions that correspond to the gyre circulation and the Antarctic Circumpolar Current. What is the logic behind your identification? Which region would have a stronger circulation?_
 - **Question 2**: <br> _In the figure above, red colours represent regions where that season's sea level is higher than the mean, and blue regions where it is lower than the mean. Notice how around the Antarctic margins there is a sort of "see-saw" pattern to the changes: when sea level goes down close to the coast like in DJF and to a lesser extent SON, further north it goes up!_ <br> _Taking this into account, what do you think the above changes in sea level throughout the seasons impact the the surface circulation? Little help: during MAM the surface circulation around the Antarctic margins speeds up! Why? Describe other changes._

#### SO circulation from geostrophy

I have calculated the velocities here, but have purposefully inverted the sign so that the flow goes the other way around, leaving higher SLAs to the right. Ideally they would figure this out and fix it in question 2. It might take ages, or be too much, in which case the notebook can be easily made correct :) 

 - **Question 1**: <br> _What do you expect this plot to be like? How are the vectors and the contours of adt going to be with respect to each other?_
 - **Question 2**: <br> _How does the circulation here compare to your expectations after the discussion on Question 1? To help you answer this, you can plot an even smaller regions to better visualise contours and vectors._ <br> _Spoiler: there is something not quite right. Once you've found it, fix it!_
 - **Question 3**: <br> _Where do you see strongest currents? Looking at the sea surface height, can you explain why the currents are strongest there?_

</details>

<details>
<summary> Class 6: Meridional Overturning Circulation </summary>

#### Meridional Overturning Circulation

 - **Question 1**: <br> _Using the same logic, explain the direction of the transport between the diamond and the star._
 - **Question 2**: <br> _With this knowledge, coming back to the circumpolar map, explain what the circulation looks like from the streamfunction._
 - **Question 3**: <br> _What's the direction of the transport in the abyssal cell?_
 - **Question 4**: <br> _[Donohue et al. (2016)](https://agupubs.onlinelibrary.wiley.com/doi/full/10.1002/2016GL070319) estimated the mean Drake Passage transport to be 173.3 Sv. How does that compare to our estimate?_
 - **Question 5**: <br> _The Ross Gyre is the other subpolar gyre in the Southern Ocean, located in the Ross Sea. It is the other area of negative $\psi$ in our circumpolar map. Calculate the seasonal cycle in this gyre's transport._

#### Meridional Overturning Circulation

 - **Question 1**: <br> _Describe the direction of the circulation in each of these areas, remembering that $T_y = \frac{\partial \psi}{\partial z}$. So, as you go deeper, $\partial z$ is negative - look at the sign of $\partial \psi$. Can you identify the abyssal cell? There is something strange... can you identify what it is?_
 - **Question 2**: <br> _Describe the circulation in the plot above, and associated water masses._
 - **Question 3**: <br> _Using the methods in `1_Transport_streamfunction.ipynb`, calculate the strength of the abyssal cell of the MOC, using the streamfunction in density coordinates. Compare the strength between the streamfunction with and without eddies._


</details>

<details>
<summary> Class 7: End of Century simulations </summary>

#### Future changes model experiment

 - **Question 1**: <br> _What variables are included in our forcing field files?_
 - **Question 2**: <br> _There is something wrong in our plots. Correct it._
 - **Question 3**: <br> _What do you think the changes to incoming longwave radiation are due to? How are these and the surface temperature changes related?_
 - **Question 4**: <br> _Using the plots above, summarise the changes applied to the forcing fields used to run the perturbation experiments. Remember that the changes are representative of future projections for a SSP585 scenario in CMIP6 models._
 - **Question 5**: <br> _We have looked at the changes in the time mean forcing fields. Explore the seasonality of the changes. For example:_ <br> - _Compare changes in wind strength changes between summer and winter._ <br> - _Surface temperatures - are they changing more in a given season?_ <br> - _Same with precipitation._

#### Future changes Southern Ocean

 - **Question 1**: <br> _Discuss, given the changes to the forcing fields, what would you expect to see happen to the ocean's circulation, stratification, temperature/salinity structure, etc. Don't be afraid to speculate._
 - **Question 2**: <br> _What variables do we have available?_
 - **Question 3**: <br> _Calculate the changes in temperature and salinity at ~500m depth, which is the depth at which Circumpolar Deep Water sits in the water column. Discuss the resulting plots._
 - **Question 4**: <br> _What has happened to the ASC in the perturbation simulation? Is it stronger or weaker than CONTROL?_
 - **Question 5**: <br> _This one is a bit more tricky: identify the bottom-intensified ASC, and describe what has happened in the perturbation experiment._
 - **Question 5**: <br> _Plot the same thing, but for the warm shelf regime (reversed ASC)._


</details>

<details>
<summary> Class 8: End of Century simulations (continued) </summary>

#### The effect of meltwater

 - **Question 1**: <br> _Using the figures from last class, discuss the changes that you observe in these simulations. How do they differ/not differ from the simulations without meltwater?_

#### Isolating the effect of meltwater

 - **Question 1**: <br> _This is the change to the DP transport due only to meltwater. How does it compare to the changes in the two indvidual simulations from last class? What's the relationship between them?_
 - **Question 2**: <br> _Similar to the Drake Passage transport, this represents the change in the strength of the MOC due to meltwater only. How does it compare to the strength of the individual simulations?_
 - **Question 3**: <br> _Discuss the changes to teh ASC due to meltwater only. Look at, what was in the CONTROL, a bottom-intensified area. Do you think it still belongs to the same regime?_

</details>
