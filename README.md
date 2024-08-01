# AD diagnosis
Diagnosis of Alzheimer's Disease by Integrating Multilayer Information from Plasma Cell-Free RNA Sequencing Data
===

Environment
---
Windows 10  
python 4.2.0  
randomForest package 4.7.1.1  

Usage
---
1.After preparing the data files, you can follow our analysis workflow in the project and utilize the Random_forest.RData file located in our model folder. Note: The first column of the data file should be designated as the sample ID column, the second column as the class column, and the subsequent columns serve as feature data columns. Specific adjustments can be made according to individual circumstances.  

2.Upon successfully running Random_forest.RData, you will obtain several ROC curve images in the directory, the number of which depends on the quantity of data files fed into the process.  

Citation
---
`Ma R, Lu L, Li Q, He C & Zhou X. "Diagnosis of Alzheimer's Disease by Integrating Multilayer Information from Plasma Cell-Free RNA Sequencing Data". In preparation.  `

License
---
For academic research, please refer to MIT license.  
For commerical usage, please contact the authors.

Content of the project
---
In __Data processing__, the implementation process for feature extraction and selection of three types of data - RNA, SNP loci, and microorganisms - is outlined.  

In __Differential expression__, the primary objective is to provide insights into the distinct expression characteristics of individual features (such as genes or transcripts) across different conditions or groups. Additionally, this analysis includes the implementation process for generating corresponding volcano plots, which visually represent the statistical significance of the expression changes and the magnitude of these changes.  

In __Enrichment analysis and pathway expression__, the implementation process for GO (Gene Ontology) analysis and pathway expression analysis is outlined for three types of RNA feature data.  

In __Functional annotation__, the process for annotating the functional roles of microbial data is presented, along with the implementation steps for generating figures such as mean_proportions_AD and mean_proportions_NCI, which likely depict the mean proportions of microbial features (e.g., taxa or gene functions) in different conditions or groups, such as AD (a hypothetical disease condition) and NCI (Non-Clinical Individuals or a control group).  

In __Microbial experiment__, the relevant implementation process for microbial data analysis is outlined, encompassing two primary experiments: the Microbial_contribution_rate_experiment, which assesses the contribution rate of microbial components, and the Randomization_MicrobialComplementaryEffectExperiment, which evaluates the predictive performance complementarity effect among microbial features.  

In __model__, the implementation process of our constructed models is detailed. Specifically, it includes:  
>__Random Forest _ Cross validationR__: A model is built in R using an 80% training set and a 20% validation set for cross-validation purposes.  
>__Random_forest__: Another Random Forest model is constructed based on the article's specified 120 samples for the training set and 208 samples for the validation set.  
>__Random_forest_CDR_MMSE__: Building upon the Random Forest model, CDR (Clinical Dementia Rating) and MMSE (Mini-Mental State Examination) indicators are incorporated to further validate and enhance the model's predictive performance.  
>__Spearman_correlation_analysis_of_CDR_MMSE__: This analysis examines the individual Spearman correlation of CDR and MMSE indicators, providing insights into the strength and direction of the relationship between these two measures.  
