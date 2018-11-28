# Utilisation de R


## Déclaration du Notebook
---
title: "R Notebook"
output: html_notebook
---

## Erreur Lors de la Connection  
```{r setup, include=FALSE}
library(odbc)
con <- dbConnect(odbc::odbc(), "PostgreSQL30")

Error in library(odbc) : aucun package nommé ‘odbc’ n'est trouvé
```
### Solution
install.packages("odbc")
install.packages("RCurl")
install.packages("tidyverse")
install.packages("httr")
install.packages("jsonlite")


#	Utilisation de R pour requete sur API
https://tclavelle.github.io/blog/r_and_apis/

# Load packages
library(tidyverse)
library(httr)
library(jsonlite)

# Save username as variable
username <- 'pierre56'

# Save base enpoint as variable
url_git <- 'https://api.github.com/'

# Construct API request
repos <- GET(url = paste0(url_git,'users/',username,'/repos'))

# Examine response components
names(repos)

##  [1] "url"         "status_code" "headers"     "all_headers" "cookies"    
##  [6] "content"     "date"        "times"       "request"     "handle"


## Importing data from a JSON file into R
https://stackoverflow.com/questions/2617600/importing-data-from-a-json-file-into-r


# API Intéressantes
[cran](https://cran.r-project.org/web/packages/jsonlite/vignettes/json-apis.html)


## Package pour faire des inputs
[svDialogs](https://cran.r-project.org/web/packages/svDialogs/index.html)
