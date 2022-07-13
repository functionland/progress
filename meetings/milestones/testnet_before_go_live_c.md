# Testnet before Go Live (C)

Attendees: Farhoud, Mehdi, Keyvan, Ehsan, Arman, Aaron (Comms) , Aaron (Dev)

Date: Wed. July 13, 2022

## Problems

1.  Aaron can't test with web gallery because images are not loading (probably due to public signalling server throttling connection)

2.  Farhoud and Aaron can't open deep links on Pixel (Android version 12)

3.  Aaron only has a single android device so only supporting Android means he could not test himself.

## Potential Solutions

1.  Get websockets working in browser

2.  Set up our own signalling server

3.  Make it easier to test with mobile only

	a ) fix deep links

	b ) support iOS

	c ) figure out how to get access to a second android device

4.  Accept limitations and Aaron / Farhoud will not be testing / Mehdi, Mahdi or Jamshid will have to finish the testnet writeup.

## Question

What is the point? Is it just to send out a tweet that we are releasing a testnet or is it to get actual people testing our software and get them excited about it?  If its the latter then the fact that Aaron can't get things working means the chances that volunteers running into a roadblock and not getting onboarded is really high.

## Directive

1.  We send out the testnet email with what we have working today (no web gallery, iOS and deep linking will not work on certain  android devices).

2.  We leave a section at the begninng mentioning a list of requirements (so that people don't have to go through the entire thing only to find out they do not meet the requirements

3.  The instructions will ask people to -

  a ) Fire up a cluster using docker compose

  b ) Upload an image to a Blox using Fotos

  c ) Verify the image was backed up to the Blox

  d ) Share an image with someone else

4.  Track success of each 'tester' along with any issues they encountered (so that we can prioritize for next release).
