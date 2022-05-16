# Kuberntes Microservice Application

## How to run it?

Execute the following command

```sh
kubectl create -f .
```

## How to perform a Rolling Update strategy?

```sh
kubectl get deployment
kubectl delete deploy\name_deploy
kubectl create -f .\deploy_name.yaml --record 
kubectl rollout history deploy\name_deploy
kubectl apply -f .\name_deploy.yaml --record
kubectl rollout history deploy\name_deploy --revision #_of_revision
kubectl describe deploy\name_deploy 
```

## How to perform a Rollout strategy?

```sh
kubectl rollout history deploy\name_deploy
kubectl rollout undo deploy/name_deploy
```

Execute the following command

```sh
kubectl create -f .
```

## How to access the application?

Check the NodePort created by executing the command, you will notice a NodePort Service created with a specific port from 30000-32767

```sh
kubectl get services
```

Access the application by concatenating the IP of the node (or localhost if running a local instance)

```sh
[IP_ADDRESS / localhost]:[NODEPORT_PORT]
```

## Architecture Diagram

![Microservice Application](/application_diagram.png "Microservice Application")
