# Testnet delivery

Attendees: Jamshid, Farhoud, Mehdi, Mahdi, Masih, Keyvan, Aaron

Date: June 13, 2022


## Purpose of Testnet

1.  Find errors and edge cases (especially long lived) before we launch

2.  Gather feedback so we can ensure we are delivering on what is important when we ship

3.  Build community / rapport with 'fx.land fan peeps'

## Directive

* we should not implement anything just for testnet

## Agenda

* what is currently working (demos)

  * OrbitDB replication

    * missing - not reliable

  * fula-sec

    * using wallet I generate DID

    * creation of DID with input of mnemonic (on web)

  * Fotos

    * I encrypt my file with DID before uploading it

    * using wallet connect to provide mnemonic


* what the UX should be
  * give option for ec2 or pi or just pi?
  * if Pi we need to figure out key sharing for cluster (send an email suffices?)

* what needs to be done for sufficient UX

  * encryption on they fly when streaming file in go mobile

  * replace input of mnemonic with wallet connect


## Shoot For

* I provision a Box environment on my own development machine

* I join a pool

* I use Fotos to back up my photos from my device

* I connect with a wallet and only my wallet account is able to access my files

## Next (short term)

* write a doc on sharing a file with someone else

* Jamshid

* Mehdi

  * reliable replication

  * namespaces
    * apps
    * users
    * clients

  * encryption of graphql DB
    * easiest path forward is to enable querying on client side

  * alternatives to orbit DB
    * using IPLD + selectors
    * replication?

## Next (long term)

  * access revoke

## What are we sending?

  * link to documentation with instructions on how to run through use cases


  * Box via 'on prem'

    * there is a third solution - we deliver 'on prem' in a pool with Box

    * cons for running Box environment on our own infra

      * puts us on the hook if something goes wrong

      * increases our provisioning workload

    * pros for running Box environment on our own infra

      * enables us to ssh in and view logs / troubleshoot when things go wrong

        * we should have that kind of diagnostics / troubleshooting available for 'on prem'
