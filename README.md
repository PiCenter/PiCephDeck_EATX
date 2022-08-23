# 220823 [background check stage]

> A plan for building up CEPH cluster by RBPi (CM4 .etc) or other linux cards to replace x86 dual CPU NAS server, purpose for having high availability with no higher power consumption.

### The main question is: why need ceph with low power consumption?

Well, as a international student who will go abroad soon, I hope the NAS in my parents' home can keep running all the time. Obviously, I can't have my parents do O&M for my NAS server, and I can't use a data-center-level solution that uses too much power. My current 4U servers running ESXi and Truenas SCALE, totaling 80 CPU threads and 134GB of ram, have made my parents reluctant to support my fidgeting. Therefore, I must make sure that the NAS at home is light enough during my study abroad.

### This proj is currently in background check stage

While I research this idea with google, I found a product almost realized what I had in mind - Jeff Geerling (@geerlingguy), who introduced a ITX motherboard with 6 CM4s, which is good for running ceph. `https://www.youtube.com/watch?v=ecdm3oA-QdQ`

However, this product is not completely in line with my idea. Some features I want is different:

- The board size should be in E-ATX or SSI-EEB
- Core boards should be mounted on a separate expansion cards to make full use of the three-dimensional space of the 3U/4U chassis
- Each core should have a separate PCIE slot to install HBA cards, cache SSDs or other high-speed IO cards
- Can be easily obtained in China

