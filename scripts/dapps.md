# Sample DApps

Date: April 29, 2022

## Videos

[Demo Videos](https://drive.google.com/drive/folders/1BoUVyWHBfxMWwSsWsIdDbJpBmFHj1fwl?usp=sharing)

## Intro


## Fotos

The following video is a demonstration of the Fotos DApp, one of the DApps that the Functionland dev team has developed to date.

Fotos is a web3 mobile DApp for backing up and sharing personal photos and video.

It was created to help people liberate their personal home photos and video from Big Tech.

With the latest release of Fotos, users can:

    * scroll back in time and have photos that they took years ago appear immediately

    * pinch/zoom the gallery to change the number of columns

    * tap on a photo to enter browse mode

    * batch select and delete photos from their gallery

    * perform thumb scroll to quickly scroll back to a previous moment in time

The Fotos DApp is fully open source so if a Box customer is not happy with their experience they can always fork the project and customize it to their own content!

If you have any questions please feel free to reach out to us directly on one of our socials.  We are always happy to chat about what we are building.

## Demo Startup

Browser :
First I load the DApp in a web browser.  After loading the DApp I enter the Box's PeerId and connect to it. After connecting...

Terminal :
First I execute the command passing in the Box ID via a cmd line or environment variable.

## Demo End

Hopefully this sample DApp has given you some fun and creative inspiration to build your own web3 DApp on top of the Fula protocol.

We look forward to engaging with you and other DApp developers from around the world so that we can build a rich ecosystem together and realize the original vision of the internet.

If you have any questions please feel free to reach out to us directly on one of our socials.  We are always happy to chat about what we are building.

## Todos Sample

This video will demonstrate how the Todos DApp can connect to a single Box installed on a raspberry Pi.

Todos is a sample DApp that demonstrates performing typical CRUD operations using the Fula Graph API in a react web single page application.

First I load the DApp in a web browser.  After loading the DApp I enter the Box's PeerId and connect to it. After connecting...

I can add a few items to my todo list such as a list of groceries I need to pick up.

I will add some milk, bananas, peanut butter and anchovies since I'm planning to make a shake later.

I can also edit each item in the list.  For example, I misspelled bananas so I will go ahead and fix that so  people don't think I am  a terrible speller.

We would have to call it CRU instead of CRUD if we didn't support delete.  So I will go ahead and remove anchovies from the list because, who likes anchovies?

Since the DApp is persisting its content to a Box that is always on, I can load the todo items from another device later in time.

[Insert Demo End]

## Gallery Sample

This video will demonstrate how a browser based gallery and companion command line client DApp can connect with a Box on a raspberry Pi in order to backup and retrieve a Box customer's personal photos.

The browser and command line DApps build on the Todos DApp by demonstrating how the Fula File and Graph APIs might be used in conjunction with each other to build a
rich multimedia based experience.

These two companion DApps also demonstrate how interop between DApps can easily be achieved by deciding on and sharing the same normalized 'gallery' vocabulary.

To get a list of photos that I previously uploaded, there needs to be a way to store and retrieve the list of references (aka content identifiers) of each photo.

When the file is uploaded using the File API and a CID is succesfully returned, the client immediately calls the graph API adding the CID to a collection we call 'gallery'.

Then the browser client can retrieve the list of CIDs from the gallery collection using the Graph API and then fetch the content for each CID using the File API.

After fetching the content for each file, the browser client can then display each image each as a data url passed to each html image tag.

The browser sample DApp also demonstrates how a standard browser based input element tag can be used with the File API.

First I load the DApp in a web browser.  After loading the DApp I enter the Box's PeerId and connect to it. After connecting,

I can then upload my photos using the html file input tag and the gallery gets updated with my newly added up photo.

Next I connect to the Box from the companion cmd line Dapp by passing in the Box ID as an environment variable.

And the photo I uploaded from the cmd line also appears in my gallery.

The companion cmd line DApp also demonstrates how the vanilla non-react javascript fula client library can be used.

Since the DApps are persisting their content to a Box that is always on, I can load the photos from my gallery, from another device later in time.

[Insert Demo End]


## Doc syncing

This video will demonstrate how a pair of document syncing companion DApps can connect to a Box on a raspberry Pi so that people can share notes with each other in real time.

The document syncing DApps were created in a dog fooding effort so that the dev team can quickly and permanently share meeting notes while on a call with each other.

There are two companion DApps:

Fsync is a cmd line interface for syncing files with a Box and Fuludocs is a web interface that fetches the doc based on a meeting code and renders the markdown in real time.

These two companion DApps also demonstrate how interop between DApps can easily be achieved by deciding on and sharing the same normalized 'meeting' vocabulary.

### Fuludocs

The Fuludocs sample DApp demonstrates how one can subscribe to and receive events in realtime using the Graph API.

It also demonstrates working with different file formats besides photos such as plain text markdown.

### Fsync

The fsync sample DApp demonstrates how updates to files can be shared in realtime by intercepting file system change events provided by the underlying OS and acting on those changes by invoking the File API.

One can execute the cmd passing in the path to the file you want to share and get a meeting code to share with other participants in the call.

First I connect to the Box from the fsync cmd line Dapp by passing in the Box ID as a cmd line parameter.

Next, I pass the url to each participant in the call so that they can load it from their own device on their own home network.

Notice that the url I shared is over the IPFS protocol meaning anyone with an IPFS capable browser can load the DApp that can be hosted on a Box or behind an IPFS gateway.

This is one of the great benefits of developing for the decentralized web.

Anyone can write a simple DApp in minutes and share it with their friends without having to worry
about the complications of setting up a cloud hosting account.

After loading the DApp I enter the Box's PeerId and connect to it.

After connecting both DApps to the Box, I can now edit the file in realtime and have the text immediately  appear in the meeting attendee's browser as markdown formatted text.

[Insert Demo End]
