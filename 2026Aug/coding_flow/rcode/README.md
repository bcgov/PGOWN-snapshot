There are three ways the script PGOWN-Snapshot.Rmd can be run

1. R Shiny app: Runs the Rmd file directly using app.R in the parent folder. This option should be used when no edits are to be made to the .Rmd file
2. Setting up project: Runs the Rmd file directly from the parent folder. To do this, you would have to create an R project in the parent folder. Then, open the project and Knit the .Rmd file. This option should be used if there are issues with R Shiny
3. Run file directly: Uncomment line 19 in the .Rmd file, set working directory to current file location, and Knit the .Rmd file. This option should be used when making edits to the .Rmd file 