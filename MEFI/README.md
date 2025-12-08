# MEFI Project 
```
- MEFI-DCI.ipynb = Notebook contains in-depth spatial analysis of economic distress using the Distress Community Index (DCI). It processes data at the ZIP Code Tabulation Area (ZCTA) level and aggregates results to the Metropolitan Statistical Area (MSA) level across multiple years. The primary goal is to identify spatial clusters (hotspots and coldspots) of distress/prosperity, analyze inequality within MSAs, and generate various population-weighted and geography-based metrics for each MSA.

The analysis evolves through several versions, primarily transitioning from Getis-Ord Gi* to Local Moran's I for cluster detection due to identified issues with Gi* Z-score calculations. The notebook also includes extensive data validation, deduplication, handling of ZCTA-MSA crosswalks, generation of statistical reports, and creation of interactive visualizations.

- MEFI_final_dataset_creation.ipynb = Edit this file once you get the msa_spatial_{year}_v{n}.csv files from MEFI-DCI.ipynb and use that to create succeeding files here. Rerun version specific file changes (currently at v8) with edits assigned by supervisor.

- maps.ipynb : After aggregating dataset confirm that they have approx ~28,000 or more ZCTAs or as described by the supervisor, then use the same msa_spatial_{year}_v{n}.csv file from MEFI-DCI.ipynb here in order to create HTML maps. You will need to download these maps to the device or write specific functions to render these maps in the notebook itself. Mention to the supervisor that this is an important way to figure data out visually as the aggregate dataset has ~1.1 million rows.


```
