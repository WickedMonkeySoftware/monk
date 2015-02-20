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

## How to contribute

Clone this repository, write some code, create a pull-request.
