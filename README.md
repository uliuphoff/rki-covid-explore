# rki-covid-explore

Small script for downloading the German Robert-Koch institut (RKI) Covid database and doing some 
basic analyzes with it.

rki-covid explore is a standalone script which gets alle the necessary data from RKI. 
The code connects to RKI ESRI data service to get the Landkreis and Bundesland geodata.
The code also downloads the latest available covid database from the RKI and saves it as a csv-file.

The code allows lineplots for selected Landkreise/Bundeslaender
or lineplots of the top Landkreise with increasing incidence

Last but not least it plots the map of germany colored by incidence.
Another option is a plot of the map with the 7 Day change in incidence.

All the plots can also be aggregated into one report pdf file.

data is saved on disc in the following way:

    subdir data: Condains the covid19 csv files
    subdir landkreise: contains the geodata of the landkreise and bundeslaender
    All plots and the report pdf file are witten to the current directory

Output is provided as text

    Überblick am: 23.01.2022
    Inzidenz    Neue Fälle  Kreis
    -------     --------  ----------------------------------
     840.3         63393  Deutschland
     922.2         14847  Bayern
    1406.9          2866  SK München

    Top Änderungen gegenüber Vorwoche:
    Inzidenz    Neue Fälle    Änderung [%]  Kreis
    -------  ------------  --------------  -----------------------------
    1601.7           128             211  LK Uckermark
    1496               0             274  LK Stormarn
     545.1             0            1296  SK Berlin Marzahn-Hellersdorf

    Top Inzidenzen:
    Inzidenz    Neue Fälle  Kreis
    ------  ------------  ----------------------------------
    1757.4             0  SK Berlin Pankow
    1763.8           307  SK Berlin Neukölln
    1782.5           115  SK Berlin Friedrichshain-Kreuzberg
    
Various diagrams are also possible:
![rki-covid-explore_output](https://user-images.githubusercontent.com/95683288/150784305-bf98b0d1-f9f6-4928-b5f6-066a4f22f3a3.jpeg)

Since all the data used comes from the RKI, do not forget to reference the data source:
"Datenquellenvermerk: Robert Koch-Institut (RKI), dl-de/by-2-0"

See https://npgeo-corona-npgeo-de.hub.arcgis.com for details of the datasets used.


Die Daten sind die „Fallzahlen in Deutschland“ des Robert Koch-Institut (RKI) und stehen unter der
Open Data Datenlizenz Deutschland – https://www.govdata.de/dl-de/by-2-0 – Version 2.0 zur Verfügung. 

Python tabulate (MIT-license) https://github.com/astanin/python-tabulate
