# Ukrainian-crime-statistics-2013_2023
### This dataset summarizes statistical data from the Office of the Prosecutor General of Ukraine on crimes committed during 2013-2023.

The dataset is sourced from xlsx files that are annually published by the Office of the Prosecutor General of Ukraine on its [official website](https://gp.gov.ua/ua/posts/pro-zareyestrovani-kriminalni-pravoporushennya-ta-rezultati-yih-dosudovogo-rozsliduvannya-2). These source files are placed unchanged in the _SOURCE_ folder. Unfortunately, the source files contain information in a format that is not suitable for use in analytical tools. Therefore, R scripts were prepared for each of the files to extract and transform the data according to the principles of "Tidy Data" and taking into account the specific use of this dataset as a fact table in MS Power BI.

The dataset is presented in the following format:

- csv
- RData

Each row of the dataset represents individual articles of the Criminal Code of Ukraine for the corresponding years as observations. Additionally, a reference of these articles in both Ukrainian and English, considering their changes at the time of the dataset preparation, is provided in the _DIMENSIONS_ folder.

The following data are presented as variables in the columns:

- Registered Crimes (Not Criminal Cases)
- Crimes with Suspicions Announced
- Crimes with Suspended Investigation
- Crimes with Indictment Sent to Court
- Conclusion on Exemption from Liability Sent to Court
- Petition for Medical Procedures Sent to Court
- Petition for Educational Procedures Sent to Court
- Investigation of Crimes Terminated
- Crimes with Unresolved Status
  
All data gaps and anomalies are retained in the dataset. However, the following changes were applied:
1. All types (grounds) for suspending and closing criminal investigations were combined into unified columns "Crimes with Suspicions Announced" and "Investigation of Crimes Terminated".
2. Information about specific categories of persons who committed crimes was removed from the data.
