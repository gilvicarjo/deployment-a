# To Run Everything Here

## Jenkins Pipeline Deploy Service A

### Setup Minikube 
> minikube start --cpus 2 --memory 2048 --driver=hyperkit

### Run Jenkins Container
> docker run -d --name jenkins -p 8080:8080 -p 50000:50000 -v jenkins_data:/var/jenkins_home --network minikube jenkins/jenkins:lts

- After finish a common Jenkins setup, you will just need to switch on .kube/config the .crt and .key by their base64 encoded data to link Jenkins with you K8s Cluster when configuring Jenkins Clouds.

### Take a Look at the Jenkins Container Logs 
> docker logs -f jenkins

### Now Update Just Stage Branch
