Client API
==========

To use the api, first get the file from:

[ TO DO: Insert link here ]

api.createPeer()
--------------

Creates a new WebRTCPeer object, which can be used to access more methods.

Returns the new WebRTCPeer object

.. code-block:: javascript

   let peer = api.createPeer();

peer.createConnection(id)
-------------------

Establish an RTCPeerConnection to ``id``

.. code-block:: javascript
   
   let id = 123456789;
   let peer = api.createPeer();
   peer.createConnection(id);

peer.assignOnStreamReceived(function)
-----------

Call ``function`` when a stream is received

.. code-block:: javascript
   
   let peer = api.createPeer();
   peer.assignOnStreamReceived((stream) => {
      console.log("Received stream!");
      console.log(stream);
   });

peer.assignOnDataReceived(function)
---------------

Call ``function`` whenever data is received

.. code-block:: javascript
   
   let peer = api.createPeer();
   peer.assignOnDataReceived((data) => {
      console.log("Received data!");
      console.log(data);
   })

peer.assignOnConnectionReceived(function)
--------------------

Call ``function`` whenever a new connection is received

.. code-block:: javascript
   
   let peer = api.createPeer();
   peer.assignOnConnectionReceived((connection) => {
      console.log("Received connection!");
      console.log(connection);
   });

peer.getConnections()
--------------------

Returns a list of the currently connected ids

.. code-block:: javascript
   
   let peer = api.createPeer();
   let connections = peer.getConnections();
   console.log("Current Connections:");
   console.log(connections);

peer.closeConnection(id)
--------------------

Returns a list of the currently connected ids

.. code-block:: javascript
   let id = 123456789
   let peer = api.createPeer();
   peer.closeConnection(id);
   // We are no longer connected to the peer with <id>


