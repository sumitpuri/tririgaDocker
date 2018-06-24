# Instructions to launch TRIRIGA Docker Image Locally

### Step 1: 
Download Docker for your operating system [here](https://www.docker.com/community-edition).

Click ‘Create a Docker ID’ to setup an account. 

### Step 2: 
Join [#tririga_docker](https://ibm-tririga.slack.com/messages/CBBLDA5QU/) channel on Slack using IBM w3 credentials.

Post your Docker ID to get access to TRIRIGA Image.

### Step 3: 
":thumbsup:" reaction on the post indicates the Docker ID has been provisioned with access to tririga repository. Proceed below once access is granted.

### Step 4: 
Open terminal (on Mac) or command prompt (on windows) and run

$ docker pull ibmtririga/tririga_10.5.3.1:v3.5.3.3_51528

where, <br />
10.5.3.1 is Application Version <br />
3.5.3.3 is Platform Version <br />
51528 is Build number of the Platform <br />
Image is ~18GB. Wait for pull to be completed

### Step 5: 
$ docker run -ti -p 8001:8001 --name tririga_10.5.3.1 -h tririgaDocker ibmtririga/tririga_10.5.3.1:v3.5.3.3_51528 bash

### Step 6: 
run ./root/runtririga.sh

### Step 7: 
Open any browser and click http://localhost:8001/index.html to launch TRIRIGA locally.

#### For support, post on [#tririga_docker](https://ibm-tririga.slack.com/messages/CBBLDA5QU/) Slack channel or contact:

Sumit Puri <br />
TRIRIGA Application Architect <br />
sumit.puri@us.ibm.com

Ray Tripamer <br />
TRIRIGA Technical Architect <br />
ray.tripamer@ibm.com

