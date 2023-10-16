The goal of this project is to create an open standard for connected social games communication, be it XR, VR, Game Consoles, PCs, Phones, or some other device that can effectively work in 3D space.

This specification has been written in markdown using [Obsidian](https://obsidian.md/), for the best reading experience it's recommended to use Obsidian to read this spec. This spec however, can be read anywhere markdown reading is supported, including GitHub.

# Fundamental communication standards
The Nexus-Realtime protocol uses a protocol known as [QUIC](https://quicwg.org/), a protocol designed and created by Jim Roskind at Google. QUIC has been chosen because of its incredibly low latency in comparison to TCP, while still having the option to be reliable. It's also a battle tested protocol, being used in the industry for many years. However, we use UDP for querying to reduce bandwidth usage and load on servers.


### Footnote 1
Currently this protocol only supports server architectures. It's possible in the near future this could change, however, to limit the scope of this specification it will be limited only to client-server based communications as opposed to P2P communications.