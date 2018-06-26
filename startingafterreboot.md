Rebooting the machine will cause to stop the TRIRIGA Container. Follow below steps to bring it back up.

### Step 1: 

Open Terminal (on Mac) or Command Prompt (on Windows 10) and run

docker ps -a 

It displays list of all containers. 
There should be ONLY one TRIRIGA container in the result. 

### Step 2: 

Note down the Image ID of the TRIRIGA Container being worked upon. 

### Step 3: 

Run

docker start <Image ID> (without <>)

It starts the TRIRIGA Container.

### Step 4: 

Run

docker attach <Image ID> (without <>)

### Step 5:

Run 

[root@tririgaDocker /]# ./runtririga.sh
