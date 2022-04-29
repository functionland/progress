# Sample DApps

Date: April 29, 2022

## Fotos

Fotos is a web3 mobile DApp for backing up and sharing personal photos and video created to help people liberate their personal home photos and video from Big Tech.

With the latest release of Fotos, users can:

    * scroll back in time and have photos that they took years ago appear immediately

    * pinch/zoom the gallery to change the number of columns in the gallery

    * tap on a photo to enter browse mode

    * browsing photos with swipe

    * a bottom toolbar with sections to show what will come next

    * batch select and delete photos from their gallery

    * perform thumb scroll to quickly scroll back to a previous moment in time

## Demo Intro

This video will demonstrate how the ___ DApp can connect to a Box app that is installed on a raspberry Pi device.

Browser : After loading the DApp I enter the Box's PeerId to connect to it.

## Demo End

Since the DApp is running on a Box that is always on, I can load the [todo items, photos, documents] from another device later in time.

## Todo

Todos is a sample DApp that demonstrates performing typical CRUD operations using the Graph API in a react web single page application.

[Insert Demo Intro]

I then can add a few items to my todo list, edit and delete them.

[Insert Demo End]

## Photos Sample

The gallery and companion command line photo upload client DApps builds on the Todos app by demonstrating how the File and Graph APIs might be used in conjunction with each other to build a rich multimedia based DApp.

To make the gallery work there needs to be a way to store and retrieve the list of references (aka content identifiers) of each photo.

So when the file is uploaded and a CID is succesfully returned, the client immediately calls the graph API adding the CID to the gallery collection.

Then the gallery reads the list using the Graph API and retrieves each CID using the File API and displays each as a data url passed to each html image tag.

It also demonstrates uploading photos via the browser from a browser based input element.

[Insert Demo Intro]

I can then upload my photos using the html file input tag and the gallery gets updated with my newly backed up fotos.

[Insert Demo End]

Uploading photos can also be done via the cmd line using a companion DApp the vanilla non-react javascript fula client library.

These two DApps also demonstrate how interop between DApps can easily be achieved by deciding on and sharing the same normalized 'gallery' vocabulary.

## Doc syncing

The following project demonstrates how someone might write a document syncing DApp so that people can share notes in real time with each other.

They were created in a dog fooding effort so that the dev team and quickly and permanently share meeting notes while on a call with each other.

There are two companion DApps:

  * fsync - a cmd line interface for syncing files with Box

  * fuludocs - a web interface that fetches the doc based on a meeting code and renders updates in real time

These two DApps also demonstrate how interop between DApps can easily be achieved by deciding on and sharing the same normalized 'gallery' vocabulary.

### Fuludocs

  * subscribing to and receiving events using the Graph API

  * working with different files besides fotos such as plain text markdown

### Fsync

  * a command line interface for sharing updates to files in realtime with anyone.

  * execute the cmd passing in the path to the file you want to share and get a meeting code to share with other participants in the call.

[Insert Demo Intro]

After launching both DApps, I can now edit the file in realtime and have the text appear in the browser as markdown formatted text.

[Insert Demo End]
