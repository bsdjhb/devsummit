FreeBSD 14.0 Planning
===
 
# Have

Things that already exist out of tree and can be upstreamed in the next 2 years (perhaps needing work to get to an upstreamable state)

| Thing                     | Owner    | Committed |
| --                        | --       | -- |
| nvlist(9)-based interface in /dev/sndstat| khng300@gmail.com | [D26884](https://reviews.freebsd.org/D26884) |
| Hole-punching for vnode | khng300@gmail.com | |
| bhyve/arm64 | andrew/UPB | -- |
| Merging Morello support (from CHERI) | brooks/jhb | -- |
| Convert stdio fileno to int | jhb | -- |
| Wireguard (kernel) | mmacy | [r368163](https://svnweb.freebsd.org/base?view=revision&revision=368163) |


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
| Modern virtio (1.x) client drivers | bryanv? / jhb | -- |
| arm64 Scalable Vector Extension | mhorne | -- |
| brand new shell (or import something else) | bapt/manu | -- |
| chacha20+poly1035 AEAD support for KTLS | jhb | -- |
| chacha20+poly1035 AEAD support for IPsec | jhb | -- |
| exFat | delphij / cem | [D27376](https://reviews.freebsd.org/D27376) |
| suspend/resume arm64 + riscv | mhorne + will seek mentorship | -- |
| low power idle/S0ix support (see bwidawsky's earlier work) | jhb? | |
| dwc_mmc SDIO | bz | -- |


# Axe Candidates

Things we might like to deprecate for 14.0.  Further discussion may be required to reach consensus.

| Thing                           | Owner     | Committed |
| --                              | --        | -- |
| asym crypto support via /dev/crypto | jhb | deprecation committed |
| Firewire support | imp | -- |
| armv6? | imp/manu | -- |
| telnetd | adrian/allanjude | -- |
| ftpd (for 13) | emaste/allanjude | -- |
| smbfs v1 (last user of DES in the kernel) | emaste | -- |
| mips??? | imp | -- |
| arm SoC support review (maybe for 13) | imp | -- |
| sendmail | manu/??? | -- |
| boot loader 4th support | imp | -- |
| svnlite | lwhsu | -- |
| NIS "crypto" | cem | -- |
| NIS | kaktus | -- |



