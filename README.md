# Ukrainian-crime-statistics-2013_2023
This dataset summarizes statistical data from the Office of the Prosecutor General of Ukraine on crimes committed during 2013-2023.
The dataset is sourced from xlsx files that are annually published by the Office of the Prosecutor General of Ukraine on its official website. These source files are placed unchanged in the SOURCE folder. Unfortunately, the source files contain information in a format that is not suitable for use in analytical tools. Therefore, R scripts were prepared for each of the files to extract and transform the data according to the principles of "Tidy Data" and taking into account the specific use of this dataset as a fact table in MS Power BI.

The dataset is presented in the following format:
Each row of the dataset represents individual articles of the Criminal Code of Ukraine for the corresponding years as observations. Additionally, a reference of these articles in both Ukrainian and English, considering their changes at the time of the dataset preparation, is provided in the DIMENSIONS folder.
The following data are presented as variables in the columns:

All data gaps and anomalies are retained in the dataset. However, the following changes were applied:

All types (grounds) for suspending and closing criminal investigations were combined into unified columns "XXX" and "YYY".
Information about specific categories of persons who committed crimes was removed from the data.
