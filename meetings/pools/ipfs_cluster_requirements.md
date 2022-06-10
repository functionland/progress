# IPFS Cluster Requirements

Attendees: Ehsan, Masih, Farhoud, Aaron

Date: June 6, 2022

## Key Takeway

  * we should start writing some failing acceptance tests that will

    * communicate hard requirements

    * help us keep track of work


### Framework

  * does not really matter as long as it exits with a code of 0 when passing and 1 when failing

### Test cases

  * I should be able to access any file at any time from the Box I uploaded the file to

  * only I should be able to remove my own files from the shared pinset

    * a malicious user in the network should not be able to remove files that I own

    * if two people upload the same file and one of them removes it then the desired replication factor should still reflect

### Questions

    * if I upload a file with replication factor of 3 then someone else uploads the same file with rp-2 what will the replication factor be?

    * what is the state of sharding?

## Discussion

  * full copy should go stay on my Box

  * each pool should be able to set their own replication factor

  * why should replication factor be fixed in a pool?
    * providers will probably go where demand is
    * I have certain data that I really don't want to lose and other that I don't really care about

  * ideally I could specify my replication factor based on a probability of loss
    * fitness function
      * can we hit 90% probability and if not what action should we take?

  * do we want to have users join / leave pools automatically?

    * for protocol design it does not matter we just need to provide an API for peers to join / leave pools


  * both edge cases should be handled


---

## Hard Requirements

  * I should always have a copy of all of my own files on my own Box

  * IPFS-Cluster should respect my desired replication factor

  * replication factor should be per file
    * UX can have sane defaults / based on folders or file types


  * failure scenario
    * if someone wants a replication factor of three and there are only two nodes

      * we must report on it

      * have peers come online that cover minimum replication factor

    * if I have a Box with 1 GB of storage I can't upload a file that is > 1GB of storage


## Hard Limitations


----


## Assumption

A pool is a grouping of peers that anyone can join to collaboratively provide redundancy of storage.

There are three participants:
  * miner
  * consumer
  * validator

### Provider

### Consumer

### Validator


## Requirements
  * only the "owner" of a pin should be allowed to request that their pin get removed

## Questions
  * should Box customers be joining pools or should that happen automatically?
  * how is the replication factor determined?
  * who decides which miners store what?
  * what is data model for pinset?
  * how do pins get added / removed from local pinset?

