Hey all, thank you for participating as a validator node for PreviewNet! Please follow the instructions here [ADD LINK] to setup your node and connect to testnet.
- The docker image tag to use is [IMAGE TAG]
- Sha256 for the docker image is [DOCKER SHA-256]
- Sha 256 for genesis blob is [GENESIS SHA-256]
- Waypoint is [WAYPOINT]

Let us know if you have any questions, and looking forward to see your node coming online!

# Retrieve latest framework

Pull the latest docker image build and copy it out

```
export TOOLS_IMAGE=<YOUR TOOLS IMAGE HERE>
docker run -it ${TOOLS_IMAGE} bash

# in a separate terminal
docker cp `docker container ls | grep ${TOOLS_IMAGE} | awk '{print $1}'`:/aptos-framework/move/head.mrb framework.mrb 
```
