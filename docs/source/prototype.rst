Prototype Functions
===================

Video Elements
--------------

createFreeVideoElement
----------------------

Used in ``getFreeVideoElement``.

Creates a new video element that can be used.

Returns the new video element

getFreeVideoElement
-------------------

Used in ``renderVideo``.

Returns an available unused video element.

Internally calls createFreeVideoElement if there are no available video elements.

renderVideo
-----------

Allocates a stream to a video element.

- Returns 0 if successful

- Returns -1 if unsuccessful

.. code-block:: javascript
    
    let result = renderVideo(inputStream);
    if (result == 0) {
        console.log("Success!");
    } else if (result == -1) {
        console.log("Failure.");
    }

connectToOthers
---------------

Create connections to all ids in data.

Ignores peers that have already been connected to.

.. code-block:: javascript
    
    let listOfIds = [123, 456, 789];
    connectToOthers(listOfIds);

createPeerConnection
--------------------

Establishes an RTCPeerConnection to the provided id, reading from the prototype's ``peerIdElement`` if no id was provided.

.. code-block:: javascript
    let id = 123456789;
    createPeerConnection(id);
    // A connection has now been established with the peer with <id>!


