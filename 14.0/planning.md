FreeBSD 14.0 Planning
===
 
# Have

Things that already exist out of tree and can be upstreamed in the next 2 years (perhaps needing work to get to an upstreamable state)

| Thing                     | Owner    | Committed / Review / Patch |
| --                        | --       | -- |
| nvlist(9)-based interface in /dev/sndstat| khng | [c96151d33509](https://cgit.freebsd.org/src/commit/?id=c96151d33509655efb7fb26768cb56a041c176f1) |
| Hole-punching for vnode | khng | [D27194](https://reviews.freebsd.org/D27194) |
| bhyve/arm64 | andrew/UPB | [Andrews GitHub branch](https://github.com/CTSRD-CHERI/freebsd-morello/tree/bhyvearm64) |
| Merging Morello support (from CHERI) | brooks/jhb | Timing/funding questions |
| Convert stdio fileno to int | jhb | -- |
| bhyve configuration | jhb | [621b5090487d](https://cgit.freebsd.org/src/commit/?id=621b5090487de9fed1b503769702a9a2a27cc7bb)
| Modern virtio (1.x) client drivers | bryanv | [9da9560c4dd3](https://cgit.freebsd.org/src/commit/sys/dev/virtio/virtio.c?id=9da9560c4dd3556519cd391a04f0db157dc3c295) |
| chacha20+poly1035 AEAD support for KTLS | jhb | [9c64fc40290e](https://cgit.freebsd.org/src/commit/?id=9c64fc40290e08f6dc6b75aa04084b04e48a61af) |
| chacha20+poly1035 AEAD support for IPsec | ae | (review open for ipsec?) |
| IPMI attachment for ARM64 | allanjude + Ampere | [D28707](https://reviews.freebsd.org/D28707) still needs a bit of work |
| Hardware accelerated SHA2 in ZFS | allanjude | [PR252316](https://bugs.freebsd.org/bugzilla/show_bug.cgi?id=252316) |
| NVMe error recovery rewrite | imp | [D28583](https://reviews.freebsd.org/D28583) rare races need to be resolved before committing. |
| Review inpcb synchronization (SMR) | glebius| in progress |
| kvmclock driver for freebsd guests | allanjude | [D29733](https://reviews.freebsd.org/D29733) + port for testing on existing releases: sysutils/kvmclock-kmod |
| ARM Mali Txxx/Gxx GPU support (Panfrost) | br | exists, but depends on [DRM for arm64 project](https://github.com/evadot/drm-subtree/) | 
| Sound pin patches from GitHub | imp | [D30619](https://reviews.freebsd.org/D30619) |
| camcorder / camdump | imp | Some polish and dependency issues |
| 9pfs client (pass filesystem from host to guest) | stevek | (https://github.com/Juniper/virtfs) |
| DTrace for VMs (from the host), but a giant diff | dstolfa | (https://github.com/cadets/freebsd/tree/dstolfa/hypertrace-cleanup, currently based on 13, merge soon) |
| wireguard module | emaste | |
| virtqueue SDT probes (for monitoring requests/replies) | stevek | patches to be contributed |
| Fix for mdroot race (md(4) may not add to rootdevnames before conf0 is generated) | stevek | patches to be contributed |
| dwc_mmc SDIO | manu | -- |



# Need

Things that someone needs in the next two years to support a product or service

| Thing                  | Owner     | Committed / Review / Patch / Status |
| --                     | --        | -- |
| DRM in base for amd64/armv7/arm64  | manu      | |
| V4l2 in base           | manu      | |
| USB Video Class in base | manu     ||
| Default to pkgbase     | manu/emaste ||
| 802.11ac Wi-Fi support| bz | |
| TB3 / USB4 support | !! (see emaste if interested) | (erj and hps are interested) |
| Intel SKL HDA sound controller (in X1 carbon 7th gen) [firmware](https://github.com/thesofproject) https://bugs.freebsd.org/242527 | emaste |  |
| DDC monitor control support (ddccontrol) | manu |  |
| OpenVPN DCO https://github.com/OpenVPN/ovpn-dco | grehan |  |
| minidump live system | mhorne/allanjude | work in progress |
| KTLS NIC receive | kib/hselaskey | |
| Inline IPsec (NIC assisted with encryption / decryption) | kib/hselaskey | |



# Want

Things that would be nice to have but aren't critical

| Thing                           | Owner     | Committed / Review / Patch / Status |
| --                              | --        | -- |
| eBPF (use cases, e.g., linuxemul seccomp needs this; software-defined networking maybe; linux-style tracing) https://ebpf.io/summit-2020/ | hrs (as a mentee maybe: 0mp) |    |
| Failsafe ~~ZFS~~ bootcode           | allanjude/imp | bootonce is done, now to the hard part (bootcode itself) |
| smbfs (client) v2 & v3          | 0mp?? | ?? |
| Better autotuning for things like R/W caching (from Axiado talk) | imp | |
| NPF                             | gnn??       |  |
| VPP on netmap                   | gnn??       |  |
| Rework of Routing Sockets       | gnn??       |  |
| ZFS ARC <-> vm page integration | jeff?? | |
| MPSAFE sysctl handlers          | kaktus??    | Partly done |
| Kill Giant dead and gone (looking for help) | imp | -- |
| Kill Giant in NEWBUS | imp | -- |
| Kill Giant in AT Keyboard driver and friends (want help) | imp | -- |
| jailctl: automated jail.conf tool in base with FW integration | https://twitter.com/antranigv ?? | (company has prototype; needs cleanup) | 
| Move more of ifconfig into libifconfig | freqlabs | still in progress 2021-06-10 |
| Cellular Drivers from ${Vendor} | gnn?? | |
| arm64 Scalable Vector Extension | mhorne | -- |
| exFat | delphij / cem | [D27376](https://reviews.freebsd.org/D27376) |
| suspend/resume arm64 + riscv | mhorne + will seek mentorship | -- |
| low power idle/S0ix support (see bwidawsky's earlier work) | jhb?? | (perhaps needs a link to Ben's branch) |
| Intel Icelake HWPMC | allanjude + Alexander@NetApp / possibly mhorne | -- |
| Make USE_LINUX=yes work for arm64 and add arm64 ports | Vincent Milum Jr. / emaste | -- |
| Remember original interface name | allanjude | [D28247](https://reviews.freebsd.org/D28247) |
| detach bpf(9) from ifnet(9) | glebius | - |
| synchronization for netgraph(9), most likely epoch(9) | glebius (can help advise) | - |
| Better Sound Quirk System (looking for help) | imp/emaste | - |
| Virtio-fs (uses fuse protocol as transport) | stevek/jhb | - |
| QEMU-user upstreaming efforts | imp/kevans | Warner upstreaming, Kyle day to day, more help needed to integrate Kyua testing |
| virtio monitoring tool(s) | stevek | in progress |
| s6-rc as pid 1 | crest | needs polish |
| sync pf(4) syntax with modern OpenBSD | !! | -- |
| loader - any info obtained via commands should also be made available to the language used by loader | stevek | -- |


# Axe Candidates

Things we might like to deprecate for 14.0.  Further discussion may be required to reach consensus.

| Thing                           | Owner     | Committed / Review / Patch |
| --                              | --        | -- |
| asym crypto support via /dev/crypto | jhb | [76681661be28](https://cgit.freebsd.org/src/commit/?id=76681661be2859622872c3a8a1bd68260403ddd0) |
| Firewire support | imp | -- |
| armv6? | imp/manu | -- |
| telnetd | adrian?? | -- |
| rlogin? rsh? libc(rcmd isruserok) | allanjude | -- |
| ftpd (for ~~13~~14) | emaste/allanjude | -- |
| smbfs v1 (last user of DES in the kernel) | emaste | Can't remove until there is a replacement |
| mips??? | imp | -- |
| arm SoC support review | imp | -- |
| sendmail | !! (emaste) | -- |
| boot loader 4th support | imp | -- |
| svnlite | lwhsu | disabled in head [a2bc17474b96](https://cgit.freebsd.org/src/commit/?id=a2bc17474b962ba9e29c4526356203fe48a549eb) |
| NIS "crypto" | cem | -- |
| NIS | kaktus | Still has active users |
| remaining ATM support (netgraph) | brooks | -- |
| Lingering obsolete CAM drivers (FCP) | imp | -- |
| Old Wireless Drivers -- an, etc | manu | [D30679](https://reviews.freebsd.org/D30679) |
| publicwkey(5) | manu | [D30683](https://reviews.freebsd.org/D30683) [D30682](https://reviews.freebsd.org/D30682)|


# Legend
| Symbol | Meaning |
| -- | -- |
| ?? | Status is in question |
| !! | Needs a new owner |



