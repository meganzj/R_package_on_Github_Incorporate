# R-package-on-Github-Incorporate
"Installation failed: Timeout was reached: Connection timed out after 10000 milliseconds"- solution

The original solution came from the below link from author(Ufos):
https://stackoverflow.com/questions/16680618/installing-packages-onto-r


To add on:
If your system prevent you from downloading R packages from github using "devtools", error messages
"Installation failed: Timeout was reached: Connection timed out after 10000 milliseconds" appears, follow the following steps.

# STEP 1.
# check directory(and its parent directory) of the R packages using the below command. 
# For security purpose, I only have the "READ ONLY" permission.
# This permission limitaion is the key reason that permit me downloading the packages from github.
.libPaths()

# STEP 2.
# prepare an external hard drive/ find a directory(folder) which you have both the "write" and "read" permission!!!!
# in my case, it is e:/ drive.

# step 3.
# create 2 folders under the directory defined in step 2
#    ---one to saved the zip file downloaded from github(named "source").
#    ---one to store the r package file(names "libs").


# step 3.
# go to the r package location on github, download the zip file. I am using the "pluralize" package as an example. 
#     --- file downloaded as "pluralize-master.zip"
# move "pluralize-master.zip" to folder "source".

# step 4.
# run below command on R consle
install.packages("E:/source/pluralize-master.zip", destdir = 'E:/source', lib = 'E:/libs', repos = NULL)

# step 5.
# use the package
library('pluralize', lib.loc = 'E:/libs')


