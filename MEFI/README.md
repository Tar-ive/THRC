# MEFI Project 

## Steps to Do with v3 DCI Data
- MEFI-DCI.ipynb = Notebook contains in-depth spatial analysis of economic distress using the Distress Community Index (DCI). It processes data at the ZIP Code Tabulation Area (ZCTA) level and aggregates results to the Metropolitan Statistical Area (MSA) level across multiple years. The primary goal is to identify spatial clusters (hotspots and coldspots) of distress/prosperity, analyze inequality within MSAs, and generate various population-weighted and geography-based metrics for each MSA. The analysis evolves through several versions, primarily transitioning from Getis-Ord Gi* to Local Moran's I for cluster detection due to identified issues with Gi* Z-score calculations. The notebook also includes extensive data validation, deduplication, handling of ZCTA-MSA crosswalks, generation of statistical reports, and creation of interactive visualizations.

- MEFI_final_dataset_creation.ipynb = Edit this file once you get the** msa_spatial_{year}_v{n}.csv files from MEFI-DCI.ipynb** and use that to create succeeding files here. Rerun version specific file changes **(currently at v8)** with edits assigned by supervisor.

- maps.ipynb : After aggregating dataset confirm that they have approx ~28,000 or more ZCTAs or as described by the supervisor, then use the same** msa_spatial_{year}_v{n}.csv file from MEFI-DCI.ipynb** here in order to create HTML maps. You will need to download these maps to the device or write specific functions to render these maps in the notebook itself. Mention to the supervisor that this is an important way to figure data out visually as the aggregate dataset has ~1.1 million rows.

##  IF Persistant Errors with Above Notebooks, Use these Notebooks to get deepdive into Data Composition and for Root Level Analysis 
- MEFI (1).ipynb : **(Only use in case of top 3 files having errors which need deeper level investigation)** -> This notebook processes BRFSS data from various years, standardizing and mapping it to current CBSA codes, and then enriches this information with MEFI scores and population figures. This complex mapping process ensures accurate linking of older BRFSS data to current metropolitan area classifications and MEFI scores, particularly for years **2007, 2008, and 2012.**

- 2017_2022_DCI.ipynb: This notebook loads and processes BRFSS (SMART) and MEFI datasets for 2017 and 2022, standardizing geographical codes, resolving inconsistencies, and merging them to enrich the BRFSS data with MEFI scores and population information. The refined data is then saved into clean, semi-clean, and full output files for further analysis.

## General Tips While Working with these Data Sources: 
1. Always load and save files with google colab directly. Helps with version tracking of files.
2. Most likely cause of issues are the changing MSA and ZCTA numbers and a clear governmental data on how many years should have how many ZCTAs and MSAs, so look through [https://www.census.gov/data/tables/time-series/demo/popest/2020s-total-metro-and-micro-statistical-areas.html] or data.gov resources only. 
3. Most cells already have outputs, study them, understand what good bad output looks like before rerunning them.
4. Precision edits will be required for the data dictionary even after programatic generation, refer to previous versions of data dictionary for reference. 
5. Notebook files have a lot of code in general (most of that is debugging as building code cells and are redundant) refer to the bottom of notebooks or ctrl+F to find the required data file names for eg : msa_spatial_{year}_v{n}.csv, see which cell's outputs save these files and work from there onwards.
