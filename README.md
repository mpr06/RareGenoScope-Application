# Creating rare disease networks
This repository contains the R script and the related files to create a rare disease network using the DisGeNET, STRING, WikiPathways, and DrugBank APIs. The script retrieves disease-related genes and their protein-protein interactions, pathways, and similar drugs based on their gene symbols. The network is then visualized using the visNetwork package in a Shiny app. It serves as a pipeline for creating and analzing rare disease networks. 

# Dependencies

The R script was made using __ version of RStudio. You will first need to install the following packages: 

install.packages("httr"). Version: 
install.packages("jsonlite"). Version: 
install.packages("dplyr"). Version: 
install.packages("igraph"). Version: 
install.packages("visNetwork"). Version: 
install.packages("shiny"). Version: 
install.packages("viridis"). Version: 
install.packages("stringdist"). Version: 


# Other tools that are needed
Obtain an API key from DisGeNET by creating a account and getting it authorized and replace the placeholder api_key in the script. Download the DrugBank dataset in CSV format and update the path to the file in the drugbank_data variable in the Rscript. Run the code and a shiny application will open. Type the name of the disease and click submit. Makesure the first letter each word is captilized

Drugbank file was downloaded from go.drugbank.com and then sorted and converted to csv using python code. this python code can be found in the repository to sort and extract the information from the file. 

# Workflow
1) Set up the API key and authorization headers for the DisGeNET API.
2) Retrieve the disease-associated genes from the DisGeNET API.
3) Convert the JSON response to a data frame.
4) Get the gene data from DisGeNET.
5) Map the gene symbols to STRING IDs using the STRING API.
6) Query the STRING API for protein-protein interactions (PPIs) among the gene products.
7) Retrieve the pathways for each gene using the WikiPathways API.
8) Combine the pathway data into a single data frame.
9) Visualize the network using the visNetwork package in a Shiny app.
11) Add similar drugs to the network as nodes and edges.
12) Visualize the updated Disease-Gene-Drug-Network using the visNetwork package in a Shiny app.



