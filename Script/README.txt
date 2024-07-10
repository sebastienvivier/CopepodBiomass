# Copepod Biomass Scripts

This repository contains scripts for analyzing copepod biomass data. Follow the instructions below to recreate the necessary environment and run the scripts.

## Prerequisites

Ensure you have Anaconda or Miniconda installed on your machine. You can download and install Anaconda from [this link](https://www.anaconda.com/products/distribution).

## Steps to Use the right Environment


cd CopepodBiomass/Script

conda activate /net/meso/work/svivier/.conda/envs/sebpy

python -m ipykernel install --user --name sebpy --display-name "Python (sebpy)"

Use the "Python (sebpy)" Kernel to run the scripts



**** Script:

###___COPEPOD_DATA.ipynb 

Construct an taxonomic abundance (ind/m^3) matrix and the corresponding total biomass (mg C/m^3) matrix per samples (Data/MeasurementValue_matrix.csv; Data/CarbonMass_matrix.csv) from COPEPOD ('https://www.st.nmfs.noaa.gov/copepod/search/by_dataset.html')

###___ICWs_evaluation_and_correction.ipynb 

1)First Step:  Construction of the final datasets used to evaluate and improve (inverse model) the ICWs of AtlantECO: 'COPEPOD80_BIOMASS'= final Total biomass matrix and 'COPEPOD80_df_clean'= final abundance matrix: 'Abundance_IM_final.csv', 'Biomass_IM_final.csv'

2) Second Step: "Rapport work= Grouping strategies + Inverse model + Result of inverse model and evaluation of the ICWs of AtlantECO"


###___ Inversemodel_test.ipynb

Input Data:  Abundance_IM_final.csv (Abundance final COPEPOD)

=> Construction of simulated data (Biomasse totale of samples) using Abundance_IM_final.csv and AtlantECO ICWs

Output Data: IM_sensitivity.csv = Result of inverse model prediction for different grouping strategy and for informative and non-informative priors

###___FGs_Data.ipynb

Construct the biomass data of functional groups (FGs_biomass.csv = Input Data for CEPHALOPOD)
Use of Abundance data and of the ICWs of each species (AtlantECO ICWs, or manual ICWs)

###___FGs_distribution_Trait_clustering.ipynb

Plot CEPHALOPOD figure (Open 'all_ens' of CEPHALOPOD (64800(latxlon) x nb(FGs) x nb(bootstrap) x nb(month)) and plot clustering and trait proportion in each cluster

