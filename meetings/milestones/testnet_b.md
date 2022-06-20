# Testnet Demos

Attendees: Mahdi, Farhoud, Jamshid, Keyvan, Emad, Mehdi, Aaron

Date: June 20, 2022

## Agenda

1.  What is currently working (demos)

  a ) Mahdi

    * I connect Fotos to a Box.

    * I use 'wallet connect' to generate a DID which I use to encrypt a file before uploading it.

  b ) Mehdi

    * preventing collection name collisions

      * multiple users upload photos to a Box and they can only see the list of photos that they uploaded

    * documentation on sharing

      * what we have currently working

      * how a developer might extend one of the samples to enable users to share a file with another

      * if it simplifies things we can just share the private key over instant messenger for now


  c ) Farhoud

    * Pin ownership: only I am able to delete my pins from a pool.

  d ) Aaron

    * Testnet setup writeup

    * https://github.com/functionland/fula/issues/217

2.  What the UX should be.

3.  What needs to be done.

## Tasks

* client-side encryption/decryption in Fotos

* support contact / submitting bug reports

* decide on launching community at same time

* instructions for connecting Fotos to Box
  * output Box multiaddrs so that they can be copy/pasted into Fotos or implement peer routing for Fotos to find Box by it's Peer ID?

* dev intake instructions (email?)

* https://github.com/functionland/fula/issues/217
  * ipfs / ipfs-cluster change latest to specific release
  * box use latest image
