# Modeling within-lineage evolution as a consequence of changes in the adaptive landscape across short and long timescales

__Article:__ Accepted

__Authors:__ Marion Thaureau<sup>1†</sup> and Kjetil Lysne Voje<sup>1</sup>

__Affiliation:__ <sup>1</sup>Evolution and Paleobiology, Natural History Museum, University of Oslo

__Contact:__ <sup>†</sup>marion.thaureau@nhm.uio.no

__Journal:__ Evolution

__Year:__ 2026  

__Abstract:__ The adaptive landscape has been suggested as a potential conceptual bridge between phenotypic evolution on generational to macroevolutionary timescales. However, this potential remains largely untapped due to a limited understanding of how the adaptive landscape changes across time. We assessed the dynamics of the adaptive landscape across different time intervals by analyzing phenotypic time series using multivariate models of adaptation. First, we examined whether a decrease in river water flow affected the optimal body mass of a salmon population over a few decades. Second, we explored whether temperature changes affected the optimal size of coccoliths in a species of coccolithophore across about a hundred thousand years in the Cretaceous. Finally, we analyzed the extent to which temperature changes affected the optimal shell size in a lineage of planktic foraminiferas over a few million years during the Miocene. We find evidence that evolution induced by changes in the adaptive landscape, driven by environmental change, occurred in the salmon and foraminifera datasets, but we do not detect a causal link between the investigated paleo‑proxies and size changes in the coccolithophore lineage. We argue that applying the same modeling framework to datasets covering different time spans not only offers a promising way to better connect evolutionary processes across timescales but also enables tests of adaptive hypotheses about within-lineage evolution.

__Keywords:__ timeseries, Ornstein-Uhlenbeck process, adaptation-inertia framework, macroevolution, microevolution.

__Info:__ This repository contains scripts and data used for analyses in the publication.


__Files:__ 

_Each following folder contains a subfolder per analyzed dataset: the salmon dataset (data from Jensen et al., 2022), the coccolith dataset (data from Bornemann and Muterlose, 2006), and the foraminifera dataset (data from Hodell and Vayavananda, 1993)._

- _Data –_ This folder contains the phenotypic and environmental time series, their associated metadata, and the EvoTS objects. 

- _Script –_ This folder contains the R and batch (.submit) scripts used for the analyses. Each script is named following the system: dataset_model_iteration(_sp).R, indicating the model(s) and the iterations it corresponds to. Most models required multiple scripts to run 100 iterations more efficiently (i. e., _it1 and _it50 respectively correspond to iterations 1 to 50 and iterations 50 to 100). Some scripts also have duplicates for which we set up starting values obtained from the best model (i. e., _sp when full __A__ matrix and diagonal __Σ__ matrix are parametrized; _sp2 when diagonal __A__ matrix and diagonal __Σ__ matrix are parametrized). This folder also contains the scripts used to produce the tables in the publication.

- _Results –_ The folder contains the results for each script as a text file (named on the same system as the scripts: dataset_model_iteration(_sp).txt) and the result tables as Excel files. The folder _Rdatafiles_ contains files with the results for all runs (dataset_allruns_model_iteration(_sp).Rdata) and the results for the best run (dataset_bestrun_model_iteration(_sp).Rdata) for each model. It also contains the best run of the best model in a separate file called dataset_bestmodel.Rdata.
