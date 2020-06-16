# Random Forest Classifier for Exoplanet Features
Ana Lam

# Introduction

Astronomers use many fundamental parameters to characterize exoplanets. The NASA exoplanet archive includes and classifies planets that meet the following criteria:
* Mass is < 30 Jupiter masses
* The planet is not free floating
* Has undergone validation checks so that false positivity is unlikely
* The above along with additional physical properties are published in peer-reviewed publications

The majority of the confirmed exoplanets, however, do not have extracted observables  for each of the parameters. Therefore, it is of great interest to estimate these missing parameters. One way of estimating parameters, is by examining the relations between several different parameters.

In 2019, [Ulmer-Moll et al.](https://www.aanda.org/articles/aa/abs/2019/10/aa36049-19/aa36049-19.html) conduted a examination of the mass-radius relation in exoplanets using random forests, a machine learning algorithm, to compute estimated radii from known mass observables from exoplanets. In this project, I will be using the random forests method to examine radius relations with different physical properties and conduct a feature importance test to determine the relation I will use to compute estimated radii.

# Results

After implementing the random forest classifier, I was able to investigate the importance of each feature in determing the radius value. Since mass was the most significant feature, I deduced that mass and radius have the strongest correlation, which is the same result that Ulmer et al. found.
I decided to fit a linear regression to the mass-radius relation because of the frequent result of null radius data in the classified planets table.
I did have some trouble analyzing the accuracy of the linear regression probably because I probably mixed up the raw data and the logarithmic data.
