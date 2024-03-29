# Continuous local Kubernetes app development using *Skaffold*
This guide walks you thru continuous local application development workflow using *Skaffold*, container tool from Google. This guide includes lab(s) that demonstrate frictionless developer experience for container application running on local Kubernetes cluster.

## What is *Skaffold*
It is a command line tool that helps iterate an application. It deploys application on either local or remote Kubernetes cluster. Basically, this OSS tool detect changes in your source code as well as the dependencies of your docker images. And automatically triggers build, push & deploy to local / remote Kubernetes cluster.

## Focus
This guide plus lab(s) focuses on local development context rather than remote context such as automated CI & CD pipeline. Advanced workflow will be covered separately.

> Consider this as *Skaffold* getting started guide for local application development

## Target audience
Target audience for this guide is primarily developer community. Developers who wants to employ simple, repeatable & yet flexible tool for building and deploying applications for Kubernetes.

> Kubernetes app developer, DevOps specialist who wants to understand & establish automated CI & CD pipeline

## Why use *Skaffold*
* Simple to use command line tool
* No cluster side set-up or server side components
* Minimal to zero knowledge of Kubernetes
* Deploy regularly when changing / saving files locally
* Deploy only the pieces of stack that have change
* Image tag management
* Pluggable architecture that supports existing tools
* Flexible workflow support for remote development and  automated CI & CD pipeline
* Backed by Google & OSS community

## Alternatives to *Skaffold*
* [_Telepresence_ from Datawire](https://www.telepresence.io/ "Telepresence's homepage")
* [_Draft_ from Azure](https://draft.sh/ "Draft's homepage")
* [_Ksync_ from Vaporware](https://vapor-ware.github.io/ksync/ "Ksync's homepage")

## Operating Modes
Two execution modes mentioned below are supported. We will cover `dev` mode in this guide.

`skaffold dev`

`skaffold run`

## Skaffold `dev`
`dev` is local development mode. Your application deployed on local Kubernetes cluster will be continually updated.  In this mode, *Skaffold*

* Watches source code and docker image dependencies for changes.
* Runs a build  and deploy when changes are detected
* Streams logs from deployed containers
* Maintains continuous build-deploy loop
* Warns on error

# Getting started with continuous local app development   
## Prerequisites   
1. Local kubernetes cluster as target cluster for *skaffold*. Any Kubernetes cluster will work.
* Minikube
* Docker Edge (Mac / Windows)
* Minishift (not tested)

2. *Docker*
* Connects to local docker daemon
* Uses "docker-for-desktop" context via local docker daemon

2. *Kubectl* (_optional_)
* Automatically configures `current-context` for local cluster environment
* Manually configure `current-context` for your remote target cluster environment

## Installation   
1. Clone this repository to get access to latest *skaffold* build
> `git clone https://github.com/parthigeo/skafdev.git`

2. Run the below install script
> `source skaffold-install.sh`

## Lab-1: First time local build & deploy
1. Verify Installation
> `skaffold version`

2. Change directories to `local-dev` example
> `cd example/local-dev/simple`

3. Verify contents under the directory by `ls -a`
> Dockefile, app.yaml, skaffold.yaml

4. Execute `skaffold dev`

5. Response log from `skaffold dev` execution
> placeholder for

6. Things done by *Skaffold* for you:
* Build an docker image from the local source code
* Tag it with its `sha256`
* Sets that image in the Kubernetes manifests defined in `skaffold.yaml`
* Deploy the Kubernetes manifests using `Kubectl apply -f`

7. Output of the deployed containers
> Placeholder

8. Output from `kubectl`
> Placeholder

## Lab-2: Local dev loop with Kubernetes manifests
1. Make changes to application source code
> Placeholder

2. Save the changes
> Placeholder

3. Automatic response from re-deployed application
> Placeholder

4. Things done by *Skaffold* for you:
* Automatically detect source code change
* Re-build an docker image from the local source code
* Re-tag it with its `sha256`
* Re-set the image in the Kubernetes manifests defined in `skaffold.yaml`
* Re-deploy the Kubernetes manifests using `Kubectl apply -f`

5. Output from `kubectl`
> Placeholder

## Lab-3: Local dev loop without Kubernetes manifests
1. Make changes to application source code
> Placeholder

# References
> Placeholder

# Credits
> Guide Author: Parthiban Srinivasan, Cloud Solution Architect @ Capgemini NA Inc
___
> Tool Author:
> Google Inc  
>*Skaffold* OSS [maintainers](https://github.com/GoogleContainerTools/skaffold/blob/master/MAINTAINERS)
