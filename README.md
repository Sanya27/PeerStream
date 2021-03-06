Multi-Client WebRTC Video
=========================

Based on https://github.com/shanet/WebRTC-Example, see [https://shanetully.com/2014/09/a-dead-simple-webrtc-example/](https://shanetully.com/2014/09/a-dead-simple-webrtc-example/) for a description of WebRTC basics.

## Usage

The signaling server uses Node.js and `ws` and can be started as 
follows:

```
$ npm install
$ npm start
```

With the server running, open Chrome and go to to `https://[server]` from any client on the LAN.

Optionally, use a URL parameter to specify the client display name, e.g. `https://[server]/?displayName=Boston`

You may have conflicting tasks already using the default HTTP and/or 
HTTPS ports (80 and 443), which will result in an error on startup. 
Change the constants in server.js and go to 
https://localhost:[HTTPS_PORT]

For production, the server can be deployed as a Windows service using 
node-windows, which can be installed as follows:

```
npm install -g node-windows
node install_service.js
```
Steps to start-->

Run npm install OR npm install --save ws in the terminal opened in PeerStream Directory.
IF RUNNING ON LAN :

In the file, webrtc.js in client directory, Uncomment line 75 and replace the IP by your IP. Also comment the line 76.

                     OR  
IF EXPOSING APP TO INTERNET -- ngrok can be used for making our local webApp public :

Just install ngrok and go to the directory where it is installed and run --> ./ngrok http https://localhost:8443

Run npm start in the terminal opened in PeerStream Directory

Open the client with ngrok provided web address OR https://YourIP:8443 (in case of LAN). First Client to connect to server is the Master. Every subsequent client is stream receiver and relayer.

Check these slides for more information about the algorithm implemented.

'https://docs.google.com/presentation/d/1YLxouDWRVHrKxgG6sKfOq8Ge4pQXBH7tD2rU1WpY1Yo/edit?usp=sharing'
