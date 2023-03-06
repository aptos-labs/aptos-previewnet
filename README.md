Hey all, thank you for participating as a validator node for PreviewNet! Please follow the instructions here [ADD LINK] to setup your node and connect to testnet.

Build Info:
- The docker image tag to use is: `preview_0a0cb31d76063d8ac4a8502c2afc2e8acd6941f4`
- Dockerhub Link: [aptoslabs/validator:preview_0a0cb31d76063d8ac4a8502c2afc2e8acd6941f4](https://hub.docker.com/layers/aptoslabs/validator/preview_0a0cb31d76063d8ac4a8502c2afc2e8acd6941f4/images/sha256-69421bdfdee3e34a8e2d0de5ee07b6db55514da393b32cca21d5fd22e910e98f?context=explore)
- Sha 256 Digest for the docker image is `sha256:69421bdfdee3e34a8e2d0de5ee07b6db55514da393b32cca21d5fd22e910e98f`

Genesis & Waypoint:
- Sha 256 for genesis blob is: `7e7f32dab96c312e2a03d0402178a150a39012a31359f38ff2f6d38165a9d235`
- Waypoint is: `0:2d6098a34ad863737a21a5e2e9affe0192aaded460bf7429a0ae1c0bb6d99a6f`
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
