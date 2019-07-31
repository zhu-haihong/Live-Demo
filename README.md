# Live Video Streaming: Framework and Demo
## Framework
![Alt text](https://github.com/ullstreaming2020/livestreaming_demo/blob/master/pic.png)
* The figure illustrates the architecture of our chunk-based live video streaming system.
  1. On the server side, video data from camera or other sources are encoded into multiple rates in realtime by the H.264 encoder. The encoded frames will be packaged into chunks and put in the sending buffers waiting for requests. The Request Handler is Websocket-based, which delivers the requested video chunks to the client. On the client side, the received video chunks are appended into a receiving buffer, waiting to be decoded by the web based decoder and rendered using WebGL.
  1. In the RL Agent, the DRL model, which is trained offline using network bandwidth traces, instructs the RL agent to select a proper rate at each time of requesting, based on the state information collected from network monitor, buffer status and the player.
## Demo
* If you want to check the system, please run the demo through the link:
https://www.youtube.com/watch?v=eNjBfOFfj1I
