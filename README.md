# Continuous local Kubernetes app development using *Skaffold*
This guide walks you thru continuous local application development workflow using *Skaffold*, container tool OSS from Google. It  aims to demonstrate frictionless developer experience for application running on local Kubernetes cluster.

## What is *Skaffold*
It is a command line tool from Google's open source container tools that helps iterate an application. It  deploys application on either local or remote Kubernetes cluster. This tool basically detect changes in your application source code as well as the dependencies of your docker images. And automatically triggers build, push & deploy to local / remote Kubernetes cluster per configuration.

## Focus
This guide focuses on local development context rather than remote context such as automated CI & CD pipeline. Advanced workflow will be covered separately.

> Consider this as *Skaffold* getting started guide for local application development

## Why use *Skaffold*
* Simple to use command line tool
* No cluster side set-up or server side components.
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
Two modes of operation are supported i.e. DEV & RUN command execution modes

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
* GKE

2. *Kubectl*
Configure `current-context` with your target cluster environment


## Installation   
1. Clone this repository to get access to latest *skaffold* build
> `git clone https://github.com/parthigeo/skafdev.git`

2. Run the below install script
> `source skaffold-install.sh`

## First time app build & deploy
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

## App change loop
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

# References
> Placeholder

# Credits
>Author: Parthiban Srinivasan, Cloud Solution Architect @ Capgemini NA Inc
___
>Google Inc

>*Skaffold* OSS authors
