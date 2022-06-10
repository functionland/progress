# Update Before Testnet

Attendees: Jamshi, Madhi, Ehsan, Kevan

Date: June 10, 2022

## Discussion

* we already implemented DID with encryption over web
  * scenario was only I can upload the file and only I can see it

* two scenarios
  *  I am the only person able to access my files from my device (Fotos)

* sharing
  * better security for exchange
  * storing encrypted object in Orbit DB

* identity can be store on their own Box and across the world for safety purposes

* file encryption
  * future work could be chunking to avoid high memory usage

* access revoke is out of scope for now

* BigInt issues (solved!)

## Outstanding questions

  * how do we share JWE?
    * use deeplink?

  * wallet DID generation process is slow

  * we should ont be storing mnemonic for customer in client

  * encryption layer two options
    * read file from disk encrypt entire contents and send to Box

    * chunk / stream

  * Go implementation is not playing well with fula-sec encryption (currently in JS)

    * implement encryption in Go?

    * implement file / graph in JS on react-native?

    * convert File into a streaming chunk API?

    * utilize libp2p via WASM?


## Requirements

1.  I create my identity through wallet connect

2.  I encrypt my files using the identity so that only my identity is able to see it

3.  I am able to share my files with another identity (optional but extremely nice to have)

## Directives
  * we want to provide as much as we have currently implemented in a nice package for testnet users to play around with

## Questions
  * offload encryption to a wallet using eths.js lib?
