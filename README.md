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

data is saved on disc in the following way
   subdir data: Condains the covid19 csv files
   subdir landkreise: contains the geodata of the landkreise and bundeslaender
   All plots are witten to the current directory
   
