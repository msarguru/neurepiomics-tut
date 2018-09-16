# "Pracital session on "Beyond Genome-wide Association Studies"
## What this session is about?
Genome-wide association studies (GWAS) have identified multiple genetic variants  associated with complex traits, many efforts have shown that a sizeable fraction of the pheotypic variance is explained by the genetics. With the recent trend of making these summary measures publicly available it has opened new avenues to test overlap between these complex traits from the genetics standpoint. In this session, we will explore some of the follow-ups strategy to infer biological evidence from otherwise purely statistical signals. 
## What you need?
To avoid any possible delays/hiccups in running the analysis from a command line (which is the ideal way anyways!!). 
This DIY session instead will use Jypternotebook (web interface) in running the analysis. By this means, participants can focus more on the analysis (then troubleshooting or setting things up)  
## Requirements:
1. Docker software (that creates a VM machine)
2. Docker image file (that contains all the necessary files to run the analysis), it is a gzipped (*.gz) file and can be downloaded through the following google drive link
http://bit.ly/2OcL8Mt

# Strongly advise to download this docker image file, prior to the session!!!

## Installing docker:
### For mac:
1. This should be a straightforward installation https://download.docker.com/mac/stable/Docker.dmg
2. for more info in installation: https://store.docker.com/editions/community/docker-ce-desktop-mac
3. After installing;
Open terminal, and try out some Docker commands.

 ```
 docker version 
 docker run hello-world 
```
### For windows 10 or less:
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
## FOR MACBOOK / Windows USERS
## STEP1: open terminal (if you have installed standard Docker) or the Docker Quickstart terminal (if Docker toolbox)
### RUN

```
   #see if there is any image already
   docker ps
   #load docker image file with,
   docker load < <downloaded tar.gz file>
   #confirm that the image is loaded with,
   docker images
   #run the docker image with,
   docker run -it --rm --user root -p 8888:8888 bioinfo_ms_tut:finalv2
   #start the notebook for interactive service with,
   jupyter notebook --ip 0.0.0.0 --no-browser --allow-root
```
## STEP 2: Above step gives you an URL 
1. copy the URL and paste it in a web browser (chrome or firefox)
2. Replace the contents within and the brackets with **localhost** 
3. if this does not work replace with 

