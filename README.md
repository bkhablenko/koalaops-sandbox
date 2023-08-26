# koalaops-sandbox

This repo was created with [KoalaOps](https://app.koalaops.com/)

## Description

A sandbox project to try out KoalaOps 🐨

## How to run locally?

```
mvn quarkus:dev
```

## How to run with Docker?

```
docker build -t koalaops-sandbox:latest .
docker run -p:5030:8080 koalaops-sandbox:latest
```

Server will listen at http://localhost:5030

## K8s Configuation and Deployment

On service creation Koala created for you 3 k8s resources to use:

- deployment.yaml
- service.yaml
- ingress.yaml

Those are located in the [deploy](deploy) directory and should be applied with kustomize. For example:

### In Production run: 

```
cd deploy
kubectl apply -k overlays/prod
```

### In Dev run: 

```
cd deploy
kubectl apply -k overlays/dev
```

