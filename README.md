# Continuous local Kubernetes app development using *Skaffold*
This guide walks you thru continuous local application development using *Skaffold* container tool. This guide aims to demonstrate frictionless developer experience for application running on local Kubernetes cluster.

## What is *Skaffold*
It is a command line tool from Google's open source container tools that helps iterate an application. It  deploys application on either local or remote Kubernetes cluster. This tool basically detect changes in your application source code as well as the dependencies of your docker images. And automatically triggers build, push & deploy to local / remote Kubernetes cluster per configuration.

## Focus
This guide focuses on local development context rather than remote context such as automated CI & CD pipeline. Advanced workflow will be covered separately.

> Consider this as *Skaffold* getting started guide for local application development

## Why use *Skaffold*
* Simple to use command line tool.
* No complex cluster / server side component.
* Deploy regularly when changing & saving files locally
* Deploy only the pieces of your stack that have change
* Image tag management support
* Pluggable architecture that supports existing tools
* Flexible workflow support for remote development and  automated CI & CD pipeline

## Operating Modes
Two modes of operation are supported i.e. DEV & RUN command execution modes

`skaffold dev`

`skaffold run`

## Skaffold `dev`
In this local development mode, your application deployed on local kubernetes cluster will be continually updated.  In this mode, *Skaffold*

* Watches source code and docker image dependencies for changes.
* Runs a build  and deploy when changes are detected
* Streams logs from deployed containers
* Maintains continuous build-deploy loop
* Warns on error

# Getting started with local application development   
<Placeholder>

## Prerequisites   
Local kubernetes cluster. Any Kubernetes cluster will work.
* Minikube
* Docker Edge (Mac / Windows)
* GKE
Kubectl. Configure `current-context` with your target cluster environment


## Installation   
1. Clone this repository to get access to latest *skaffold* build
`git clone https://github.com/parthigeo/skafdev.git`

2. Run the below install script
`source skaffold-install.sh`

## Continuous development - first time build & deploy
1. Verify Installation
`skaffold version`

2. Change directories to `local-dev` example
`cd example/local-dev/simple`

3. Verify contents under the directory by `ls -a`
> Dockefile, app.yaml, skaffold.yaml

4. Run 'skaffold dev'

5. Logs from `Skaffold dev`
> placeholder for

6. Things done by *Skaffold* for you:
* Build an docker image from the local source code
* Tag it with its `sha256`
* Sets that image in the Kubernetes manifests defined in `skaffold.yaml`
* Deploy the Kubernetes manifests using `Kubectl apply -f`

7. Output of the deployed containers
> Placeholder

## Continuous development - change loop
1. Update application code
> Placeholder

2. Save the file
> Placeholder

3. Output from re-deployed application
> Placeholder

4. Things done by *Skaffold* for you:
* Automatically detect source code change
* Re-build an docker image from the local source code
* Re-tag it with its `sha256`
* Re-set the image in the Kubernetes manifests defined in `skaffold.yaml`
* Re-deploy the Kubernetes manifests using `Kubectl apply -f`

# Credits
>Author: Parthiban Srinivasan, Solution Architect @ Capgemini
___
>Google Inc

>Skaffold OSS authors
