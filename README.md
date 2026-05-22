# 2026_Current_Biology_Spratt_et_al
# Spratt_SPI2_tuning_paper
This repository contains summary data and code used in Spratt M. & Lane K. (2026) DOI: 


# Flow Cytometry Data 

## Summary Dataframes 
6 .xlsx files are included - found in FlowSummaryStats

FlowJo was used to analyze FCS files. The .xlsx files contain summary statistics as exported by FlowJo and are organized by figure. 

# DIMM Data: 

## Summary Dataframes 
Summary datafiles for untracked data are located in DIMM_untracked and contain a csv file for each experiment with regionprops data for all cell labels before and after media transition.

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

- **ParentProgenyCorrelative_Plotting.ipynb - contains code to filter and plot Figure 5F

- **RandomForest.ipynb** - contains code used to generate and plot random forest regressor models as in Figure 5

# Macrophage Data

## Extracted Data

- **IC_Bact_Tracking** - folder contains .pkl files extracted from Trackmate for tracked bacteria in Figure 6B

- **BAF_pHrodo.csv** - data used in Figure 6F

- **BAF_STm_Infection.csv** - data used in Figure 6F-I

## Analysis

  

