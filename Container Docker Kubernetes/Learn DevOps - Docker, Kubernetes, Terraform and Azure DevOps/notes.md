container: when an image is running, it's called a container

image: a static version either on the (hub) reposity or at local

bridge network: when we run a container, it is part of **internal Docker network**, called a bridge network
- by default, all containers run inside the bridge network
- not be able to access the container, unless the port is exposed outside
- (Mapping) HostPort:ContainerPort. 

launch
- a separate terminal tab or a command prompt tab
- same tab
