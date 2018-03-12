# R related issues

### Timeout issue using "devtools" package
"Installation failed: Timeout was reached: Connection timed out after 10000 milliseconds"- solution

To add on:
If your system prevent you from downloading R packages from github using "devtools", error messages
"Installation failed: Timeout was reached: Connection timed out after 10000 milliseconds" appears, follow the following steps.

## STEP 1.
# go to the r package location on github, download the zip file. I am using the "XYZ" package as an example. 
#     --- file downloaded as "XYZ-master.zip"
#     --- move "XYZ-master.zip" to folder "E:/source". You can choose your own directory.

## STEP 2.
# run below command on R consle
devtools::install("E:/source/XYZ-master")
#################################################################
## Other solution reference
from author(Ufos):
https://stackoverflow.com/questions/16680618/installing-packages-onto-r


