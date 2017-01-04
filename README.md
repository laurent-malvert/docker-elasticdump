## Description

Provides a `Dockerfile` to build a docker image allowing you to build
your own images to automate Elasticsearch import/export operations
using [elasticdump][1] and [jq][2].

## Why?

3 simple reasons:

 * There are no elasticdump images out there.

 * The community images out there often use an outdated version and
   have not kept up with the latest updates in the fast evolving
   Elastic Stack world.

 * I write my own automation scripts for some elasticsearch-based
   projets, and I need to be able to export/import data from
   ES easily (notably Kibana dashboards). Writing simple scripts
   using elasticdump and jq (to beautify on export and re-compress
   on import automagically) is a nice approach. So I wanted a
   base image including both, in their latest version.

## Pull From DockerHub

    docker pull laurentmalvert/docker-elasticdump

## Build It Yourself

    docker -t elasticdump .

## Usage

### Running `elasticdump`

    docker run          \
           laurentmalvert/docker-elasticdump

## Possible Improvements ?

 * I might publish some of my automation scripts for direct reuse,
   in a separate image.


[1]: https://www.npmjs.com/package/elasticdump
[2]: https://stedolan.github.io/jq/

