[![CircleCI](https://circleci.com/gh/db7gs/Udacity-project5/tree/master.svg?style=svg)](https://circleci.com/gh/db7gs/Udacity-project5/12)

# Udacity-project5
This is a project for udacity nanodegree Cloud dev-ops Engineer about to use Docker.

### DESCRIPTION
In this project I applied all the skills I have learned to setup a Machine Learning Microservice API into Docker.


## The files included are:
```sh
* /.circleci : CircleCI configuration file for running the tests.
* /model_data : all the relevant data for the model.
* /output_txt_files : Output log files with the result of the model run execution 
* Dockerfile : Dockerfile for building the image 
* Makefile : includes instructions on environment setup and lint tests
* app.py : Python  app that serves our predictions. 
* make_prediction.sh : Send a request to the app to get a prediction.
* requirements.txt : Install any dependencies 
* run_docker.sh : file to be able to get Docker run
* run_kubernetes.sh : file to run the app in kubernetes
* upload_docker.sh : file to upload the image to docker

## CircleCI Integration

This repository has been verified with CircleCI

### SETUP
After clonnig the project follow this steps:

Create (and activate) a new environment, named .devops with Python 3
```
python3 -m venv ~/.devops
source ~/.devops/bin/activate
```

At this point your command line should look something like:

```
(.devops) <User>:project-ml-microservice-kubernetes<user>$
```

Installing dependencies via project Makefile

```
make install
```

### RUNNING THE APP
To run the APP into a terminal 

```
./run_docker.sh
```

After a brief waiting period, you should see messages indicating a successful build, along with some indications that your app is being served on port 80, you will see:

```
Successfully built <build id>
Successfully tagged <your tag>
```

into other tab open a new terminal and run

```
./make_prediction.sh
```
In the prediction window, you should see the value of the prediction, and in your main window, where it indicates that your application is running, you should see some log statements print out. You’ll see that it prints out the input payload at multiple steps; when it is JSON and when it’s been converted to a DataFrame and about to be scaled.

License
-------
udacity-IaC is a public domain work, dedicated using
[CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/). Feel free to do
whatever you want with it.
