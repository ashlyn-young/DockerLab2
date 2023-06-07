Deploy your stack or docker-compose.yaml file : 
    docker deploy -c docker-compose.yaml <imagename>-stack
    (type into terminal/command line)

Scale your first stack into 7 instances/replicas :
    Within yaml file :
        <Deploy:
            replicas: 'number'>
        (Replace 'number' with the amount of replicas you're wanting to create.)
    From command line :
        docker service scale <imagename>-stack_websitename='number'
        (type into terminal/command line, replace 'number' with desired amount of replicas.)

Remove stack / delete containers:
    Delete containers: 
        docker stop <Container_ID>
        docker rm <Container_ID>
        (If container is in a stack this will only stop and remove that specific container, however a new one will be created to continue running the stack.)
    
    Remove stack :
        docker stack rm <imagename>-stack