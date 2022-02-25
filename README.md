# Polaris Project 2022: Characterizing a Non-Interacting Black Hole Candidate

## Project Goals

We are interested in studying black holes to learn more about the late stage evolution of massive stars and the underlying properties of compact objects. There are more than 10^8 black holes in the Milky Way, but only a few dozen have been observed. 

The majority of stellar mass black holes are detected in X-ray binary systems or in gravitational wave mergers, but these systems represent a small fraction of possible binary configurations. Most black holes will be isolated or in non-interacting systems. Detecting these systems is difficult, since the black holes are electromagnetically dark, but not impossible. In this project we will work with radial velocity data and photometric data of a red giant star to determine the nature of its binary companion!

## Data Files

There are two data files in this git repo we will need:

The 'kelt_clipped' file gives the magnitude of the giant star on different [helocentric julian days](https://en.wikipedia.org/wiki/Heliocentric_Julian_Day). See below for a description of the magnitude system. [KELT](https://keltsurvey.org/) is a survey telescope mission designed to search for exoplanet transits by monitoring millions of bright stars over ~daily cadence. We don't have any planets here, but we can use KELT to search for signals of ellipsoidal variability. 

The 'stellar_rv' file gives the radial velocity (in km/s) of the star on different barycentric julian days. The third column gives the error on the RV measurements.

## Background papers/articles

* [TAT-1 press release](https://news.osu.edu/scientists-may-just-have-discovered-a-new-class-of-black-holes/)
* [LIGO mass plot](https://media.ligo.northwestern.edu/gallery/mass-plot)
* [RV method video](https://www.youtube.com/watch?v=sJ45Gb99KII) -- except we have a black hole instead of a planet
* [Description of magnitude system](http://www.astronomynotes.com/starprop/s4.htm)
* [Core Collapse Supernovae](https://astronomy.swin.edu.au/cosmos/c/core-collapse)
* [The Black Hole Mass Distribution in The Galaxy (Ozel 2010)](https://ui.adsabs.harvard.edu/abs/2010ApJ...725.1918O/abstract) -- focus on sections 1 and 2
* [A Unicorn in Monoceros (Jayasinghe 2021)](https://ui.adsabs.harvard.edu/abs/2021MNRAS.504.2577J/abstract)
* [An Isolated Mass Gap Black Hole (Lam 2022)](https://ui.adsabs.harvard.edu/abs/2022arXiv220201903L/abstract)
* [High Tide: A Systematic Search for Ellipsoidal Variables (me lol)](https://ui.adsabs.harvard.edu/abs/2021MNRAS.507..104R/abstract)
* [Islands of BH formation](http://www.astroexplorer.org/details/apj522871f13)
* [Periodogram background and examples](https://online.stat.psu.edu/stat510/lesson/6/6.1)
* [Understanding the LS periodogram](https://iopscience.iop.org/article/10.3847/1538-4365/aab766)

## Python Tools

The most important packages for this project will be [astropy](https://www.astropy.org/), [pandas](https://pandas.pydata.org/docs/), [numpy](https://pandas.pydata.org/docs/), and [matplotlib](https://matplotlib.org/stable/api/index)

Some notes on these:
* For astropy we are primarily going to use the [Lomb Scargle Periodogram](https://docs.astropy.org/en/stable/timeseries/lombscargle.html) class. This documentation runs through the basic setup and execution steps to get a period estimate from time-series data
* We will use pandas to load in our RV/light curve data as a "dataframe" and do various calculations. There are tons of resources for this online, and the package is very google-able. The first two lessons of [this tutorial](https://bitbucket.org/hrojas/learn-pandas/src/master/) are a good starting point. I've also added a jupyter notebook showing and example of how I have used pandas for my work. 
* Matplotlib is a great for making quick plots but can also make high-quality poster/publication level plots. We will look into this more when we make our poster. 

[Python Cheat Sheets](https://ehmatthes.github.io/pcc_2e/cheat_sheets/cheat_sheets/)

## Reading Scientific Papers

Section 3 of [Cooke et al. (2020)](https://arxiv.org/abs/2006.12566) describes the questions one should try to answer while reading a paper:
* What is the specific problem this paper is investigating?
* To address this problem what did they observe and what specifically are they measuring?
* What was the primary result of their observations and how are these results novel?

Three part astrobites piece on [Tools for Reading Papers](https://astrobites.org/2017/12/19/tools-for-reading-papers-part-1/)

[More astrobites tips](https://astrobites.org/2011/04/19/journal-articles-in-astronomy/)

[How to (seriously) read a scientific paper](https://www.science.org/content/article/how-seriously-read-scientific-paper)

# February 14
* Background on why we care about non-interacting black holes
* TAT-1 press release
* LIGO mass plot
* Intro to pandas, astropy, etc.
* After class:
  * Sections 1 and 2 of Ozel (2010)
  * Read in light curve data (kelt_clipped.csv')
  * If time permits, plot the light curve

# February 21
* Defining orbital phase
* Visualizing system geometry
* Background on fourier analysis and lomb scargle periodogram
* After class:
    * Plot periodogram and select best period

