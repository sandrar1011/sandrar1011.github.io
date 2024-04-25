# Affordable Housing and Transportation Insecurity
by Sandra Romero

I am interested in exploring the kinds of facilities (walking and transit) are in proximity of the pipeline of affordable housing projects in Los Angeles. I would like to incorporate LA Metro GTFS data to add bus and train routes. I am mostly basing my projects around the LAHD Affordable Housing Project List and seeing what data can be tied to the area surrounding the sites. Through the data I am curious to see the trends, are projects mostly in census tracts with high transportation access? Are they in already dense areas? The current data sets are the: 2021 Walk and Bike Counts https://data.lacity.org/dataset/2021-Walk-Bike-Count/9tzi-nz7g/about_data LAHD Affordable Housing Project List https://data.lacity.org/Housing-and-Real-Estate/LAHD-Affordable-Housing-Projects-List-2003-to-Pres/mymu-zi3s/about_data Transportation Index https://geohub.lacity.org/datasets/lahub::transportation-index/about Vision Zero Prioritized Corridors https://geohub.lacity.org/datasets/ladot::vision-zero-prioritized-corridors/about

import pandas as pd
import json    
import requests
import pprint
import numpy as np
pp = pprint.PrettyPrinter
!pip install geopandas
import geopandas as gpd
pd.set_option('display.max_columns', None)
!pip install contextily
import contextily as cx
from scipy.stats import pearsonr
from datetime import datetime
import seaborn as sns
import matplotlib.pyplot as plt
import geopandas as gpd
import os
from mapboxgl.utils import *
from mapboxgl.viz import *
from census import Census
from us import states

import statsmodels.api as sm
from statsmodels.stats.outliers_influence import variance_inflation_factor ### VIF package
from stargazer.stargazer import Stargazer

import warnings; warnings.simplefilter('ignore')
