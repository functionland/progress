# Testnet Demos

Attendees: Mahdi, Farhoud, Jamshid, Keyvan, Emad, Mehdi, Aaron

Date: June 20, 2022

## Agenda

### Demos

  * I use a standalone app to encrypt/decrypt files 

  * initial testnet email writeup

### What needs to be done

#### Before wednesday

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

#### After wednesday

* how will testnet users load the 'web gallery'?

  * options are
    * fix the `npm run build` JS error

      * try 'npm run build' in fula-sec

    * provide instructions on running locally

* Fotos should post to a 'gallery' collection similar to the gallery web app

#### Community

* support contact / submitting bug reports

* decide on launching community at same time

* dev intake instructions (email?)


#### Future

  * sharing (Jamshid)
    * update README on grabbing mnemonic
    * access revocation refactoring
    * design doc: mapping of peer id to DID

  * multi-tenancy / name space collisions
