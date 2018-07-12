# FunMappOne

### Install dependencies

```R
source("http://bioconductor.org/biocLite.R")
biocLite("clusterProfiler")
biocLite("org.Hs.eg.db")
biocLite("org.Mm.eg.db")
biocLite("KEGG.db")
biocLite("reactome.db")
biocLite("GOSim")

#Install CRAN dependencies
cran_pkgs <- c("ggplotify", "RColorBrewer", "reshape", "ggplot2", "shiny", "shinyjs", "tibble", 
               "gProfileR", "DT", "randomcoloR", "readxl", "cellranger", "devtools")
cran_pkgs.inst <- cran_pkgs[!(cran_pkgs %in% rownames(installed.packages()))]
if(length(cran_pkgs.inst)>0){
  print(paste0("Missing ", length(cran_pkgs.inst), " CRAN Packages:"))
  for(pkg in cran_pkgs.inst){
    print(paste0("Installing Package:'", pkg, "'..."))
    install.packages(pkg, repo="http://cran.rstudio.org", dependencies=TRUE)
    print("Installed!!!")
  }
}
```
### Run FunMappOne from GitHub
```R
# Load 'shiny' library
library(shiny)
library(shinyjs)
# Using runGitHub
runGitHub("FunMappOne", "Greco-Lab")
```

#### How to run locally
```R
  # Clone the git repository
  git clone https://github.com/Greco-Lab/FunMappOne FunMappOne

  # Start R session and run by using runApp()
  library(shiny)
  runApp("FunMappOne/")
```
