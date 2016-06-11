---
layout: default
title: Research
permalink: /research
---


# Polar vortex dynamics

<img src="/images/vortex.gif" width="200" style="float:right; margin: 1em 0 4em 2em;"
title="Potential vorticity during the vortex splitting event in December 1984."/>

A polar vortex is a region of strong winds which encircles the pole of Earth and
many other planets with atmospheres. On Earth, the vortex is strongest in the
stratosphere; the region of the atmosphere between about 15-50 km in altitude,
just above where passenger aircraft fly. Occasionally (about 2/3 of winters in
the Northern Hemisphere but very rarely in the Southern Hemisphere), this vortex
can break down in an event called a sudden stratospheric warming (SSW). These
SSWs occur in one of two ways; a displacement of the vortex far away from the
pole, or a splitting of the vortex. Importantly, previous work has suggested
that these events may have significant impacts upon surface weather, such as
increasing the likelihood of cold spells over Northern Europe. The animation to
the right shows a vortex split in December 1984.

I developed a method to objectively identify these split and displacement events
in both observations and models, using a measure called *elliptical diagnostics*
([Seviour *et al.*
2012](http://onlinelibrary.wiley.com/doi/10.1002/grl.50927/abstract)). I then
went on to apply this method to several models in the CMIP5 ensemble, which
entered the last IPCC report ([Seviour *et al.*
2016](http://onlinelibrary.wiley.com/doi/10.1002/2015JD024178/full)). The models
and observations show some consistent differences between vortex splits and
displacements, indicating that the dynamics driving them may be very different.
However, there were also a large discrepancies between models, meaning that
there is lots of work still to be done in order to understand and model these
events.

**Resources**

* I have made animations of 850 K (mid-stratosphere) potential vorticity over
  all winters from 1979-2009.
  [View/download them here.](https://www.dropbox.com/sh/fv2nogjs7m3irly/AADLKFPzbtqpBNQIunl1rAOea?dl=0)
* I have written a python package to calculate moment diagnostics of a polar vortex,
  using either geopotential height or potential vorticity.
  [See the Github repository](https://github.com/wseviour/vortex-moments) for
  more details.


# Seasonal prediction

<img src="/images/seasonal_prediction.png" width="300" style="float:right;
margin: 1em 0 4em 2em;" title="GloSea5 prediction of zonal-mean zonal wind at
60S, 10hPa. Grey lines show individual ensemble members, and the black line
shows observations."/>

Seasonal predictions aim to forecast the average weather conditions from several
weeks to months ahead of time. There has been rapid progress in this field over
the past few years, and the first skillful forecasts are now starting to be
seen. Working with the [UK Met Office Seasonal Prediction
Group](http://www.metoffice.gov.uk/research/climate/seasonal-to-decadal/seasonal-prediction),
I analysed their latest seasonal prediction system,
[GloSea5.](http://www.metoffice.gov.uk/research/climate/seasonal-to-decadal/gpc-outlooks/user-guide/technical-glosea5),
This system has much higher vertical resolution than previous seasonal
forecasting systems, and I was interested in whether this increased resolution
improves the skill of the forecast.

We showed ([Seviour *et al.*
2014](http://journals.ametsoc.org/doi/abs/10.1175/JCLI-D-14-00264.1)) that the
increased resolution in the stratosphere does not add much to the skill in the
Northern Hemisphere, but it has a significant effect in the Southern Hemisphere,
where timescales for stratospheric variability are much longer. This allowed the
model to make the first skillful seasonal prediction of the Southern Annular
Mode - the dominant mode of atmospheric variability over the Southern
Hemisphere.


# Ozone and the Southern Ocean

I am investigating the effect of ozone depletion on the climate of the Southern
Ocean and Antarctica as part of the [Ozone and Climate
Project.](https://ozoneandclimate.squarespace.com/). Ozone depletion, and the
formation of the ozone hole, has been one of the largest anthropogenic changes
to the Earth's climate system. The effects of ozone depletion are greatest in
the ozone layer (mid and lower-stratosphere), but significant impacts have also
been detected on surface weather over the Southern Hemisphere.

My research has aimed to address what role ozone depletion may have played in
driving observed climate trends over the Southern Ocean. One such trend is an
overall increase in Antarctic sea ice over the past three decades, a feature
which most climate model simulations do not capture. I have run a series of
climate model simulations with the [GFDL ESM2M
model](http://www.gfdl.noaa.gov/earth-system-model) in order to better
understand the role of ozone depletion in this trend.


# Brewer-Dobson circulation

The Brewer-Dobson circulation is the large-scale meridional circulation of the
stratosphere, with air rising in the tropics, moving poleward, and descending in
the extra-tropics. This circulation plays a crucial role in setting the
distributions of ozone and water vapour within the stratosphere, but is very
difficult to diagnose directly from observations. We calculated the
Brewer-Dobson circulation from the (then) new reanalysis data set,
[ERA-Interim](http://www.ecmwf.int/en/research/climate-reanalysis/era-interim)
([Seviour *et al.*
2012](http://onlinelibrary.wiley.com/doi/10.1002/qj.966/abstract)). We analysed
the structure of the circulation, and the factors driving it, in greater detail
than was previously possible.

**Resources**

* The transformed Eulerian mean diagnostics calculated in Seviour *et al.*
  (2012) are available to download [here](https://www.dropbox.com/s/p8k2x54msq2n4nc/TEMdiags_era-int_1979-2010.nc?dl=0).
