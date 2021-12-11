## My project
 This Project will work with RStudio, mtcar from base R is chosen for this project.

 To better analyze the data you will need to install some R packages. The required packages can be installed using R commands.

```{r}
installed_pkgs <- row.names(installed.packages())
pkgs <- c("car", "dplyr")
for(p in pkgs){
	if(!(p %in% install_pkgs)){
		install.packages(p)
	}
}
```
## Platform
Make sure your wsl is wsl 2 

## Execute the analysis

## Docker
Run the following codes in WSL2
```{r}
#to pull the image from my DockerHub
docker pull zoeyzuo1126/info550dechw5fp 

docker run -it zoeyzuo1126/info550dechw5fp 

#Retrieve 
#create output dir
mkdir ~/doutput
#execute and generate report 
docker run -v ~/doutput:/FP/output zoeyzuo1126/info550hw5fpdec

#Then you should be able to find the report in the directory
#If Not, you can use the following line to set the directory to where you want to find the report
docker run -v ~/doutput:/FP/output zoeyzuo1126/info550hw5fpdec

#just replace ~ with the path

```



## OR
To execute the analysis, from the folder you can run
```{r}
Rscript -e "rmarkdown::render('report.Rmd')"
```

This will create a file called report.html output in your directory that contains the results.

## OR
You could just run the Makefile through terminal to generate report.


