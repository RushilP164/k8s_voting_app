# Introduction
This is a basic K8s structure for microservice application. Advanced concepts will be added in future.


## Installation

K8s dependencies must be installed to run this applications. 

## Overview
### 1. Deployments
- postgres
- redis
- voting-app - frontend - allows to vote
- result-app - frontend - allows to see the result
- worker-app - backend - no outside access
### 2. Services
- redis(ClusterIP)
- postgres (ClusterIP)
- result-service (NodePort)
- voting service (NodePort) ​

## Steps
1. Create deployments
```bash
cd deployments
```
```bash
kubectl create -f .
```
2. Create Services
```bash
cd services
```
```bash
kubectl create -f .
```
3. Run Services
```
minikube service voting-service --url
minikube service result-service --url
```
4. Hit the returned URLs in the browser and we are good to go.
