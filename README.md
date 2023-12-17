*SDS 3386: Data Science Lab - Fall 2023 - Professor: Dr. Tanyah Schmah -  University of Ottawa*

## Project by Team IKEA:

# **On the streets of Ottawa**: *A perspective on crime, drugs and homelessness*

<br>

**Jiménez Guadalarrama, Emiliano** (300209723)

**Taillardat, Alexis** (300244377)

**Tawadros, Kevin** (300244537)

The three of us live and/or study in Ottawa. Like a lot of people, we could not help but notice some issues in our streets have been seemingly increasing for the past years: more homelessness, more ambulances coming to handle overdoses, an intensified presence of the police to prevent crimes… But are these increases a real fact? If so, is there a reason behind it? And what has been done to address it? These are the questions this project seeks to answer. In this project we used a dashboard, interactive maps, hypothesis tests and group-based maltivariate trajectory modeling (gbmt).


## Project files

**README.md** (this)

**SDS3386_FinalReport_TeamIKEA_JimenezTaillardatTawadros.pdf**: pdf file reports all the important results in the project.

**requirements.txt**: text file contains all libraries and packages for the project (Python and R)

**clean_datasets**: folder contains all cleaned datasets produced by notebooks/data_cleaning.ipynb and Scripts/clean_data.Rmd

**clusters**: folder contains clusters results in form of original data plus additional column indicating the cluster id (in form of pickle file) produced by notebooks/clusters.ipynb

**datasets**: folder contains all raw datasets for this project:

* **CMHC_RentalsMedianPrices.csv**: contains median prices of apartements in Ottawa between 2001 and 2023. 
* **CMHC_VacancyRate.csv:** contains vacancy rate of apartements in Ottawa 2001 and 2023.
* **Community_Police_Centers_Open_Data.csv**: contains FID (Id), Name (Police Center Name), Address (Police Center address), Division (Police center division: East, west or Center) of all Community Police centers in Ottawa
* **Confirmed_Opioid_related_Deaths_of_Ottawa_Residents_.csv**: contains information on the number of deaths of Ottawa residents by quarter and year. It covers the period from April 2017 to June 2023.
* **Criminal_Offences_Open_Data.csv**: contains the occurrence date, reported date, year (of the reported date), occurrence hour, weekday, offence summary, offence category, Neighbourhood Name, Sector, Division, Census Tract of crimes reported between 2018 and 2022 in Ottawa.  
* **Hospitals.geojson**: contains information about the locations of hospitals in Ottawa
* **Housing_Services_monthly_HIFIS_data.csv**: contains the monthly aggregated data of unique clients and/or families in shelter system
* **Opioid_overdose_emergency_department_visit_count_by_month_-_Monthly_Opioid_ED_visits.csv**: contains information regarding the count of patient emergency visits to Ottawa hospitals with an overdose's diagnosis. It covers the period from April 2017 to August 2023.
* **OPS_Neighbourhoods_Open_Data.csv**: contains the shape of the neighbourhoods in Ottawa
* **OPS_Neighbourhoods_Open_Data.geojson**: contains the shape of the neighbourhoods in Ottawa
* **Overdose_Calls_Open_Data.csv**: contains information about the emergency calls related to overdoses with a precise date (includes day of the week, day of the month, month, and year) and time of the report. This dataset covers the period from 2018 to 2022.
- **RESOURCES:** https://open.ottawa.ca/datasets/; https://data.ottawapolice.ca/

**notebooks**: folder contains all jupyter notebooks for this project:

* **app.py**: python file contains a flask app for the dashborad.
* **clusters.ipynb**: jupyter notebook that clusters crimes using k-means and DBSCAN to compare it to the actual police centres and hospitals locations in Ottawa.
* **data_cleaning.ipynb**:  jupyter notebook that contains all the data cleaning and manipulation of raw data. All resulted tables are saved in clean_datasets folder.
* **homelessness_analysis.ipynb**: jupyter notebook that contains all analysis for homelessness datasets including visualisation and linear regression model.
* **neighbourhood_trajectory_visualisation.ipynb**: jupyter notebook that contains a visulistaion on a map for neighbourhoods trajectory groups produced by Scripts/Trajectory_analysis.Rmd
* **overdose_analysis.ipynb**: jupyter notebook that contains all analysis related to overdoses datasets inlcuding TukeyHSD test, F-test, t-tests and visualisation


**Scripts**: folder contains all R markdown folders:

* **clean_data.Rmd**: R markdown file that clean the raw data to clean data used in trajectory analysis. All clean datasets are saved in clean_datasets folder.
* **Trajectory_analysis.Rmd**: R markdown file contains all grouped-based multivariate trajectory modeling applied to overdoses, shelters and crime related datasets. All plots are saved in Trajectories/plots folder.

**Trajectories:** folder contains Trajectory analysis results produced by scripts/Trajectory_analysis.Rmd

* **plots:** folder contains all plots produced by scripts/Trajectory_analysis.Rmd as png files
* **traj_nei_results.csv**: csv file contains neighbourhood name and group id produced by scripts/Trajectory_analysis.Rmd
