dock commands: [in28minutes / devops-master-class](https://github.com/in28minutes/devops-master-class/tree/master/docker#commands)

url:    localhost:5000

img:
docker run -p 5000:5000 in28min/hello-world-python:0.0.1.RELEASE
- https://hub.docker.com/r/in28min/hello-world-python:0.0.1.RELEASE
- repository: in28min/hello-world-python
- tags (version): 0.0.1.RELEASE
- -p: --publish
- HostPort:ContainerPort (mapping)
- the container is **tied** to the terminal
docker run -p 5000:5000 in28min/hello-world-java:0.0.1.RELEASE
docker run -p 5000:5000 in28min/hello-world-nodejs:0.0.1.RELEASE

docker run -p -d 5000:5000 in28min/hello-world-python:0.0.1.RELEASE
- -d: --detach (detach mode)
- in detach mode, multiple container can be launched in one terminal or a command prompt ta
- it will return an id of container

dock logs [container id]
- show the logs based on container id
- only first 4 letters of container id is required (short cut)
- -f (--follow), the log will be tied to the termial (will show logs of one conatiner in real-time)
- ctrl+c will detach the logs, but the container remains runing

ctrl + c : Terminate Container

docker image
- list all images locally

docker container ls
- list containers running

clear