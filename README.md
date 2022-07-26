# **Survival Analysis for Seed Germination**

Survival analysis approach consists of the analysis of the time it takes for **events** to occur. The data consist in a set of individuals that are followed until the event of interest occurs. This repository shows how to analyse seed germination (**event**) data through a time-to-event approach, using a data set of seeds of *Ipomoea hederacea* (Convolvulaceae). The analysis is part of an assessment of inbreeding depression in this species carried out in a population in the State of Veracruz (Mexico) during 2012 and 2013 ([Delgado-Dávila and Martén-Rodríguez, 2021](https://www.researchgate.net/publication/356285929_A_test_of_the_reproductive_assurance_hypothesis_in_Ipomoea_hederacea_does_inbreeding_depression_counteract_the_benefits_of_self-pollination)).  

Because the study design include only a short interval of time to evaluate if the event occurs, the data analysed here corresponds to [**censored data**](https://www.nature.com/articles/6601118), *i.e.* not all seeds had germinated by the time the monitoring period was over.  

## Objective 

The objective is to evaluate the number of days seeds took to germinate through a survival analysis ([Clark *et al*., 2003](https://www.nature.com/articles/6601118); [Onofri *et al*., 2010](https://www.researchgate.net/publication/227892810_A_new_method_for_the_analysis_of_germination_and_emergence_data_of_weed_species)), by fitting **cure models** to test for differences in germination times between pollination treatments per year ([Onofri *et al*., 2011](https://www.researchgate.net/publication/216320776_The_cure_model_An_improved_way_to_describe_seed_germination)). 

## Seed data

The complete data set of the study is available through [Zenodo](https://zenodo.org/record/5091713). For this repository only the file **Germination_ID.csv** is used. The file includes the identity of the plants and the fruits, the seeds weight, and the day of germination. The seeds were obtained after the application of the following pollination experiments in 38 plants:  

* Hand-self pollination (HSP): flowers were manually pollinated with pollen from the two longest anthers of the flower.

* Hand-cross pollination (HCP): emasculated flowers were manually pollinated with pollen obtained from the two longest anthers of two-three donor plants.  

## Cure model

The file [CureModel.Rmd](https://github.com/REDD1326/SurvivalAnalysis_SeedGermination/vignettes/CureModel.Rmd) shows how to fit a parametric Cure Model following [Onofri *et al*. 2011](https://www.researchgate.net/publication/216320776_The_cure_model_An_improved_way_to_describe_seed_germination), using the R package ```flexsurvcure``` (Amdahl, 2017). The file also shows how to plot the survival curves to graphical comparison between observed and predicted values. 

