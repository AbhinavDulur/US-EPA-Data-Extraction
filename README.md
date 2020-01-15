# US-EPA-Data-Extraction
This repository is used to obtain toxic release information about a particular zipcode by using the U.S. EPA Data API. The end goal is to enter a zipcode and retrieve associated EPA information.

The way that the API works is that, through their data model, you select (up to 3) specific data tables to look at. I selected 3 data tables of interest (TRI_FACILITY for facility zip code, TRI_REPORTING_FORM for reporting year and chemical name, and TRI_RELEASE_QTY for the amount released).

I then subselected by zip code. This gives us a final dataframe, of facilities, by zip code. Each row will then correspond to the total release quantity of a specific facility, of a specific compound, on a specific year.

API Usage https://www.epa.gov/enviro/envirofacts-data-service-api#metadata

Data Model https://www.epa.gov/enviro/tri-reported-chemical-information-subject-area-model

Useful variable descriptions:

Chemical Name: https://enviro.epa.gov/enviro/EF_METADATA_HTML.tri_page?p_column_name=CAS_CHEM_NAME
Total Release: https://enviro.epa.gov/enviro/EF_METADATA_HTML.tri_page?p_column_name=TOTAL_RELEASE
