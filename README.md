# "Pracital session on "Beyond Genome-wide Association Studies"
## What this session is about?
Genome-wide association studies (GWAS) have identified multiple genetic variants  associated with complex traits, many efforts have shown that a sizeable fraction of the pheotypic variance is explained by the genetics. With the recent trend of making these summary measures publicly available it has opened new avenues to test overlap between these complex traits from the genetics standpoint. In this session, we will explore some of the follow-ups strategy to infer biological evidence from otherwise purely statistical signals. 
## What you need?
To avoid any possible delays/hiccups in running the analysis from a command line (which is the ideal way anyways!!). 
This DIY session instead will use Jypternotebook (web interface) in running the analysis. By this means, participants can focus more on the analysis (then troubleshooting or setting things up)  
## Requirements:
1. Docker software (that creates a VM machine)
2. Docker image file (that contains all the necessary files to run the analysis), it is a gzipped (*.gz) file and will be comminucated few days prior to the session.

# Strongly advise to download this docker image file, prior to the session!!!

## Installing docker for MAC (https://docs.docker.com/docker-for-mac/install/) and Windows 10 Pro (https://docs.docker.com/docker-for-windows/install/)
1. You can set-up a free docker hub account and follow the instructions prompted. Should be straightforward
2. After installing;
Open terminal, and try out some Docker commands.

 ```
 docker version 
 docker run hello-world 
```
### Installing docker for windows 10 or less:
1. Please install docker toolbox https://download.docker.com/win/stable/DockerToolbox.exe , and not the standard docker as it requires Windows 10 Pro
2. stick to the default settings during installation, for more info: https://docs.docker.com/toolbox/toolbox_install_windows/#step-2-install-docker-toolbox
3. After installing;
On your Desktop, find the Docker QuickStart Terminal icon.
-   Click the Docker QuickStart icon to launch a pre-configured Docker Toolbox terminal
-   If the system displays a User Account Control prompt to allow VirtualBox to make changes to your computer. Choose Yes.
-   The terminal does several things to set up Docker Toolbox for you. When it is done, the terminal displays the $ prompt.
-   Try
```
    docker version 
    docker run hello-world 
```

## Questions?
Please email muralisarguru@live.co.uk (with the subject neurepi2018) if you have any questions/tbst in installing docker or others!


# Running the analysis
## CASE 1: FOR MACBOOK / Windows USERS who have installed Standard Docker AND NOT DOCKER TOOLBOX
## STEP1: open terminal or cmd line tool
### RUN

```
   #see if there is any image already
   docker ps
   #load docker image file with, it takes some time WAIT
   docker load < <downloaded tar.gz file>
   #confirm that the image is loaded with,
   docker images
   #run the docker image with,
   docker run -it --rm --user root -p 8888:8888 bioinfo_ms_tut:trial
   #start the notebook for interactive service with,
   jupyter notebook --ip 0.0.0.0 --no-browser --allow-root
```
## STEP 2: Above step gives you an URL 
1. copy the FULL URL and paste it in a web browser (chrome or firefox)
2. Replace the contents within and the brackets with **localhost** and hit ENTER

## CASE 2: FOR MACBOOK / Windows USERS who have installed DOCKER TOOLBOX
## STEP1: open Docker Quickstart terminal (wait until you see a dollar sign, give admin permission as it prompts up)
### RUN

```
   #see if there is any image already
   docker ps
   #load docker image file with, it takes some time WAIT
   docker load < <downloaded tar.gz file>
   #confirm that the image is loaded with,
   docker images
   #run the docker image with,
   docker run --rm -it --user root -d -p 8888:8888 bioinfo_ms_tut:trial
   docker ps
   docker exec -it <containerID> bash
   #start the notebook for interactive service with,
   jupyter notebook --ip 0.0.0.0 --no-browser --allow-root
```
## STEP 2: Above step gives you an URL 
1. copy the FULL URL and paste it in a web browser (chrome or firefox)
2. open a new terminal by right clicking and left clicking docker quickstart terminal
``` 
   docker-machine ls
   docker-machine ip default
```
2. Replace the contents within and the brackets with the IP number and hit ENTER
