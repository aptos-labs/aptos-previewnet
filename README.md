Hey all, thank you for participating as a validator node for PreviewNet! Please follow the instructions here [ADD LINK] to setup your node and connect to testnet.

Build Info:
- The docker image tag to use is: `preview_0a0cb31d76063d8ac4a8502c2afc2e8acd6941f4`
- Dockerhub Link: [aptoslabs/validator:preview_0a0cb31d76063d8ac4a8502c2afc2e8acd6941f4](https://hub.docker.com/layers/aptoslabs/validator/preview_0a0cb31d76063d8ac4a8502c2afc2e8acd6941f4/images/sha256-69421bdfdee3e34a8e2d0de5ee07b6db55514da393b32cca21d5fd22e910e98f?context=explore)
- Sha 256 Digest for the docker image is `sha256:69421bdfdee3e34a8e2d0de5ee07b6db55514da393b32cca21d5fd22e910e98f`

Genesis & Waypoint:
- Sha 256 for genesis blob is: `83f0ed223fe5e88328038ba49ce613c3b10d72b5eb6cc58a50f417275f8b46e7`
- Waypoint is: `0:aa7a0f5f2d0d6bf10035bcf39729927e151b4b52fe2bd1637e5a7523f186f75e`
- Both have been provided in this repo as `waypoint.txt` and `genesis.blob`


Let us know if you have any questions, and looking forward to see your node coming online!

# Retrieve latest framework

Pull the latest docker image build and copy it out

```
export TOOLS_IMAGE=<YOUR TOOLS IMAGE HERE>
docker run -it ${TOOLS_IMAGE} bash

# in a separate terminal
docker cp `docker container ls | grep ${TOOLS_IMAGE} | awk '{print $1}'`:/aptos-framework/move/head.mrb framework.mrb 
```
