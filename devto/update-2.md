---
title: Fula: a new, innovative way to develop decentralized applications
published: true
description: Aaron gives his story on how he came to Functionland and provides an update to the DEV.TO community on what we are building
tags: #p2p #web3 #showdev #blockchain
cover_image: https://dev-to-uploads.s3.amazonaws.com/uploads/articles/hp1mnxd7nuci2cgwqta4.png
---

Greetings fellow DEVs!  First off, a warm thank you to the DEV.TO community for all the support they’ve given Functionland!

As a relatively new member of the dev team, I can tell you that  @ben's [comment on our previous post](https://dev.to/ben/comment/1f4k4) was one of the first things I read when I discovered this project.

A lot has changed since then. Time for an update! Hopefully we can garner *EVEN MORE* support from you now, in the final days of our [crowdfunding campaign](https://www.indiegogo.com/projects/box-secure-subscription-free-cloud-alternative#/).

Before I get to the updates I'd like to share what first resonated with me about the `Fula` protocol; the open source p2p protocol we mentioned in the last [DEV.TO update](https://dev.to/fx/google-photos-open-source-alternative-with-react-native-80c).

Before joining Functionland I wanted to learn more about web3.  So I joined an [eth global](https://ethglobal.com/) hackathon. There I worked on a token gated [livepeer](https://livepeer.org/) video streaming site that creators could use to host an online ticketed concert.

It was a really great learning and networking experience and I would encourage any web2 dev wanting to get into web3 to check it out.

However, I was a little disappointed when I learned that the status quo for access control in web3 still tended to be centralised, relying on a single node to verify that the NFT holder matches their wallet address.

I felt let down. The appeal of writing networked permissionless software vanished. I’d discovered I had to be a [bridge keeper](https://www.youtube.com/watch?v=pWS8Mg-JWSg) to users of my “DApp”.

This meant I'd have to set up my own cloud account and monitor usage and make sure that if usage spikes I have a way to pay the bills. 

It also meant that I couldn’t really claim permissionless anymore because at any moment I could pull the plug.

I went down a bit of a rabbit hole looking for better decentralized solutions that would enable me - a third party DApp developer - to get out of the way! After all, isn’t that the big promise of web3? Always on permissionless computing?

I looked into a lot of decentralized computing projects and came to two conclusions:

1. When it comes to using a surrogate for my own computations, I don't think it’s possible to completely remove 'trust'.

2. There is no such thing as 'free energy.' If someone is offering 'free cloud computing' there must be a catch.

Then I discovered Functionland.  What resonated with me was the fact that the team was building a solution (Box) for people to replace cloud computing with something new, not just another native cloud solution. 

The Functionland team was [proposing](https://fx.land/FulaWP.pdf) a completely new paradigm - hybrid cloud/on prem. computing for *consumers* with customized plug and play hardware so that they don't have to compromise on convenience.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/kj6t8rk6wgs1earcvgcj.jpeg)

Box as unveiled on [Indiegogo](https://www.indiegogo.com/projects/box-first-free-forever-cloud-storage-alternative/x/20718750#/)

This solution continues to offer the properties of cloud that consumers take for granted, like availability and reliability. It also offers consumers new elements that cloud alone can’t provide:

  * truly permissionless DApps. The developer doesn’t have to hold any API keys

  * additional security and privacy. The user can choose to run everything on their own hardware

  * complete data ownership. Everything I upload also sits on my own home server

Let's take a moment (and a deep breath) and appreciate the magnitude of offering a hybrid solution for consumers.  Hasn't enterprise spent the last few decades migrating all of their data from their own servers to a cloud data centre to cut down on the cost of staffing their own sys admins?

Yes but any high paid sys admin out there can tell you many organisations have not and will not ever fully migrate all their data to the cloud.  Why? Because there is certain data (aka systems of record) that is so important to the business that it isn’t worthwhile to trust someone else with it.

So why do consumers need what only the largest enterprises have?  To answer that, let’s do a little thought experiment.  Let’s say we came up with essentially the same solution from a system design perspective as the personal cloud storage providers, except we use a decentralized storage network.

That’s great because we are now enabling anyone (with the technical know how) to be a storage provider. But what happens when you stop paying the bills and your device turns off?  You would have to call each individual storage provider's customer support and ask them to please hold on to your data in good faith even though you are behind on a bill.  That doesn’t sound right to me.  Especially since we are talking about my personal home photos and video - a big part of my legacy that I would like to some day pass down to my children.

So, after rolling my eyes and saying to myself 'not another web3 protocol', I began to understand the need for something new that not only takes advantage of the [cutting edge in peer to peer networking](https://libp2p.io/) but also acknowledges the fact that the client-server architecture is also not going away (which is incredibly important in a world full of low-powered, embedded devices).

![Fula Network](https://docs.fx.land/assets/images/fula-network-arch-42cc4c9855aa4df83f37df5abeff4d8d.png)

Now… Let’s get back to that update!

The dev team has been hard at work developing a usable [Fotos DApp](https://github.com/functionland/fotos), `Fula` (the web3 protocol I've been ranting about) and Box (it's reference implementation).

We've also put a lot of time and consideration into a new consolidated [docs](docs.fx.land) site where interested externals can come to:

  * learn how to develop their own rich web3 DApps on top of Fula

  * read our latest whitepaper

  * look at our latest designs for future work in the [RFCs section](https://docs.fx.land/RFCs/rfc-process)

The [Fula](https://github.com/functionland/fula) protocol was designed to power the Fotos DApp as a Web3 decentralised application using open interoperable specifications that include IPFS and libp2p.

However, it was not designed only for the purpose of backing up and sharing photos from a react native mobile client.

We also provide Todo, Web Gallery and Doc syncing sample DApps to illustrate how developing DApps for web3 can be even easier than developing apps for web2!

The [TODOs sample DApp](https://github.com/functionland/fula/tree/main/examples/react-todo-app) illustrates making CRUD operations over graphql and the [gallery sample DApp](https://github.com/functionland/fula/tree/main/examples/react-gallery) illustrates how to use the FILE and GRAPH APIs in conjunction with each other.

Finally, the [doc syncing companion DApps](https://github.com/functionland/fula/tree/main/examples/doc-sync) illustrate the following:

  * how one can subscribe to and receive events in realtime using the Graph API

  * working with different file formats besides photos such as plain text markdown

  * how updates to files can be shared in real-time by intercepting file system change events provided by the underlying OS and acting on those changes by invoking the File API

  * how a developer could add a simple deploy script that calls `IPFS add -r` on the app's build output as a package.json deploy script (no cloud hosting account needed)

To learn how to get the samples running and how to work with the FULA client libraries, developers can head over to the [getting started](https://docs.fx.land/getting-started/) section on [docs.fx.land](https://docs.fx.land/).

Recently, besides refining the Graph and File APIs, the team has made some first steps towards improving DApp availability and reliability with local pools by refactoring the Box architecture to include [IPFS Cluster](https://cluster.ipfs.io/).

We have also included support for [client side encryption](https://github.com/functionland/fula/tree/main/libraries/fula-sec) through the use of decentralised identifiers (DIDs).

That’s it for the update!  We would like to acknowledge the technical mountain we are trying to overcome in a short amount of time.  There are incredibly smart people that have been working on the problem we are trying to solve for over a decade.

We believe we can get there in a relatively short amount of time because of the following:

  * laser focus on delivering what matters with the flagship DApps when we ship

  * exceptional funding thanks to support from the open source development community (that is YOU!)

  * most importantly, standing on the shoulders of giants (from hardware to software)

Thanks and we really look forward to hearing feedback from the wonderful DEV.TO community about what we are building!

As always, please feel free to bash our idea!  We are still learning and we consider you all as frenz.  Frenz tell frenz when they have something stuck in their teeth. :D


