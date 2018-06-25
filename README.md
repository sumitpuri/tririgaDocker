# Instructions to launch TRIRIGA Docker Image Locally

### Step 1: 
Download and install Docker for [Windows](https://store.docker.com/editions/community/docker-ce-desktop-windows) or [Mac](https://store.docker.com/editions/community/docker-ce-desktop-mac)

### Step 2: 
Click ‘Create a Docker ID’ to setup an account. 

### Step 3: 
Join [#tririga_docker](https://ibm-tririga.slack.com/messages/CBBLDA5QU/) channel on Slack using IBM w3 credentials.

Post your Docker ID to get access to TRIRIGA Image.

### Step 4: 
":thumbsup:" reaction on the post indicates the Docker ID has been provisioned with access to tririga repository. 

Proceed below once access is granted.

### Step 5: 
Open terminal (on Mac) or command prompt (on windows) and run

docker pull ibmtririga/tririga_10.5.3.1:v3.5.3.3_51528

where, <br />
10.5.3.1 is Application Version <br />
3.5.3.3 is Platform Version <br />
51528 is Build number of the Platform <br />
Wait for pull to be completed

### Step 6: 
Run

docker run -ti -p 8001:8001 --name tririga_10.5.3.1 -h tririgaDocker ibmtririga/tririga_10.5.3.1:v3.5.3.3_51528 bash

### Step 7: 
Run

./runtririga.sh

### Step 8: 
Open any browser and click http://localhost:8001/index.html to launch TRIRIGA locally.



#### For any questions, post on [#tririga_docker](https://ibm-tririga.slack.com/messages/CBBLDA5QU/) Slack channel or contact:

Sumit Puri <br />
TRIRIGA Application Architect <br />
sumit.puri@us.ibm.com

Ray Tripamer <br />
TRIRIGA Technical Architect <br />
ray.tripamer@ibm.com

