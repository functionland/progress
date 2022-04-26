# Replication

## Availability + File Syncing

I have some meeting notes I would like to share with two of my colleagues ( Farhoud and Mehdi) on a call.

I have already created a swarm of two Boxes (Box0 and Box1) using docker-compose.
I connect to Box0 from fsync passing in the path to a plaintext markdown file I want to share.
I send each person a link to fuludocs with my meeting code as a query param in the URL.
They connect to each Box from the fuludocs client and the markdown file is rendered in the browser.
I edit the file and the updates are reflected in each browser window in real time.

I take down Box1..
and I make edits to the shared text file again..
Mehdi is unable to view the updates in the client because he connected to Box1..
however, Farhoud is still able to view the updates since he connected to Box0.

Mehdi is also able to connect to Box0 and recover the latest updates to the document.

I close the fsync application..
and everyone is still able to view the notes after the meeting because they are permanently saved by each healthy Box.
