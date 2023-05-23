# Final-Project-Sta440: Analysis of Fishery Data froM Gulf of Alaska Bottom Trawl Survey.

Environmental modeling is becoming increasingly important as climate change increases in
severity, as businesses, scientists, and the policymakers need to be able to quickly react to
changes in species’ population. For my individual project, we intend to try to tackle this topic
using methods in the spatiotemporal modeling literature, as well as try to find relationships
between the covariates, species abundance, and key metrics of animal welfare in the Alaskan
Gulf region.

The data we will be working with in this case study is the Alaskan Fishery Science Center’s
Groundfish and Crab Assessment Program (GAP), specifically surveys of populations on the
bottom of the Alaskan Gulf. The dataset that we will be working with during this project is
from the National Oceanic and Atmospheric Administration (NOAA) website, which contains
survey data over the years 1993-2021. The data was collected via a process called bottom
trawling, where researchers drag a large net across the bottom of the ocean floor to capture
ground fish, crabs, and other crustaceans in order to assess their population. In this report,
we will be specifically addressing a particular type of cod named the walleye pollock, as it is
one of the most sustainably managed and economically valuable species to Alaska.

In this project, we have two main aims:

Aim 1: How can we best predict CPUE (Catch per unit effort) for the walleye pollock across both
spatial and temporal dimensions in the Gulf of Alaska, and what will happen to
the population in the near future?

Since CPUE is supposed to be proportional to abundance, it is of value for an organization
like NOAA to be able to predict CPUE in order to predict fish abundance. Surveys like the
GOA Bottom Trawl Survey are expensive and time consuming to conduct; additionally, they
only occur biannually. It would be useful for NOAA to be able to predict CPUE into the
future for different locations, so that between surveys, fisheries will have a good estimate of
what their population looks like. This is the major goal of this report, and it will be assessed
by comparing a zero-inflated generalized linear model (GLM) to a specific fishery model VAST
(Vector Autoregressive Spatiotemporal model), and then predicting abundance from the model
that performs the best.

Aim 2: How do different covariates present in the dataset predict CPUE?
It is also of use to understand how different variables affect CPUE, as without controlling for
other effects on the CPUE, CPUE is not directly proportional to population abundance. For
example, suppose we were interested in the population of a particular kind of surface fish; if
all of our samples consisted of depths in the deep sea, we would expect to catch no fish on
the surface. This would result in a near 0 CPUE, which would be not at all proportional to
the abundance of our target species. (Mark N. Maunder 2006) gives many more situations
in which the CPUE may give an inaccurate estimate of species abundance, such as using the
wrong kind of hook/net, seasonality, and shifting water temperatures, to name a few.
Thus, it is of value to try to understand how different covariates impact the CPUE in our
model in order to try to get a more accurate estimation of species abundance over time and
space. This will be assessed by comparing our best model to a model with no covariates to
see how much more of our variance is explained by adding our covariates of interest.

The answers to these aims, along with the methodology used, further description of the data, 
and figures, can be found in the full report in Final__Report.pdf. The code can be found in
Final_Report_with_code.qmd.
