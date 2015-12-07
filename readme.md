# Core Services
Service files for coreOS to run webapp

Step 1: Get the docker image onto dockerhub (privately if it contains sensitive info but will need to be logged into docker on coreos)

Step 2: Clone onto the coreOS machine:

>`git clone https://github.com/darcys22/coreservices.git`


>`cd coreservices`


>`fleetctl submit *`


>`fleetctl start *`


Notes: The haproxy currently uses the old pre 1.9 docker0 ip address for etcd2. needs to be updated dynamically to whatever docker0 is from `ip addr show` 
wont connect to etcd 

Steps to getting a website up and running:
1: Have a github repo that works 


2: build a docker image using that webserver


3: change the webapp.service to pull from that docker repo


4: start these services


5: update nameservers to digital ocean

If you want SSL then use the darcys22/haproxyssl image (Uncomment) but you need to have your certs in the ~/config/certs file because docker mounts that to the loadbalancer
