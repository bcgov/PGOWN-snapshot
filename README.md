<!--
Copyright 2018 Province of British Columbia
&#10;Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at
&#10;https://www.apache.org/licenses/LICENSE-2.0
&#10;Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, 
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and limitations under the License.
-->

# pgown-snapshot <a href='https://www2.gov.bc.ca/gov/content/environment/air-land-water/water/groundwater-wells-aquifers/groundwater-observation-well-network'><img src='man/figures/BC_gov_logo.png' align="right" height="139" /></a>

<!-- badges: start -->

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/license/apache-2-0)
<!--[![R-CMD-check](https://github.com/bcgov/bcdata/actions/workflows/R-CMD-check.yaml/badge.svg)](https://github.com/bcgov/bcdata/actions/workflows/R-CMD-check.yaml)
[![Codecov test
coverage](https://codecov.io/gh/bcgov/bcdata/branch/main/graph/badge.svg)](https://app.codecov.io/gh/bcgov/bcdata?branch=main)-->
<!-- badges: end -->

Coding pipeline for the Provincial Groundwater Observation Well Network (PGOWN) snapshot (bi-annual) maintained by the LSDMR team in the EMA branch of the EPD division in the Ministry of Env and Parks

An R coding pipeline for retrieving & summarizing data from [AQUARIUS](https://bcenv-enmods.aqsamples.ca/) for the groundwater well network.

### Code structure

The coding flow has three streams of data input/output. 

data: contains reference data needed to run the scripts (data_jb, data_rc, data_old) that need to be updated for each snapshot, and a folder for storing new data (data_new) generated on running this script.

generated: contains a copy of the figures and tables generated on running this script as well as their underlying data.

rcode: contains the R Markdown file that needs to be run to generate the output report "PGOWN-Snapshot.html". Also contains the script for API calls to the AQUARIUS database as well as an .Renviron that needs to be updated for each snapshot.

**Note:** The `pgown-snapshot` coding pipeline uses data from the AQUARIUS Time-Series API Client. However, data on that server is password protected. If you do not have verified and functional credentials, you will not be able to use this coding pipeline. If you have credentials, update them in the .Renviron file in the folder rcode. Currently they are set to test values and will not work. If you have credentials but encounter errors in running this code, please file an
[issue](https://github.com/bcgov/PGOWN-snapshot/issues/).

### Installation

1. Download the entire folder structure from GitHub as a ZIP file onto your laptop.
2. Unzip the file using the "Extract all" option onto your parent directory. By default, the extracted folder is PGOWN-snapshot-main.
3. If you are running the code for the snapshot report due in Feb 2025, rename the folder labeled "2024July" to "2025Feb".
4. Next, within the folder renamed above, go to /coding_flow/data/ and get updated files from relevant stakeholders for folders data_jb and data_rc.
5. If you want to simply use the files already in this folder, open subfolder "data_rc" and unzip the file "PGOWN_Grades_Appr.zip" to extract the csv file directly.
6. Whether use uploaded your own files in step 4 or not, copy the files in "data_new" subfolder (new in the last run) and paste them in "data_old" (old for this new run).
7. Go to /coding_flow/rcode/ and update the .Renviron file with updated credentials and policy targets' data.
8. Run the file PGOWN-Snapshot.Rmd in R Markdown. If you encounter errors in running this code, please file an [issue](https://github.com/bcgov/PGOWN-snapshot/issues/).

### Reference

[pgown-snapshot 📦 home page and reference
guide](https://bcgov.github.io/pgown-snapshot/)

### Getting Help or Reporting an Issue

To report bugs/issues/feature requests, please file an
[issue](https://github.com/bcgov/PGOWN-snapshot/issues/).

### How to Contribute

If you would like to contribute to the package, please see our
[CONTRIBUTING](https://github.com/bcgov/PGOWN-snapshot/blob/master/CONTRIBUTING.md)
guidelines.

Please note that this project is released with a [Contributor Code of
Conduct](https://github.com/bcgov/bcdata/blob/master/CODE_OF_CONDUCT.md).
By participating in this project you agree to abide by its terms.

### License

Copyright 2018 Province of British Columbia

Licensed under the Apache License, Version 2.0 (the “License”); you may
not use this file except in compliance with the License. You may obtain
a copy of the License at

<https://www.apache.org/licenses/LICENSE-2.0>

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an “AS IS” BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

------------------------------------------------------------------------

*This project was created using the
[bcgovr](https://github.com/bcgov/bcgovr) package.*
