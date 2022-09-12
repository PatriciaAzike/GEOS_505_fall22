# GEOS 505: Research Computing in the Earth and Environmental Sciences

## Patricia Azike

# Brief overview of my research: Data-enabled modeling of wildfire smoke transport

Wildfires are unexpected fires that start in rural or urban regions and can last long over a vast land area. Out of all the wildfire emissions, most studies are chiefly concerned with accurately estimating concentrations of fine particulate matter with a diameter of 2.5 micrometers, commonly known as PM2.5 because of its aggravating health impacts. It can easily flow to the respiratory and circulatory systems since it is tiny, causing breathing complications, cardiovascular morbidity, neonatal defects, and sometimes death in sensitive groups.

Wildfires are a common natural disaster in many parts of the world, especially the Western United States, Australia, and Siberia. In the United States, California is famous for its wildfires, with the largest fire since 1932 being the August Complex fire of 2020, said to be caused by lightning and recorded to have burned over a million acres.

The effects of smoke vary over temporal and spatial scales; hence several models have been built to simulate its past and present behavior, predict its impacts, and also make regulatory decisions in smoke management. Most of these models often focus on one or several aspects of the underlying physics of wildfires, such as the emissions source term,  the effects of wind on the dispersion of smoke particles, the height of the plume, rate of heat release, temperature inversion, mixing height/depth, and concentration of particulate matter. The emissions source is a significant factor to consider in the transport of smoke, as it plays a massive role in estimating the concentration of smoke effluents such as particulate matter. In general, it is simply any forcing that causes smoke to be injected into the atmosphere. Some models go further to include the chemical changes that occur as the gases are emitted and are vital for addressing a variety of air quality concerns, including ozone generation. 

However, there are multiple challenges found in modeling smoke transport, but the most prevalent, as we observed while going through the seed papers, are issues encountered while attempting to estimate the emissions source term. The start of a fire is usually spontaneous or random, so it is difficult to quantify it adequately. This difficulty led the researchers to make assumptions to evaluate the rate at which the effluents are dispersed. Other challenges include the inadequate description of models by researchers, and the absence of one go-to model that can be used to estimate the emissions source. It is also difficult to procure data, and the large areas over which wildfires spread put a constrain on computational resources since not all locations on the physical domain have smoke.

To counter these challenges, we propose the implementation of Smoke3d, a software framework that employs conservative numerical schemes, which ensures the accuracy of predictions. Smoke3d is a stand-alone application of [ForestClaw](https://github.com/ForestClaw/ForestClaw/wiki), a suite for solving hyperbolic partial differential equations. It is computationally cost-effective as it makes use of adaptive mesh refinement (AMR), thereby targeting only areas with smoke on the physically domain. We are currently testing how different source term functions affect the transport of smoke and impact PM2.5 concentrations, by specifying guages, which are akin to locations influenced by smoke, and using a nonlinear least squares solver to estimate the parameters of the source term based on the output of the guages and measure the L2 error. To do this, we runForestClaw as a black-box forward solver using a Python frontend script with input parameters (both observed and starting values) to enable parameter estimation based on the output of the gauges. 


# Goals for the semester

1. Take my comprehensive examination and focus more on my research
1. Sharpen my programming and computing skills to a certain level of competency by the end of the semester.
2. Dare myself by undertaking projects beyond the scope of the class
3. Use the knowledge gained from the class to build a "dashboard" or site or something that accurately predicts smoke transport in Idaho
4. Set aside at least 3 hrs each week to practice what I have learned

