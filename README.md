# rki-covid-explore

Small tool for downloading the German Robert-Koch institut (RKI) Covid database and doing some 
basic analyzes with it

rki-covid explore is a standalone running tool and gets the necessary data from RKI
The code connects to RKI ESRI data service to get the Landkreis and Bundesland geodata
The code also downloads the last available covid database from the RKI and saves it as a file (csv)

The code allows lineplots for selected Landkreise/Bundeslaender
or lineplots of the top Landkreise with increasing incidence

Last baut not list it plots the map of germany colored by incidence
Another option is a plot of the map with the 7 Day change in incidence

All the plots can also be aggregated into one report pdf file.

data is saved on disc in the following way
   subdir data: Condains the covid19 csv files
   subdir landkreise: contains the geodata of the landkreise and bundeslaender
   All plots and the report pdf file are witten to the current directory
   
Since all the data used comes from the RKI, do not forget to reference the data source:
"Datenquellenvermerk: Robert Koch-Institut (RKI), dl-de/by-2-0"

See https://npgeo-corona-npgeo-de.hub.arcgis.com for details of the datasets used.


Die Daten sind die „Fallzahlen in Deutschland“ des Robert Koch-Institut (RKI) und stehen unter der
Open Data Datenlizenz Deutschland – https://www.govdata.de/dl-de/by-2-0 – Version 2.0 zur Verfügung. 

Python tabulate (MIT-license) https://github.com/astanin/python-tabulate
