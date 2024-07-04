All data Available on meso: /net/meso/work/svivier/Git/Data/


###___Description of the data of COPEPOD_DATA.ipynb 

Input Data:
'/net/meso/work/svivier/COPEPOD_data/Data_copepod/copepod__*/data_src/short-format/*.csv' #All data that present Abundance and Biomass observation in COPEPOD: https://www.st.nmfs.noaa.gov/copepod/search/by_dataset.html

Output:

combined_csv.csv: All data from COPEPOD (https://www.st.nmfs.noaa.gov/copepod/search/by_dataset.html) with both: "Zooplankton biomass data and zooplankton abundance data "= 28 different Ship cruise combined in one .csv 
Abundance.csv: Original Abundance data and Abundance data in ind/m^3
Biomass.csv: Original Biomass data and Biomass data in mg.C/m^3
MeasurementValue_matrix.csv: Abundance matrix (ind/m^3): Line= unique_id (Samples), Colonne= Taxa-Name
CarbonMass_matrix.csv: Biomass matrix (mg C/m^3): Line= unique_id (Samples), Colonne= One colone (Carbon Mass)


###___Description of the  ICWs_evaluation_and_correction.ipynb 

Input Data:
CarbonMass_Atlanteco.csv #Mean, Min, Max ICWs of AtlantECO for each Copepod Species
MeasurementValue_matrix.csv: Abundance matrix (ind/m^3): Line= unique_id (Samples), Colonne= Taxa-Name
CarbonMass_matrix.csv: Biomass matrix (mg C/m^3): Line= unique_id (Samples), Colonne= One colone (Carbon Mass)

Output Data:
'Abundance_IM_final.csv' #Final abundance data used to evaluate AtlantECO ICWs and to improve these ICWs with inverse model (ind/m^3)
'Biomass_IM_final.csv' #Final total biomass data used to evaluate AtlantECO ICWs and to improve these ICWs with inverse model (mg C/m^3)


1)First Step:  Construction of the final datasets used to evaluate and improve (inverse model) the ICWs of AtlantECO: 'COPEPOD80_BIOMASS'= final Total biomass matrix and 'COPEPOD80_df_clean'= final abundance matrix: 'Abundance_IM_final.csv', 'Biomass_IM_final.csv'

2) Second Step: "Rapport work= Grouping strategies + Inverse model + Result of inverse model and evaluation of the ICWs of AtlantECO"


###___ Inversemodel_test.ipynb

Input Data:  
Abundance_IM_final.csv #Abundance final COPEPOD

=> Construction of simulated data (Biomasse totale of samples) using Abundance_IM_final.csv and AtlantECO ICWs

Output Data: 
IM_sensitivity.csv #Result for different grouping strategy and for informative and non-informative priors


###___FGs_Data.ipynb

Input Data: 
1) /net/kryo/work/public/shared/AtlantECO/BASE/AtlantECO-BASE-v1_microbiome_traditional_Copepoda_abund+biomass_20221220.csv #AtlantECO data
2) trait.xlsx #FGs per Species and Traits per Species

Output Data: 
FGs_biomass.csv #Carbonmass data for each FGs (mg C/m^3) = input Data in CEPHALOPOD

###___FGs_distribution.ipynb

Input Data:

