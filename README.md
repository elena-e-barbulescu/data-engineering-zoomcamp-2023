# Data Engineering Zoomcamp 2023
Data Engineering ZoomCamp with Alexey Grigorev 2023 (https://github.com/DataTalksClub/data-engineering-zoomcamp)

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

## Week 1 - Basic Setup
Steps:
- 1 - Introduction to Docker  (see video provided in Resources)
- 2 - Clone the github repo from DataTalks Github (https://github.com/DataTalksClub/data-engineering-zoomcamp) at command line
- 3 - Access of week 1 folder locally on Gitbash

![image](https://user-images.githubusercontent.com/68255140/212756449-39a696db-ced5-4ce2-b06f-8efb4559816e.png)

- 4 - [Installing Docker on Windows](https://docs.docker.com/desktop/install/windows-install/)


4 - Installing Python 3.9 in the docker container
$ docker run -it python:3.9


Resources:
- [Docker + SQL notes (Provided by Alexey)](https://docs.google.com/document/d/e/2PACX-1vRJUuGfzgIdbkalPgg2nQ884CnZkCg314T_OBq-_hfcowPxNIA0-z5OtMTDzuzute9VBHMjNYZFTCc1/pub)

>> Video - [Introduction to Docker](youtube.com/watch?v=EYNwNlOrpr0&list=PL3MmuxUbc_hJed7dXYoJw8DoCuVHhGEQb) (24 minutes)
