# 2026_Current_Biology_Spratt_et_al
# Spratt_SPI2_tuning_paper
This repository contains summary data and code used in Spratt M. & Lane K. (2026) DOI: 

# Fixed Cell Data
- **Fixed_Cell_SLData** -contains .csv files extracted with region props for Figure 1 and associated supplement, each experiment is it's own file. Note that pLL565 refers to the PssaG-sfGFP(LVA)-mRuby2 reporter, pLL749 refers to the PssaB-sfGFP-mRuby2 reporter, pLL889 is the promoterless GFP(-) control construct, and the KO strain is the ssrB KO in this data set.  
- **Fixed_Cell_SLCode** - notebook to process, filter and plot data from the above CSVs as in Figure 1 and associated supplement.

# smFISH Data
-**smFISH_Data** - contains folders for data files that have all intracellular spot intensities (spot_int_dataframes), the spots detected per cell (spot_count_dataframes), and and rare instances of saturated cells to be removed (rna_saturation).

-**smFISH_Code** - contains notebook used to process and plot the data from those three dataframe sets. 

# Flow Cytometry Data 

## Summary Dataframes 
6 .xlsx files are included - found in FlowSummaryStats

FlowJo was used to analyze FCS files. The .xlsx files contain summary statistics as exported by FlowJo and are organized by figure. 

## FCS Files

All FCS files and FlowJo workspaces can be found on Zenodo, Figure 1 FCS and .wsp files are included in /FlowFCSandWSP as examples. 

# DIMM Data: 

## Summary Dataframes 

4 data files are included from the tracked data set - found in DIMM_summaries

- **Full_MotherCell_Data.csv** - contains all processed median sfGFP and mRuby2 intensity values and cell length (feret_diameter_um) for 3 separate experiments - 258 total mother cells. 

- **CellCycle_Stats.csv** - contains information about all cycles of all tracked cells. Every combination of unique_ID and cell_ID will have multiple rows pertaining to what cycle the data is on. Cycle numbers start at 0 for each cell that emerges. Note that this contains 'incomplete' cycles that were not fully captured by the imaging - these are filtered in the analysis notebooks. 

- **Switch_Stats.csv** - contains information pertaining to detected GFP reporter switches of each cell. This includes all mother cells and progeny cells. Cells that were born above the GFP(+) threshold or do not have a detected start increase time have NaNs in these columns. Also contains boolean classifiers that are used for filtering in notebooks. See companion text file for details on what each column header refers to. 

- **mRuby_Stats.csv** - contains information about Ruby features for each cell_id.

- **model_params.xlsx** - contains parameters (as column names) for each of the Random Forest Regressor models created

## Analysis
4 jupyter notebooks for downstream analysis and plotting are included - found in DIMM_code 

- **Cycle_Feature_Plotting.ipynb** - contains code used to filter and plot cell cycle features as in Figure 5A-C

- **Mother_Plotting.ipynb** - contains code used to plot mother cell data as in Figure 4

- **ParentProgenyCorrelative_Plotting.ipynb** - contains code to filter and plot Figure 5F

- **RandomForest.ipynb** - contains code used to generate and plot random forest regressor models as in Figure 5

# Macrophage Data

## Extracted Data

- **Tracked_Bacteria_Dict.pkl** - contains .pkl files extracted from Trackmate for tracked bacteria in Figure 6B

- **full_pHrodo.csv** - data used in Figure 6F

- **BAF_STm_Infection.csv** - data used in Figure 6F-I

## Analysis
- **Tracked_Bact_Plotting.ipynb** - contains code to process and plot .pkl files as in Figure 6B
- **pHrodo_plotting.ipynb** - contains code to plot pHrodo bioparticle data
- **BAFA1_Infection_Analysis.ipynb** - contains code to plot BAF-A1 infection data in Figure 6F-I and associated supplement
  

