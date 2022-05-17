# FX.DApp.Dev Team Update No. 3

Date: Apr. 21, 2022

## Video

[Functionland Dev Tam Update April 2022](https://www.youtube.com/watch?v=sAKym-u07e0&t=32s)

## Summary

In the past month, the fx.dapp.dev team has continued work on Docs, Fula, and Foto.

## Fula

### Encryption

  * included the ability for DApps to encrypt owner's files before uploading it to their Box
    so that if a third party somehow accesses the file on their Box
    they will not be able to view the contents.


### Availability

  * ability for Box owners to replicate their data across several Boxes

    * the main goal of this setup is to improve both availability and reliability

      * if a Box loses internet connectivity then an owner's DApps should still work seamlesly with another Box

      * if a Box is damaged and becomes unusable then an owner should be able to recover all of their data from a source of redundancy

    * decoupled IPFS as an embedded library of the Box application to a standalone process invoking the IPFS HTTP API from the Box app

    * included IPFS-Cluster in the Box environment for the following reasons:

      * private network setup from a shared private key

      * conflict resolution with no centralized point of failure

      * notifying peers of updates to the pinset

      * efficient transmission and management of data based on a desired replication factor

      * providing peer pinning status for a future administrative monitoring dashboard

      * works synergistically with IPFS which the team has adopted for other purposes such as scalable content distribution and deduplication


    * also replicated the DB that is currently powering the graph API

      * since we are currently using Orbit DB the work mainly involved making some configuration changes

        * telling each Orbit DB about it's Peers

        * passing in the same private key we are using to secure IPFS and IPFS Cluster

    * supporting docker-compose scripts for creating a test environment with two Boxes


### File Syncing

  * new pair of companion sample DApps demonstrating:

    * how the File API can be used for other file types besides photos (eg/ plain text)

    * how the File API and Graph API can be used in conjunction with each other to enable several files to be synced at the same time

    * how to subscribe to Graph API events

    * contains two DApps that work in conjunction with one another
      * cmd line interface that accepts a path to a plaintext markdown file and invokes both the Graph and File APIs when there are updates

      * a browser interface for participants in a meeting to recieve updates to the file without having to refresh the browser and renders the markdown into
        a more stylized / human readable form

## Fotos

In the latest release of Fotos, users are now able to:

  * batch select and delete photos from their gallery

  * perform thumb scroll to quickly scroll back to a previous moment in time


