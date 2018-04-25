# Continuous LOCAL development using *Skaffold*
This guide walks you thru continuous local development using *Skaffold* container tool. This OSS container native tool from Google facilitate better developer experience for Kubernetes application.

## What is *Skaffold*
It is a command line tool that help iterate an application locally and then deploys it on local / remote cluster. This tool detect changes in your application source code as well as the dependencies of your docker images. And automatically triggers build, push and deploy to local / remote Kubernetes cluster.

## Focus
This guide focuses on local development context rather than remote context such as automated CI & CD pipeline. Advanced workflow will be covered separately.

> Consider this as *Skaffold* getting started guide for local application development

## Why use *Skaffold*
* Simple to use command line tool.
* No cluster / server side component.
* Deploy regularly when saving files locally
* Deploy only the pieces of your stack that have change
* Image tag management support
* Pluggable architecture that supports existing tools
* Flexible workflow support for remote development and  automated CI & CD pipeline

## Operating Modes
Two modes of operation are supported i.e. DEV & RUN

'skaffold dev'
'skaffold run'

## Skaffold "*dev*""
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
>Author: Parthiban Srinivasan,
>Solution Architect @ Capgemini
___
>Google Inc
>Skaffold OSS authors
