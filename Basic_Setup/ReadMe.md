
# Data Engineering Zoomcamp 2023
Data Engineering ZoomCamp with Alexey Grigorev 2023 (https://github.com/DataTalksClub/data-engineering-zoomcamp)

# Week 1 - Basic Setup 

## The Tools
**Docker**:   allows for "containerization" of what's needed to run a particular application (ie. OS, system-level libraries, python, etc)

We can have multiple containers on the host computer.

The container:
> - Runs on a host machine.
> - Completely isolated from the host environment.
> - Can have the Unbuntu 18.0 while your host is running on Windows
> - Is great on running locally for experiments, integration tests, CID/CD, batch jobs, Spark, servless, etc.

Why it's important to use Docker?
- Reproducibility
- Local experiments
- Integration tests (CI/CD)
- Taking the image and running on the cloud

**Postgres** is used for practicing with SQL, and as a general purpose database, and can be used as a data warehouse as well.
> - Set up locally to practice SQL and test things before doing this in the cloud.

## Google Platform Setup
Video [here](https://www.youtube.com/watch?v=ae-CV2KfoN0&list=PL3MmuxUbc_hJed7dXYoJw8DoCuVHhGEQb).

1 - Setting up a free account on Google Cloud Platform
![image](https://user-images.githubusercontent.com/68255140/212763494-f5530d47-5a77-478b-99a5-b5cf3e5a8e60.png)
2 - [Create the SSH Key](https://cloud.google.com/compute/docs/connect/create-ssh-keys)

![image](https://user-images.githubusercontent.com/68255140/212764857-771982e7-34ed-44b7-a27b-c8284e773afe.png)

![image](https://user-images.githubusercontent.com/68255140/212765077-6ee17494-5dae-402c-8c77-af8e45223508.png)

This creates the private and the public keys  (to print the public SSH key - "cat decampssh.pub").  

The public key gets added to the "Metadata" setting section of the "Computer Engine" menu of the Google Cloud Platform.  

3 - Creating the BOOT Disk requirements for Ubuntu
![image](https://user-images.githubusercontent.com/68255140/212767437-a7349651-caf1-4343-bba1-691986cf02c3.png)

4 - Starting the instance and pulling the External IP
$ ssh -i ~/.ssh/<privatesshkey> <username>@<externalIP>

![image](https://user-images.githubusercontent.com/68255140/212770060-f2f1ab25-604f-473a-bf5d-ab524094f8f1.png)

5 - Checking what type of machine we're working with:

![image](https://user-images.githubusercontent.com/68255140/212770197-7605fe29-47bc-4ce3-80a0-5eb80a50f76b.png)

## Installing Anaconda - [Linux Version](https://www.anaconda.com/products/distribution)

1 - Installing Anaconda Linux version on the virtual environment

![image](https://user-images.githubusercontent.com/68255140/212770742-e73eae51-ce74-47bd-ac19-ac84b187dc24.png)

![image](https://user-images.githubusercontent.com/68255140/212771299-45cf1a01-8805-4718-b78d-3e865b54fd22.png)


2 - Configure connection to the server

![image](https://user-images.githubusercontent.com/68255140/212771468-f2f371bd-3308-43bd-bda2-116240b60317.png)

>> Make sure to install the following extension: https://code.visualstudio.com/docs/remote/ssh-tutorial

![image](https://user-images.githubusercontent.com/68255140/212776875-2aa6e241-1926-44ef-bd02-b668fe4b507a.png)

3 - Checking for python and pandas version

![image](https://user-images.githubusercontent.com/68255140/212777008-2bd20687-4927-4a54-b8ae-47d440b290d2.png)

Ctrl+D to exit

4 - Install Docker

>> first do:  sudo apt-get update  | to get a list of packages
>> then do:  sudo apt-get install docker.io

5 - Remote SSH Extension - Connect to Remote Window - Connect to Host
- a drop down menu with the configured file should be existing 

![image](https://user-images.githubusercontent.com/68255140/212778031-49d2eb68-1358-42fd-91cb-de56b66ad124.png)

![image](https://user-images.githubusercontent.com/68255140/212778172-616d669d-35f2-49ba-88bf-a3460559e51f.png)

6 - Cloning the DEZoomcamp repo from DataTalks

![image](https://user-images.githubusercontent.com/68255140/212778429-ea59ccc1-8821-4360-9e9d-b236ed1dac48.png)

>> using the following link for the commands:  github.com/sindresorhus/guides/blob/main/docker-without-sudo.md
>> and when in doubt Ctrl+D, logout and log backin
>> reactivating with ssh de-zoomcamp - the config file already established

![image](https://user-images.githubusercontent.com/68255140/212778929-4e55fd66-c8d6-4ec1-bac0-0aca9c1266c8.png)

7 - Run the following:   docker run -it ubuntu bash

![image](https://user-images.githubusercontent.com/68255140/212779036-b596d04f-f71b-4b9f-817f-eb407024a8a6.png)

8 - Install Docker Compose

https://github.com/docker/compose

https://github.com/docker/compose/releases

Create the directory for all executable files

![image](https://user-images.githubusercontent.com/68255140/212779548-059f7d6c-99b9-4d1b-ab0f-84fa852911d5.png)

Making executable and checking version

![image](https://user-images.githubusercontent.com/68255140/212779643-dd53f9af-c7da-488c-a7f6-4d8829f8ed25.png)

9 - Make it visible from any director and have to add this to the path variable

Open the bash receive file  - (in the repo directory not in bin) - "nano .bashrc"
Crtl+O to save, then enter, and then 

![image](https://user-images.githubusercontent.com/68255140/212780077-f854b4bc-3323-4a53-970a-d733b560de4a.png)

10 - Downloading the images for PgAdmin and Postgres

![image](https://user-images.githubusercontent.com/68255140/212780219-9774ef27-5c32-429e-945d-0174363bf960.png)

run : docker-compose up -d (in detached mode)
  
  ![image](https://user-images.githubusercontent.com/68255140/212780546-842503c0-ce02-40f0-9182-afa860dbb299.png)


11 - Install PGCli

  ![image](https://user-images.githubusercontent.com/68255140/212780598-f4ec8af2-e8aa-41f3-bb64-e001ee2ae1ca.png)

12 - Get taxi data (root password = root)
  
 ![image](https://user-images.githubusercontent.com/68255140/212780877-62bd6827-6641-4afa-a3e9-a3393077be8b.png)

  it's WORKING!
  
  ![image](https://user-images.githubusercontent.com/68255140/212780952-914197d7-c902-4e12-adac-09ac95d64430.png)

  
13 - Uninstal pgcli and resinstall using conda
  
  ![image](https://user-images.githubusercontent.com/68255140/212781130-0e38e962-dede-46f9-aef9-0f26a6633e49.png)

  ![image](https://user-images.githubusercontent.com/68255140/212781214-fb7ea156-6c37-4ec2-9cac-2ec81fcd91d5.png)

  Oh yea, this was fun, conda solving the environment as it was attempting to install pgcli
  
  ![image](https://user-images.githubusercontent.com/68255140/212782720-d4149c05-d6db-4c41-b7f3-d53d54086b6c.png)

  IT WORKED again!
  
  ![image](https://user-images.githubusercontent.com/68255140/212782916-5c3ed305-6a41-4c04-854d-30e2f076fd81.png)

14 - Forward the current port locally so that it can be interacted with locally
  
 ![image](https://user-images.githubusercontent.com/68255140/212783084-160b550c-42c6-4d1b-abea-82a37778338d.png)

  ![image](https://user-images.githubusercontent.com/68255140/212783135-5d7021a4-4082-4d5a-9c14-64cd44ff1e98.png)

  This [Resource](https://github.com/DataTalksClub/data-engineering-zoomcamp/tree/main/week_1_basics_n_setup/2_docker_sql) is the best thing I've ever used!
  
 15 - Lastly, connecting via the terminal with command:  pgcli -h localhost -U root -d ny_taxi
  
 ![image](https://user-images.githubusercontent.com/68255140/212784211-c3cd4f8f-3fae-4476-9ae7-2e120cea601d.png)

  
  
## Remote Setup
Steps:
- 1 - Introduction to Docker  (see video provided in Resources)
- 2 - Clone the github repo from DataTalks Github (https://github.com/DataTalksClub/data-engineering-zoomcamp) at command line
- 3 - Access of week 1 folder locally on Gitbash

![image](https://user-images.githubusercontent.com/68255140/212756449-39a696db-ced5-4ce2-b06f-8efb4559816e.png)

- 4 - [Installing Docker on Windows](https://docs.docker.com/desktop/install/windows-install/)



Installing Python 3.9 in the docker container
$ docker run -it python:3.9


Resources:
- [Docker + SQL notes (Provided by Alexey)](https://docs.google.com/document/d/e/2PACX-1vRJUuGfzgIdbkalPgg2nQ884CnZkCg314T_OBq-_hfcowPxNIA0-z5OtMTDzuzute9VBHMjNYZFTCc1/pub)

>> Video - [Introduction to Docker](youtube.com/watch?v=EYNwNlOrpr0&list=PL3MmuxUbc_hJed7dXYoJw8DoCuVHhGEQb) (24 minutes)
