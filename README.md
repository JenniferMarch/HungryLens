# Hungry Lens Analyses

This is the repository where I am storing the data and code used to generate **1 behavioural** and **(2) modeling** analyses for the preprint: https://osf.io/preprints/psyarxiv/wvfnb 

## 1 Behavioual Analyses

All analyses are carried out in R using RMarkdown. The analyses are structured using the suffix A_ to F_ and at the beginning of each file are futher information about the analyses. 

**Note 1:**  To run A_Preprocess_Food.Rmd the original .csv files are needed, which can be requested from jennifer.march@uni-hamburg.de
A_Preprocess_Food.Rmd creates two .RData files which are used for all subsequent behavioural and modeling analyses: *food_data.RData* and *food_modeling_data.RData*

**Note 2:** C1_GLMMs_Food.Rmd takes quiet long as the function compares the best fitting GLMM given various (combination of) predictors. C2_GLMMs_fast.Rmd merely implements the best model as obtained from C1_GLMMs_Food.Rmd

## 2 Modeling Analyses

**Requirements:** JAGS, dwiener

All analyses are carried out in R using RMarkdown and JAGS (see Folder BayesModels). The analyses are named after the respective model, except for the preprocessing, which essentially transforms the food_modeling_data.RData into the the files 
*data_prep.RData* and *data_prep_want.RData* used for all taste and wanting analyses. At the beginning of each file are futher information about the analyses. 


### Recommended Folder Structure
*…to speed up reproducibility*

1.	Create folder (e.g. “modeling analysis”)
2.	Create R.proj for this folder 
3.	Copy data file “data_prep.RData” into folder 
4.	Copy all modeling scripts (.Rmd files) into folder
5.	Dowload Folder “BayesModels” (.txt files for the modeling in JAGS) and copy into folder, such that “BayesModels” is a folder in the folder “modeling analyses”
**Note** If you rename the folder BayesModels, or the models in that folder, you have to rename them when calling the models in the .Rmd files!
6.	Run analyses!


