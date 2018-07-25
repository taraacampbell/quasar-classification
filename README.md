# Quasar Classification

## Description:
Preliminary quasar classification based on light curve properties [not done with packaged classification algorithms]. A model for quasar candidates was made using the SDSS quasar catalog and the Massive Astrophysical Compact Halo Object (MACHO) database, then applied to the  All SKy Automated Survey (ASAS). Done for an undergraduate course (Research Methods in Astrophysics - Yale University Oct-Dec 2017)

## Background:
Quasars are characterized as galaxies with Active Galactic Nuclei (AGNs) at their centers, emitting high amounts of energy. Their light is variable in nature, with a strong correlation to the “damped random walk” model. By creating an algorithm to look for this specific kind variability, quasar candidates can be identified for further spectral analysis. Using techniques similar to supervised machine learning, previous data was used to build a classification system for any given light curve. This analysis builds off of previous work using similar techniques, with guidance from papers like Geha et al. (2003), and Ivezić, Ž., & Macleod, C. (2013).

This work was modeled off of a paper, Variability-selected Quasars in MACHO Project Magellanic Cloud Fields (Geha et. al 2003). The paper created a model for the light curve profile of quasars and applied it to the MACHO databade to discover quasars in the Magellanic Clouds.

## Methodology:
Using the SDSS catalog, I created a very rough model for the light curve profile of a quasar. Qualifications were as follows:
  - Periodicity of the source, using the Lomb Scargle method.
    Lomb Scargle estimates the best fit frequency of a data set using a least squares fit of a sinusoid. To determine how good a given frequency fits the data, a power is assigned. Curves with powers greater than 0.35 were removed.
  - Variation of the source.
    A maximum and a minimum threshold was determined, using chi-squared statistics to test for statistically significant deviation from a straight line
