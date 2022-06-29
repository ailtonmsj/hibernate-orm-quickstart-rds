# Quarkus demo: Hibernate ORM and RESTEasy

This is a minimal CRUD service exposing a couple of endpoints over REST,
with a front-end based on Angular so you can play with it from your browser.
To use in an Kubernetes Cluster in AWS to access a AWS Aurora MySQL

## To Build and Push to dockerhub:
```
docker buildx build -f src/main/docker/Dockerfile.jvm -t <YOUR_USER>/amazon-rds-quickstart:<TAG> --push .
```
example:
```
docker buildx build -f src/main/docker/Dockerfile.jvm -t ailtonmsj/amazon-rds-quickstart:1.0.2 --push .
```

## To deploy (EKS Cluster)
```
kubectl apply -f ./src/main/kubernetes/
```

## Requirements

1. An Aurora MySQL Database accessible from Cluster (carefull about VPC)
2. Service Mesh running on EKS


