# Database Requirements

Attendees: Mehdi, Ehsan, Aaron

Date: June 9, 2022

## Discussion


  * should we depart from using OrbitDB?
    * IPFS handles replication
    * IPLD handles manipulation of data
    * OrbitDB is batteries included 


  * difference between web2 and web3

  * how about offering encrypted queries / how do I keep my data secure while using IPLD?
    * homomorphic encryption is too complex for our use case?

    * simple solution (partial encryption)
      * client writes a selector
      * we perform query / cache results encrypted
      * problem is we are leaking the key/query

  * could we just not provide queries and instead do indexing on the client?

    * middle ground - timestamped based indexing?

      * this depends on the use case
        * could be timestamp for photos and title for todos

      * how do we grow the index if we are pre-rendering?

        * growing chain of single DAGs

        * create a new node with filed of type 'link'

    * what is the business requirement?

      * we want to givea graphql interface to developers
        * they are querying on JSON


  * how do we hit timeline for hitting 'production'?
    * we need to reduce scope

    * timeline
      * by November we release Box

      * we have developer docs with sample apps enabling devs to write their own apps

      * apps we are releasing
        * photos
        * dropbox like app
        * password manager (not shipped in Nov.)

      * blockchain layer must go live
        * ensure that if your Box is destroyed you can restore a copy of your data from the pool

      * pools
        * two types of replication
          * I own three Boxes and a full copy of all my files exists on each Box

          * I join a pool with others and it is based on replication factor

      * testnet in a month
        * no physical Box (people will install on their own hardware)

        * 1 pool


    * we need ability to spin up a 'Box' in any region
      * safe to break area for ourselves that is constantly running

    * OTA (ability to provide updates in background)

    * should we go

# Areas

    * database

    * CI/CD work on automated deployments

      * constant running integration tests

      * https://status.solana.com/

    * integration with blockchain team
      * necessary APIs
      * review of their work



