# Game networking

This text has the objective to give the basics to understand game networking and some issues that comes with it.

## What is LAN?

LAN is a local network only available to computers inside it, most noticeable in games that have a local play option like Minecraft's open to LAN feature, that hosts a game in the machine and opens the server to computers in the Local Area Network, something that helps with lag, as there is only the client, network switch and the host application processing time in the pipeline.

### Differing LAN from WAN
WAN is a type of network similar to LAN to the end-user, with the most distinguishing features being that it is more sensitive to lag, the host being in an external network, and sometimes is even located on a different continent.

### Why does WAN has so many problems?
With WAN making the server located in a different region than the client, it increases the data transmission time, as even light has a latency when transmitting it in long distances, but the most noticeable issue is processing the forwarding of the data from the various nodes in the way to the desired computer and the processing time that host needs to send an answer back.

## Ping

### what is ping?
Ping is a popular form of referring to latency. It is the time it takes from the local data package to be received by an external server and the client receives an answer from the server.

### Why does ping matter?
When using a time-sensitive application, it can decrease the responsiveness, popularly referred to as lag, and sometimes even cause synchronization problems between clients and the host, something popularly referred to as desync.

### Desync
When using an applicating suffers desync, it is possible to notice differences between clients and hosts, with the most noticeable ones being: 
- Assets not appearing to the client that suffered desync, also known as replication issues.
- The host receives impossible results from the client.

### Lag
When there is a long delay between sending and receiving data, the application may wait for the new packages to execute an action as a way to avoid a desync, something that can cause the lack of responsiveness in games.

A way to decrease the latency is to minimize the connection points that happen when using VPNs and matchmaking services, as it introduces more processing time as forwarding requests need to be processed. Doing so can help a little, but opens the client to attacks like a vulnerability flaw in Crab game's Steamworks implementation that leaked streamer's IP addresses.

A good ping is considered below or near the rendering time, as it is the time that the player will be visually informed of any action taken by the game.
