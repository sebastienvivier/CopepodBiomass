###___Description of the output data of COPEPOD_DATA.ipynb 

combined_csv.csv: All data from COPEPOD (https://www.st.nmfs.noaa.gov/copepod/search/by_dataset.html) with both: "Zooplankton biomass data and zooplankton abundance data "= 28 different Ship cruise
Abundance.csv: Original Abundance data and Abundance data in ind/m^3
Biomass.csv: Original Biomass data and Biomass data in mg.C/m^3
MeasurementValue_matrix.csv: Abundance matrix (ind/m^3): Line= unique_id (Samples), Colonne= Taxa-Name
CarbonMass_matrix.csv: Biomass matrix (mg C/m^3): Line= unique_id (Samples), Colonne= One colone (Carbon Mass)


###___Description of the  ICWs_evaluation_and_correction.ipynb 

CarbonMass_Atlanteco.csv: Mean, Min, Max ICWs of AtlantECO for each Copepod Species



1)First Step:  Construction of the final datasets used to evaluate and improve (inverse model) the ICWs of AtlantECO: 'COPEPOD80_BIOMASS'= final Total biomass matrix and 'COPEPOD80_df_clean'= final abundance matrix: 'Abundance_IM_final.csv', 'Biomass_IM_final.csv'

2) Second Step: "Rapport work= Grouping strategies + Inverse model + Result of inverse model and evaluation of the ICWs of AtlantECO"




