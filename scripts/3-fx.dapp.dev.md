# Video Script Update No. 3

Good morning, afternoon and evening everyone.

Today is April 22nd 2022 and this is a progress update from the Functionland dev team.

In the past month we have continued work on Fotos (a web3 mobile app for backing up and sharing personal photos and video), Box (our reference implementation of the Fula protocol)
as well as Fula itself (a protocol for DApp developers that provides an alternative to working with traditional cloud platforms).

## Fotos

In the latest release of Fotos, users are now able to:

  * batch select and delete photos from their gallery

  * perform thumb scroll to quickly scroll back to a previous moment in time


## Fula

On the Fula front, we have completed developer previews for user stories around:

  * encryption

  * availability

  * file syncing

### Encryption

For encryption, we have included the ability for DApps to encrypt owner's files before uploading them to their Box
so that if a third party somehow accesses the file they will not be able to view it's contents.

### Availability + File Syncing

To provide availability and reliability for DApps that work with a Box, the Fula dev team made some major changes to the Box system architecture.

We decoupled IPFS as an embedded library of the Box application to a standalone process that is invoked with the IPFS HTTP API.

This enabled the inclusion of the Go implementation of IPFS Cluster that also has IPFS as a dependency.

We included IPFS-Cluster in the Box environment since it provides:

  * private network communications of swarm participants using a shared private key

  * conflict resolution with no centralized point of failure

  * notifying peers of updates to the pinset

  * efficient transmission and management of data based on a desired replication factor

  * providing peer pinning status for a future administrative monitoring dashboard

  * works synergistically with IPFS which the team had already adopted for other purposes such as scalable content distribution and deduplication

To demonstrate the availability and file syncing stories we will make use of a pair of sample DApps.

Fsync is a command line interface for sharing updates to files in realtime and fuludocs is a companion client for receiving the updates and rendering them as markdown in the browser.

The Fsync sample Dapp demonstrates:

    * how a desktop file syncing client might work in the Fula network
    * how the File and Graph APIs can be used in conjunction with each other to enable several files to be synced at the same time

The fuludocs sample DApp demonstrates:

    * how to subscribe to Graph API events

    * how to use the File API with other file types besides photos (eg/ plain text)

In this scenario, [insert replication story](../stories/replication.md)

In the future, the fsync and fuludocs DApps could accept a list of Box `Peer IDs`
add auto-connect to another available Box in the swarm if a connection is lost.
However, for demo purposes we are doing this manually.

Also, since we are using libp2p we could also make
the browser clients talk directly to the fsync application
thus cutting out a hop in the roundtrip of the connection and reducing latency.

However, once again, we had each client connect to each Box in the swarm to
demonstrate that the connection to one of the Boxes is in fact lost and
how the recovery process could work.

Regardless, for certain use cases, this network topology might still be optimal.

For example, lets say a Box owner wanted to watch the football game on three different devices.
One in their family room, one in their kitchen, and one on their phone.

They could minimize bandwidth by streaming the game directly to the Box
and then multicasting the stream to each device that is sitting behind their home network.

That is the beauty of libp2p, since each device in the network is considered a peer,
it provides the developer with a straightforward way to cover different topologies depending on the use case.

## DApp distribution

The fuludocs sample also demonstrate a simple way for developers to distribute their DApps by hosting them on IPFS.

A developer could add a simple deploy script that calls IPFS add -r on the app's build output.

They could then take the CID for the root of the dist folder as is and use it to serve the app in an IPFS capable browser
or put it behind an http gateway and/or naming service.

## Fula Wrapup

Hopefully you can see how the encryption and replication stories are complimentary to each other.

A Box owner might choose to backup their data on a swarm of Boxes that they own.
Or they might also choose to backup their data with a small group of friends and
their friends are still unable to view the contents of their data unless they get access to the owner's private key
or the owner gives them access to it by generating a GWE for their identity.

It should be mentioned as a caveat, however, that content must be still encrypted by the DApp.

For example, fsync is not currently making use of the Fula encryption protocol,
so anyone with the link and Box `Peer ID` will be able to view the contents of the file as long
the Box is making that content available.

In the future, fsync and fuludocs will be updated to make use of the owner's private key and encrypt the document's contents as privacy should be on by default.

Besides encryption, we will also showcase an additional security layer based on an ACL in a future release that will give
Box owners additional protection over how outsiders can access their content.

## Wrapup

Thats it for the April 22nd update.  As always, the functionland dev team looks forward to updating you again in the future.
