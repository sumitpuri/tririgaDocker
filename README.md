# TRIRIGA 10.6 Docker Image local install using Command Line

### Step 1: 
Download and install Docker for [Mac](https://download.docker.com/mac/stable/Docker.dmg) or [Windows 10](https://download.docker.com/win/stable/Docker%20for%20Windows%20Installer.exe) 

### Step 2: 
Click [here](https://hub.docker.com/?next=https%3A%2F%2Fhub.docker.com%2F) to create a Docker ID.

### Step 3: 
Join [#tririga_docker](https://ibm-tririga.slack.com/messages/CBBLDA5QU/) channel (in TRIRIGA Workspace) on Slack using IBM w3 credentials.

Post your Docker ID to get access to TRIRIGA Image.

### Step 4: 
":thumbsup:" reaction on the post indicates the Docker ID has been provisioned with access to tririga repository. 

Proceed below once access is granted.

### Step 5: 
Open Terminal (on Mac) or Command Prompt (on Windows 10) or Docker Quickstart Terminal (on Windows 7).<br />
Type the command after dollar sign and hit enter:

```
$ docker login
```


```
$ docker pull ibmtririga/tririga_10.6
```

Wait for pull to be completed

### Step 6: 
Run

```
$ docker run -ti -p 8001:8001 --name tririga_10.6 -h tririgaDocker ibmtririga/tririga_10.6 ./runtririga.sh
```

Note: This command needs to be run only once for installation. 

### Step 7: 
Open browser and click http://localhost:8001/index.html to launch TRIRIGA locally. 

username: system <br />
password: admin

<br />

### Useful Docker commands

To relaunch TRIRIGA Docker Container next time, run below commands in succession:
```
$ docker start tririga_10.6
$ docker attach tririga_10.6
$ ./runtririga.sh
```

To Delete Docker Container:
```
$ docker ps -a (list all docker containers)
$ docker rm -f <container-id or container-name> (delete specified docker container)
```
To Delete Docker Image:
```
$ docker images (list all docker images)
$ docker rmi -f <image-id> (delete specified docker image)
```

To Start/Stop Containers:
```
$ docker start <container-id or container-name> (start docker container)
$ docker stop <container-id or container-name> (stop docker container)
```

To see Container logs:
```
$ docker logs -f <container-id or container-name> (tail docker container logs)
```


<br />

#### For any questions, post on [#tririga_docker](https://ibm-tririga.slack.com/messages/CBBLDA5QU/) Slack channel or contact:

Sumit Puri <br />
TRIRIGA Application Architect <br />
sumit.puri@us.ibm.com

Ray Tripamer <br />
TRIRIGA Technical Architect <br />
ray.tripamer@ibm.com

