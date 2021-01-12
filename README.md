# SimpleK8s

This project demonstrate basic use of kubernetes.

The client pod consists of one single container which image is built in previous exercises.

The configuration of pod and services tells kubernetes engine how to create containers and how to connect to it.

## Concept of _*Pod*_

A pod is a minimal deployable unit in kubernetes node. We use pod to run one or more containers.

## What is _*Service*_?

A service in kubernetes cluster sets up sets up networking properties.

The list of properties depends on the type of service.

A NodePort service exposes a container to the outside world.

A pod is running on local kubernetes node. A NodePort service sets up communication between the pod and outside world.

The `selector` section defines how to find matching pod.

The `ports` section defines ports used for communication. `targetPort` specifies the port to talk to the target pod.

The `port` allow other pods to talk to this pod via the service.

The `nodePort` is the port outside world use to communicate with the pod.

## Start `minikube`

Run this command: `minikube start`.

This will create a virtual machine running as a *node*. We will then use control command to start a *pod*.
