# Instructions to launch TRIRIGA Docker Image Locally

### Step 1: 
Download Docker for your operating system [here](https://www.docker.com/community-edition).

Click ‘Create a Docker ID’ to setup an account. 

### Step 2: 
Join [#tririga_docker](https://ibm-tririga.slack.com/messages/CBBLDA5QU/) channel on Slack.

Post your Docker ID to get access to TRIRIGA Image.

### Step 3: 
Once ":thumbsup:" reaction is received on the post [indicating the Docker ID has been provisioned with access to tririga repository], proceed below.

### Step 4: 
Open terminal (on Mac) or command prompt (on windows) and run

$ docker pull ibmtririga/tririga_10.5.3.1:v3.5.3.3_51528

Wait for pull to be completed

### Step 5: 
$ docker run -ti -p 8001:8001 --name tririga_10.5.3.1 -h tririgaDocker ibmtririga/tririga_10.5.3.1:v3.5.3.3_51528 bash

### Step 6: 
run ./root/runtririga.sh

### Step 7: 
Open any browser and click http://localhost:8001/index.html to launch TRIRIGA on your local machine.

#### For any questions, contact:

Sumit Puri <br />
TRIRIGA Application Architect <br />
sumit.puri@us.ibm.com

Ray Tripamer <br />
TRIRIGA Technical Architect <br />
ray.tripamer@ibm.com

