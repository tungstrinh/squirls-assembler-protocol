---
title: Install DES Assembler App
authors:
    - Pranit Shinde
---

# Install DES Assembler App on Windows


## 1. Prerequisites ##

* The following files are provided by DES.
  - Assembler app executable.
  - Docker image `assembly.tar.gz` file
  - Batch script `load_image.batch` to load the docker image
* Docker engine for windows. E.g: https://docs.docker.com/desktop/install/windows-install/

## 2. Installation ##
- Create a folder to place all the files provided by DES. Eg. assembler 
- Unzip the assembler executable file in the assembler folder
- Double click the load_image.batch file, this will open up a command line window with the message Loading docker image…. Wait for the image to load and do not close the window.
- Once the image is loaded, navigate to the assembler app executable. And double click on it. This should start the assembler app.
