# monk
Quite Possibly Ambitious

## What is monk?

Monk is a (brand spanking new) docker orchestration/cluster provisioner/code deploying system, written entirely in javascript / meteor.

## Why?

Because everything else sucks (sorry if that offends you).

## Monk Requirements

The goals of monk:

- Manageable from any machine
- Deployable from any machine
- Be distributed and self healing
- Simple to bootstrap, and fast
- As simple as pushing my code to deploy
- Multiple environments (such as staging/qa/production)
- rolling releases
- ANY code, any app
- Scalable, self healing, distributed data stores
 - Galera for MySQL
 - Hot standby/streaming replicaiton PostgreSQL
 - Distributed fs available to the application
 - etc...
- *only* HTTP/DNS interfaces to components
- Beautiful

## Planned Component Design

- monk-roshi: A virtual machine that runs via vagrant, for the purpose of deploying and managing a cluster.
- monk-shami: Bootstraps a server, running in a datacenter cluster. Updates server on demand.
- monk-jushoku: Schudules app/server deployments, handles traffic routing as required.
- monk: front-end for monk-roshi, monk-shami, monk-jushoku.

## Provisioning a cluster

1. clone monk-roshi
2. vagrant up
3. visit http://localhost:9999
4. follow the instructions in your browser

## Deploy an application
1. `monk create my-app` - create's an app called my-app
2. cd my-app
3. edit Dockerfile
4. edit example config file
5. `monk build v1.0` - builds the docker file, tags with v1.0
6. `monk register` - registers the application to monk's docker registry and sets configuration params
7. visit http://localhost:9999
8. deploy the application to the cluster(s)
9. set scaling, constraints, rolling deployments, etc.
10. your app is running

## How to contribute

Clone this repository, write some code, create a pull-request.
