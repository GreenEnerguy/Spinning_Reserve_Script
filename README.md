# Spinning_Reserve_Script
A Jupyter Notebook to read primary and secondary spinning reserve data from a .iso file distributed by the Salvadoran Dispatch Center (UT)
## Python script to read .csv with spinning reserve data from a .iso file

## 1. Description
In El Salvador, the Dispatch Centre (Unidad de Transacciones, UT) delivers the operating data of the generators connected to the country transmisssion line, including data about the expenses incurred by renewable energy generators for not being able to provide the system with firm capacity (primary and secondary spinning reserve). 

The operating data for each generator is posted in the generator's private section in a .iso file. This .iso file contains several folders, one of which includes the .csv file with data about primary and secondary spinning reserves.

This script loops through all available .iso folders, reads spinning reserve data into a list, and then concatenates all data into a single dataframe. Subsequently this dataframe is resampled into daily format so that it is possible to calculate daily and monthly expenses in spinning reserves. Finally the data is exported into an Excel file with two tabs, one for the primary and one for the secondary reserves.


## 2. How to use the script
The script is written in Python in a Jupyter notebook. The script and the folder that contains the .iso file have to be copied within the same folder. Apart from that, just running the script loops through all existing folders and reads .csv within .iso files. The only caveat is that it needs a temporary .csv file to store the data read in every loop. This file can be anywhere, just the path has to be provided to the command 'iso.get_file_from_iso'.

## 3. Output
The script output is a .xlsx file with two tabs summarizing the daily primary and secondary reserve expenses for the whole timeframe available. 
