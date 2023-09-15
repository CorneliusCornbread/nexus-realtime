The goal of this project is to create an open standard for connected social games communication, be it XR, VR, Game Consoles, PCs, Phones, or some other device that can effectively work in 3D space.

This specification has been written in markdown using [Obsidian](https://obsidian.md/), for the best reading experience it's recommended to use Obsidian to read this spec. This spec however, can be read anywhere markdown reading is supported, including GitHub.

# Fundamental communication standards
The Nexus-Realtime protocol uses a protocol known as [KCP](https://github.com/skywind3000/kcp/blob/master/README.en.md), a protocol designed and created by [skywind3000](https://github.com/skywind3000), in addition to regular UDP for unreliable transmission. While KCP itself does not define a specific protocol to build upon, our implementation will be built upon UDP[[#Footnote 1|(1)]], beyond that see KCP's specification [here](https://github.com/skywind3000/kcp/blob/master/README.en.md). KCP has been chosen because of its incredibly low latency in comparison to TCP, while still being reliable.

## KCP
KCP is used for reliable transmission during the realtime connection, KCP requires a session number which will be gathered during the [[Initial Connection Handshake|initial handshake]] that creates the realtime stream. 

## UDP
UDP is used for unreliable transmission of data, for example transmission of voice packets will be sent over UDP. See [[Voice Transmission]] for more details

### Footnote 1
Currently this protocol only supports server architectures. It's possible in the near future this could change, however, to limit the scope of this specification it will be limited only to client-server based communications as opposed to P2P communications.