# MVP Use Cases

# Takeways
  * we need to have primitives for both global + local pools
    * ideally there is as much overlap between the two as possible


Black boxes -
  * setup box
  * search pools
  * connect to pool


# Joining a pool

I have already setup their box.

To join a pool, I see a list of pools nearby by name.
The list of pools are ranked by their
I connect to the pool by clicking a 'connect' button.

Why local pools?

  * latency
    * a file is chunked across several nodes and to reassemble it takes a long time

    * important for both retrieval and backups

    * backups
      * minimize roundtrips across the globe
        * I could have three Boxes on my own premise and it should not have to go through the ISP

      * minimize chatiness

# Private pools vs local pools

  * replication factor should be same as number of peers?

  * free non blockchain connected option

  * for 20 people in a small community or people that own  multiple Boxes


Why private pools?

  * provide functionality for Boxes without internet
    * backups

  * privacy

# Global pools vs local pools
  * where do I store identity + ACL?
    * if I store on a local pool only then it potentially goes away
      * if I leave the pool
      * if local pool goes away

    * there is other metadata associated with the identity besides the address and we need to store it somewhere permanently

# Roles

  * pool administrator

    * create pool

# Pool properties

  * speed of ping

  * what layer 2 it is on

  * replication factor

# Metrics

  * ideal size of pool (# of peers) based on computational resources & bandwidth in it
    * roundtrip latency

  * proof of bandwidth

# Non functional requirements

  * private pools should work without a public internet connection

  * disaster recovery (sudden drop a bunch of Boxes in an an area hit with a natural disaster)

# Discussion points

  * we should not expose the complexities of pool administration to less technical

  * pool admin is web2 pattern - not permissionless
    * everything should be automatic/based on consensus
      * anyone can create pool and name is unique (similar to domain registration)
      * properties (eg/ replication factor) are decided on creation

    * if someone does not like a property they can create their own pool

    * how to prevent bad actors?
      * examples - they keep dropping in and out of pool

      * answer - pool standards

    * incentivization / reputation / score

      * applies to actors and pools
      * metadata based on behavior and calculating a score based on metadata
      * reputation protocol
        * anyone can define their own algo for calculating reputation

      * whats in it for the validator?

      * meaningful score calculation gets rewarded

      * if it is measurable then it can be part of reputation score
        * eg/ response time to ping

      * similar to pagerank in google

      * score of each  pool is different for each member in the public fula network

        * so it has to be calculated so I can decide what is right for me

      * incentivation is left up to layer 2

      * bad actors are booted based on autonomous protocol
        * proof of stake encourages hoarding

      * zero config networks
        * target + actual scores
        * provide actions based on scores
          * we can operate on actual metrics

    * tokenomics

      * this is pluggable - we only need to create primitives

      * how is value of $FULA token decided

      * people get rewarded for the time they were in the network

      * strawman

      * genesis
        * worthless until are people join the network

      * we need to generate rewards so that OS contributors get paid

        * transactions

        * mining rewards

      * byte by byte counting
        * if you  provide 1 Tb and I provide 2 Tb then I get rewards

# Logistics

## Formidable

  * file manager (aka dropbox)

  * box admin


# Ehsan follow-up

Let's just use two names for the pools:

1- data pool: which is the pool that keeps data. Parameters are swarm key and replication factor(high level)

2- identity pool: which keeps identities and have swarm key and replication factor as parameters

No need to confuse ourselves with local, private, global naming

With a swarm key that only I have, creates a pool between my own boxes. If i have 2 boxes, i set replication factor to 2, if I have 3, i change it to 3

With a swarm key that is shared between my neighbors, we can create a local pool

And with a swarm key that is shared between all boxes, we create a global

So there is no need for that previous naming.

There just "pools"
