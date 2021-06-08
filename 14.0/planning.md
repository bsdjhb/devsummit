FreeBSD 14.0 Planning
===
 
# Have

Things that already exist out of tree and can be upstreamed in the next 2 years (perhaps needing work to get to an upstreamable state)

| Thing                     | Owner    | Committed |
| --                        | --       | -- |
| nvlist(9)-based interface in /dev/sndstat| khng | [c96151d33509](https://cgit.freebsd.org/src/commit/?id=c96151d33509655efb7fb26768cb56a041c176f1) |
| Hole-punching for vnode | khng | [D27194](https://reviews.freebsd.org/D27194) |
| bhyve/arm64 | andrew/UPB | -- |
| Merging Morello support (from CHERI) | brooks/jhb | -- |
| Convert stdio fileno to int | jhb | -- |
| bhyve configuration | jhb | [621b5090487d](https://cgit.freebsd.org/src/commit/?id=621b5090487de9fed1b503769702a9a2a27cc7bb)
| Modern virtio (1.x) client drivers | bryanv | [9da9560c4dd3](https://cgit.freebsd.org/src/commit/sys/dev/virtio/virtio.c?id=9da9560c4dd3556519cd391a04f0db157dc3c295) |
| chacha20+poly1035 AEAD support for KTLS | jhb | [9c64fc40290e](https://cgit.freebsd.org/src/commit/?id=9c64fc40290e08f6dc6b75aa04084b04e48a61af) |
| chacha20+poly1035 AEAD support for IPsec | ae | -- |



# Need

Things that someone needs in the next two years to support a product or service

| Thing                  | Owner     | Committed |
| --                     | --        | -- |
| DRM in base for amd64  | manu      | |
| V4l2 in base           | manu      | |
| USB Video Class in base | manu     ||
| Default to pkgbase     | manu/???  ||
| 802.11ac Wi-Fi support| bz | |
| TB3 / USB4 support | bz | |
| Intel SKL HDA sound controller (in X1 carbon 7th gen) [firmware](https://github.com/thesofproject) https://bugs.freebsd.org/242527 | emaste | -- |
| DDC monitor control support (ddccontrol) | manu | -- |


# Want

Things that would be nice to have but aren't critical

| Thing                           | Owner     | Committed |
| --                              | --        | -- |
| eBPF (use cases, e.g., linuxemul seccomp needs this; software-defined networking maybe; linux-style tracing) https://ebpf.io/summit-2020/ | hrs (as a mentee maybe: 0mp) |    |
| Failsafe ZFS bootcode           | allanjude | bootonce, more to come |
| smbfs (client) v2 & v3          | 0mp       |    |
| Better autotuning for things like R/W caching (from Axiado talk) | imp | |
| NPF                             | gnn       |  |
| VPP on netmap                   | gnn       |  |
| Rework of Routing Sockets       | gnn       |  |
| ZFS ARC <-> vm page integration | jeff | |
| MPSAFE sysctl handlers          | kaktus    | Partly done |
| Kill Giant dead and gone        | imp | -- |
| Kill Giant in NEWBUS | imp | -- |
| Kill Giant in AT Keyboard driver and friends | imp | -- |
| Migrate CAM to NEWBUS | imp | -- |
| jailctl: automated jail.conf tool in base with FW integration | https://twitter.com/antranigv | (company has prototype; needs cleanup) | 
| Move more of ifconfig into libifconfig | freqlabs/??? | in progress |
| ARM LIMA/Panfrost GPU support | br/manu | -- |
| Cellular Drivers from ${Vendor} | gnn | |
| 9pfs client (pass filesystem from host to guest) | swills / stevek | -- |
| arm64 Scalable Vector Extension | mhorne | -- |
| brand new shell (or import something else) | bapt/manu | -- |
| exFat | delphij / cem | [D27376](https://reviews.freebsd.org/D27376) |
| suspend/resume arm64 + riscv | mhorne + will seek mentorship | -- |
| low power idle/S0ix support (see bwidawsky's earlier work) | jhb? | |
| dwc_mmc SDIO | bz | -- |


# Axe Candidates

Things we might like to deprecate for 14.0.  Further discussion may be required to reach consensus.

| Thing                           | Owner     | Committed |
| --                              | --        | -- |
| asym crypto support via /dev/crypto | jhb | [76681661be28](https://cgit.freebsd.org/src/commit/?id=76681661be2859622872c3a8a1bd68260403ddd0) |
| Firewire support | imp | -- |
| armv6? | imp/manu | -- |
| telnetd | adrian/allanjude | -- |
| ftpd (for 13) | emaste/allanjude | -- |
| smbfs v1 (last user of DES in the kernel) | emaste | -- |
| mips??? | imp | -- |
| arm SoC support review (maybe for 13) | imp | -- |
| sendmail | manu/??? | -- |
| boot loader 4th support | imp | -- |
| svnlite | lwhsu | disabled in head [a2bc17474b96](https://cgit.freebsd.org/src/commit/?id=a2bc17474b962ba9e29c4526356203fe48a549eb) |
| NIS "crypto" | cem | -- |
| NIS | kaktus | -- |



