# Testnet Demos

Attendees:

Date: June 22, 2022

## Agenda

1.  What is currently working (demos)

    * I connect Fotos to a Box (Aaron)

    * I use 'wallet connect' to generate a DID which I use to encrypt a file before uploading it (Mahdi)

    * same as Fotos but with web gallery (Mehdi)
      * using wallet connect to provide the private key

      * client side encryption before uploading photos

2.  What the UX should be

3.  What needs to be done

## Tasks

--- dev

---- before wednesday

* get some sleep (everyone)

* integration of client-side encryption/decryption in Fotos (Mahdi, Farhoud)

* web gallery (Mehdi)
  * latest encrypt/decrypt
  * wallet connect integration
  * polish UI (Emad)

* instructions for connecting Fotos to Box (Aaron)
  * logging Box multiaddrs in Box log and include in instructions (Farhoud)

* docker-compose for testnet release (Aaron, Farhoud)
  * ipfs / ipfs-cluster change latest to specific release
  * box use latest image

* testnet writeup  (Aaron)

  * split up email from docs.fx.land

  * sections in docs.fx.land
    * What is testnet?
    * What does it include?
    * How to get started <- the git clone plus readme
    * How to report bugs etc.

---- after wednesday

* how will testnet users load the 'web gallery'?

  * options are
    * fix the npm run build JS error
      * try 'npm run build' in fula-sec

    * provide instruction on running locally

* Fotos should post to a 'gallery' collection similar to the gallery web app


--- community

* support contact / submitting bug reports

* decide on launching community at same time

* dev intake instructions (email?)

## Future

  * sharing (Jamshid)
    * update README on grabbing mnemonic
    * access revocation refactoring
    * design doc: mapping of peer id to DID

  * multi-tenancy / name space collisions
