# coreservices
Service files for coreOS to run webapp

Step 1: Get the docker image onto dockerhub (privately if it contains sensitive info but will need to be logged into docker on coreos)

Step 2: Clone onto the coreOS machine:

>`git clone https://github.com/darcys22/coreservices.git`
>`cd coreservices`
>`fleetctl submit *`
>`fleetctl start *`
