# **Survival Analysis and Seed Germination**

## Description  

This repository shows how to analyse seed germination data through a time-to-event approach, using a data set of seeds of *Ipomoea hederacea* (Convolvulaceae). The analysis is part of an assessment of inbreeding depression in this species carried out in a population in the State of Veracruz (Mexico) during 2012 and 2013. You can find the related paper in this [link](http s://www.researchgate.net/publication/356285929_A_test_of_the_reproductive_assurance_hypothesis_in_Ipomoea_hederacea_does_inbreeding_depression_counteract_the_benefits_of_self-pollination).  

## Repository structure  

**I.** The first section explain the objective of the analysis and the structure of the data to be analysed.    

**II.** The second part shows how to fit a parametric Cure Model following [Onofri *et al*. 2011](https://www.researchgate.net/publication/216320776_The_cure_model_An_improved_way_to_describe_seed_germination).    

 
## I. Survival analysis

This approach consists of the analysis of the time it takes for events to occur. The data consist in a set of individuals that are followed until the event of interest occurs (germination of the seeds in this case). Because the study design include only a short interval of time to evaluate if the event occurs, the data analysed here corresponds to [**censored data**](https://www.nature.com/articles/6601118), *i.e.* not all seeds had germinated by the time the monitoring period was over.   
The objective is to evaluate the number of days seeds took to germinate through a survival analysis ([Clark *et al*., 2003](https://www.nature.com/articles/6601118); [Onofri *et al*., 2010](https://www.researchgate.net/publication/227892810_A_new_method_for_the_analysis_of_germination_and_emergence_data_of_weed_species)), by fitting **cure models** to test for differences in germination times between pollination treatments per year ([Onofri *et al*., 2011](https://www.researchgate.net/publication/216320776_The_cure_model_An_improved_way_to_describe_seed_germination)). 

The complete data set of the study is available through [Zenodo](https://zenodo.org/record/5091713). For this repository only the file **Germination_ID.csv** is used. The file includes the identity of the plants and the fruits, the seeds weight, and the day of germination. The seeds were obtained after the application of the following experiments in 38 plants:  

* Hand-self pollination: flowers were manually pollinated with pollen from the two longest anthers of the flower.

* Hand-cross pollination: emasculated flowers were manually pollinated with pollen obtained from the two longest anthers of two-three donor plants.  

### Seed data  

germination <- read.csv("https://zenodo.org/record/5091713/files/Germination_ID.csv?download=1")
head(germination)

## II. Cure Model

The file [CureModel.Rmd](https://github.com/REDD1326/SurvivalAnalysis_SeedGermination/vignettes/CureModel.Rmd) shows how to fit a Cure Model and how to plot the survival curves to graphical comparison between observed and predicted values. 

