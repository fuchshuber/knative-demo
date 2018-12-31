# knative-demo

## Installing Knative

Follow these step-by-step guides for setting up Kubernetes and installing Knative components as a local demo showcase:
* Minikube: https://github.com/knative/docs/blob/master/install/Knative-with-Minikube.md
* Docker for Mac: https://github.com/knative/docs/blob/master/install/Knative-with-Docker-for-Mac.md
* MiniShift: https://github.com/knative/docs/blob/master/install/Knative-with-Minishift.md

## Deploy pre-built application

Let's deploy an existing public Docker image as an autoscaling stateless application to Knative:

```
kubectl create ns helloworld

knctl deploy \
      --namespace helloworld \
      --service hello \
      --image gcr.io/knative-samples/helloworld-go \
      --env TARGET=Rev1
```

## More informations

* Deploying 12-factor apps to Knative: https://starkandwayne.com/blog/deploying-12factor-apps-to-knative/
* Building Containers with Kubernetes and Knative: https://boxboat.com/2018/08/10/building-containers-with-kubernetes-and-knative/
