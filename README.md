# Continuous LOCAL Kubernetes app development using *Skaffold*
This guide walks you thru continuous local application development using *Skaffold* container tool. This guide aims to demonstrate frictionless developer experience for application running on local Kubernetes cluster.

## What is *Skaffold*
It is a command line tool from Google's open source container toolset that helps iterate an application locally. Then deploys application on either local or remote Kubernetes cluster. This tool bascially detect changes in your application source code as well as the dependencies of your docker images. And automatically triggers build, push and deploy to local / remote Kubernetes cluster.

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

# Getting started with local development   
<Placeholder>

## Prerequisites   
<Placeholder>

## Installation   
<Placeholder>

## Continuous development
<Placeholder>

# Credits
>Author: Parthiban Srinivasan, Solution Architect @ Capgemini
___
>Google Inc

>Skaffold OSS authors
