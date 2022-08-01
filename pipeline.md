# FX.Pipeline

## Fula

1. Make Box easier to run long lived

  * connect Fotos to Box rpi

  * mount external hard drive to rpi

  * memory leak in Box?
    * health monitoring (to help determine cause when something goes wrong)

  * investigate runaway cluster logs

2. Access control

  * only Box owners are allowed to upload files to their Box

3. Pools

  * blockchain integration

    * near term

      * restart proof engine issue?

      * is IPFS rewarding based on file size?

      * should not have to add to local IPFS

      * my balance should increase over time as I continue to store a file as a provider

    * long term

      * when I upload a file it should get pinned on  other nodes with a certain replication factor

        * the other nodes should get rewarded for storing my file

  * other issues

    * pin ownership

    * starting from nothing


4. Security (ideally audit of each section can be done both internally and externally)

  * blockchain delivery
    * what are the threat models + strategies for avoiding them?

  * API

  * components
    * IPFS /  IPFS  Cluster / Box
      * is it connected to a public network?
        * if yes then should it be?
          * if yes then is it rate limited / private?


  * hardware
    * how are we verifying it is not tamper proof?


## Fotos

1. Better client support

	* desktop/web

	* iOS

2. Better UX

  * sharing should not require so much back and forth to share a photo

  * better way of connecting to a Box (setup + sharing)

  * DApp wallets auth vs. web2 login

    * custodian

    * transferance

    * barrier to entry

    * in web2 bank accounts and web2 accounts are separate

3. Features

  * blockchain integration

  * sharing

    * connect to Box over WAN

    * anyone with a link can view the file/folder

    * access revoke

  * batch upload all my photos

  * albums

  * search

  * stories


## Measuring

## Goals

  * make the project look more attractive to investors

  * QA

    * how does software perform under certain loads

    * what are expected 'loads' for an average user

    * how does the network perform?

      * loading time



## Metrics
  * Number of pools
  * Number of nodes / pool
  * Number of photos backed up
  * Total used storage
  * Average replication factor
  * Time to reach ‘desired’ replication factor
  * Loading time (average / min / max)
  * Time to get shared (from share initiated to received)

  * Along with a few health metrics (perhaps we could use something off the shelf like Nagios or AWS cloudwatch) -

    * Disk I/O throughput

    * CPU uptime

    * memory
