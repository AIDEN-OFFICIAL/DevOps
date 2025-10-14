# what is Docker?
Reasons :
- One or more files missing
- software version mismatch
- different configuaritons across different machines
- suppose think like Docker is a package , and it consis tof your applications  nodejs , mongo db and the whole app with a fixed version
- docker-compose up : to add a  application into the container (isolated environment, where we can run any number of application versions)
- we can easily remove any app vversion without causing any issues in one go.
- suppose we have the tension of unknowlingly delete any dependencies, that we think would be used in one version that we would like to remove, but at the same time we are afraid if its something that shouldnt be removed , in such a situation docker helps us sort out the dependencies specific to different versions of apps and remove those
docker-compose down --rmi all
- a virtual machine: is a n abstraction of a machine (physical hardware)
