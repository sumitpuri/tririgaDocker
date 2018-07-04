# Instructions to launch TRIRIGA 10.5.3.2 Docker Image Locally

### Step 1: 
Download and install Docker for [Mac](https://download.docker.com/mac/stable/Docker.dmg) or [Windows 10](https://download.docker.com/win/stable/Docker%20for%20Windows%20Installer.exe) or [Windows 7](https://download.docker.com/win/stable/DockerToolbox.exe).

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
$ docker pull ibmtririga/tririga_10.5.3.2:v3.5.3.3_51528
```

where, <br />
10.5.3.2 is Application Version <br />
3.5.3.3 is Platform Version <br />
51528 is Build number of the Platform <br />
Wait for pull to be completed

### Step 6: 
Run

```
$ docker run -ti -p 8001:8001 --name tririga_10.5.3.2 -h tririgaDocker -d ibmtririga/tririga_10.5.3.2:v3.5.3.3_51528 ./runtririga.sh
```

Note: This command needs to be run only once for installation. 

### Step 7: 
Open browser and click http://localhost:8001/index.html to launch TRIRIGA locally. 

username: system <br />
password: admin

<br />

### Other useful Docker commands

To relaunch TRIRIGA Docker Container after machine reboot, run 
```
$ docker start tririga_10.5.3.2
```

To view TRIRIGA Docker Container logs, run
```
$ docker logs -f tririga_10.5.3.2
```
To list all Docker Images
```
$ docker images
```
To list all Docker Containers
```
$ docker ps -a
```
To delete Docker Container and Images
```
$ docker rm -f <container-name>
$ docker rmi -f <image-id>
```


<br />

#### For any questions, post on [#tririga_docker](https://ibm-tririga.slack.com/messages/CBBLDA5QU/) Slack channel or contact:

Sumit Puri <br />
TRIRIGA Application Architect <br />
sumit.puri@us.ibm.com

Ray Tripamer <br />
TRIRIGA Technical Architect <br />
ray.tripamer@ibm.com

