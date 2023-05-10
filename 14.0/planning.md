FreeBSD 14.0 Planning
===
 
# :heavy_check_mark: Completed

Things that have been committed to the tree.

| Thing                     | Owner    | Committed / Review / Patch |
| --                        | --       | -- |
| nvlist(9)-based interface in /dev/sndstat| khng | [c96151d33509](https://cgit.freebsd.org/src/commit/?id=c96151d33509655efb7fb26768cb56a041c176f1) |
| bhyve configuration | jhb | [621b5090487d](https://cgit.freebsd.org/src/commit/?id=621b5090487de9fed1b503769702a9a2a27cc7bb)
| Modern virtio (1.x) client drivers | bryanv | [9da9560c4dd3](https://cgit.freebsd.org/src/commit/sys/dev/virtio/virtio.c?id=9da9560c4dd3556519cd391a04f0db157dc3c295) |
| chacha20+poly1035 AEAD support for KTLS | jhb | [9c64fc40290e](https://cgit.freebsd.org/src/commit/?id=9c64fc40290e08f6dc6b75aa04084b04e48a61af) |
| Sound pin patches from GitHub | imp | [ef790cc7407e](https://cgit.freebsd.org/src/commit/?id=ef790cc7407e827db9563d08a52a71ab36436986) |
| Hole-punching for vnode | khng | [de2e15295966](https://cgit.freebsd.org/src/commit/?id=de2e15295966) |
| kvmclock driver for freebsd guests | allanjude | [6fa88a627d5e](https://cgit.freebsd.org/src/commit/?id=6fa88a627d5e) and [6c69c6bb4c7f](https://cgit.freebsd.org/src/commit/?id=6c69c6bb4c7f) |
| minidump live system | mhorne/allanjude | [0a5c04a8926e](https://cgit.freebsd.org/src/commit/?id=0a5c04a8926e) |
| KTLS NIC receive | kib/hselaskey | [fe8c78f0d202](https://cgit.freebsd.org/src/commit/?id=fe8c78f0d202) |
| Removed asym crypto support via /dev/crypto | jhb | [76681661be28](https://cgit.freebsd.org/src/commit/?id=76681661be2859622872c3a8a1bd68260403ddd0) |
| Removed mips | imp | [c09981f1422e](https://cgit.freebsd.org/src/commit/?id=c09981f1422ef0d44042dacc5d1265392fba39f1) and others |
| Removed svnlite | lwhsu | [a2bc17474b96](https://cgit.freebsd.org/src/commit/?id=a2bc17474b962ba9e29c4526356203fe48a549eb) and [0333fad1b7e0](https://cgit.freebsd.org/src/commit/?id=0333fad1b7e0) |
| Removed an(4) | manu | [663b174b5b53](https://cgit.freebsd.org/src/commit/?id=663b174b5b53) |
| NVMe error recovery rewrite | imp | [9bbd0a7ca999](https://cgit.freebsd.org/src/commit/?id=9bbd0a7ca999) and [502dc84a8b67](https://cgit.freebsd.org/src/commit/?id=502dc84a8b67) |
| Union GEOM facility | kirk | [c7996ddf8000](https://cgit.freebsd.org/src/commit/?id=c7996ddf8000cfb19a9e91a636f56747860d03d7) |
| ISA soundcard driver retirement | emaste | [df51e63eb5d7 (ad1816)](https://cgit.FreeBSD.org/src/commit/?id=df51e63eb5d7e34e7a79da144e962dbf5e7cdb4c) [aa83e9b189d6 (ess)](https://cgit.FreeBSD.org/src/commit/?id=aa83e9b189d67c8aa772fed4f9dd26cbcbff4e3f) [754decef384a (gusc)](https://cgit.FreeBSD.org/src/commit/?id=754decef384a1ab30b39704264742fa33bfa365e) [5126e5eeeb5e (mss)](https://cgit.FreeBSD.org/src/commit/?id=5126e5eeeb5e07ceef3c809452a8c9f508b2d4d1) [5126e5eeeb5e (sbc/sb8/sb16)](https://cgit.FreeBSD.org/src/commit/?id=716924cb4832ea0a440daf09913a06f3166f243e) |
| DPAA2 | bz | Working with Dmitry Salychev https://github.com/mcusim/freebsd-src/commits/lx2160acex7-dev |
| wireguard module | emaste | probably merged in late June/July |
| OpenVPN DCO | kp | [D34340](https://reviews.freebsd.org/D34340) |
| 16k PAGE_SIZE on arm64 | andrew | [D34793](https://reviews.freebsd.org/D34793) |
| ZFS support in makefs(8) | markj | [D35248](https://reviews.freebsd.org/D35248) |
| ARM64 PMC: CMN-600 driver | ray / tsoome | [D32321](https://reviews.freebsd.org/D32321) |
| ARM64 PMC: DMN-620 driver | ray / tsoome | [D32670](https://reviews.freebsd.org/D32670)
| Review inpcb synchronization (SMR) | glebius| [de2d47842e88](https://cgit.freebsd.org/src/commit/?id=de2d47842e880281da07f2589b9ec558b42c09c1)|
| Cross-building ftp/(mini-)memstick/disc1 images from non-FreeBSD | jrtc27 | various |

# :airplane: Have

Things that already exist out of tree and can be upstreamed in the next 2 years / before the next release (perhaps needing work to get to an upstreamable state)

| Thing                     | Owner    | Committed / Review / Patch |
| --                        | --       | -- |
| bhyve/arm64 | andrew/UPB | [Andrews GitHub branch](https://github.com/CTSRD-CHERI/freebsd-morello/tree/bhyvearm64) |
| Merging Morello support (from CHERI) | brooks/jhb | Timing/funding questions, probably refactoring/prep for 14.x but no actual support |
| Convert stdio fileno to int | jhb | gnulib workaround needs resolving to make FILE opaque |
| chacha20+poly1035 AEAD support for IPsec | ae | https://people.freebsd.org/~ae/ipsec-chacha.diff |
| IPMI attachment for ARM64 | allanjude + Ampere | [D28707](https://reviews.freebsd.org/D28707) still needs a bit of work |
| Hardware accelerated SHA2 in ZFS | allanjude | [PR252316](https://bugs.freebsd.org/bugzilla/show_bug.cgi?id=252316) |
| ARM Mali Txxx/Gxx GPU support (Panfrost) | br | exists, but depends on [DRM for arm64 project](https://github.com/evadot/drm-subtree/) | 
| camcorder / camdump | imp | Some polish and dependency issues (reviews expected Q1 2023) |
| 9pfs client (pass filesystem from host to guest) | stevek | (https://github.com/Juniper/virtfs) |
| DTrace for VMs (from the host), but a giant diff | dstolfa | (https://github.com/cadets/freebsd) |
| virtqueue SDT probes (for monitoring requests/replies) | stevek | patches to be contributed |
| Fix for mdroot race (md(4) may not add to rootdevnames before conf0 is generated) | stevek | patches to be contributed |
| dwc_mmc SDIO | manu | -- |
| Full GPU Passthough for bhyve(8) and edk2 | manu / corvin | -- |
| DRM in base for amd64/armv7/arm64  | manu      | |
| Debugger command restrictions via MAC | mhorne | [D35370](https://reviews.freebsd.org/D35370) |
| KASAN for ARM64 | mhorne | ~1-2 months |
| tarfs (mount a compressed tar file) | des / thj | in progress |
| LinuxBoot support for amd64 and aarch64 | imp | In progress, reviews expected Q3 2022 |
| nvme dynamic namespace support | imp | Patches in progress, reviews expected Q3 2022 |
| Linux compatibility for sys/endian.h and byteswap.h | imp | [D32051](https://reviews.freebsd.org/D32051) mopping up compat issues | 
| jectl (boot environments for jails) | rew / allanjude | [github: jectl](https://github.com/KlaraSystems/jectl) - testing |
| Serial console over USB xHCI Debug | hrs | in progress, expected in July 2022 |
| syslogd(8) rewrite to support TCP and TLS | hrs | in progress, expected in July 2022 |
| Various bhyve suspend/resume fixes | | in review |
| arm64 boot from iscsi | emaste / dch | [src](https://github.com/khng300/freebsd-src/tree/khng/current/iscsi) https://reviews.freebsd.org/D34475 + https://reviews.freebsd.org/D34476 + https://reviews.freebsd.org/D34477 |
| arm64 Scalable Vector Extension | andrew | -- |
| pmcstat for PIEs | jrtc27 | [D39595](https://reviews.freebsd.org/D39595) |
| pmcstat for separate debug files | jrtc27 | in progress (reworking [D39626](https://reviews.freebsd.org/D39626)) |
| lposix - add more posix functions to flua in base | kevans | [D39083](https://reviews.freebsd.org/D39083) |
| jail devctl | dch / jamie | [jail_devctl](https://github.com/fubarnetes/kmod_devctl_jail/) approx 200LoC |

# Need

Things that someone needs in the next two years to support a product or service

| Thing                  | Owner     | Committed / Review / Patch / Status |
| --                     | --        | -- |
| V4l2 in base           | manu      | |
| USB Video Class in base | manu     ||
| Default to pkgbase     | manu/emaste ||
| 802.11ac Wi-Fi support| bz | in progress |
| TB3 / USB4 support | !! (see emaste if interested) | (erj and hps are interested) [usb4]https://github.com/hselasky/usb4 [dpc for hotplug]https://github.com/linnemannr/dpc |
| DDC monitor control support (ddccontrol) | manu | almost done, kernel support is present, Linux tool needs to be ported |
| Inline IPsec (NIC assisted with encryption / decryption) | kib/hselaskey | |
| Hetergenuous core scheduler (big.LITTLE / AlderLake) | emaste/mav/thj | -- |
| Revisit security knob defaults | emaste/mw | -- |


# Want

Things that would be nice to have but aren't critical

| Thing                           | Owner     | Committed / Review / Patch / Status |
| --                              | --        | -- |
| eBPF (use cases, e.g., linuxemul seccomp needs this; software-defined networking maybe; linux-style tracing) https://ebpf.io/summit-2020/ | hrs (as a mentee maybe: 0mp) |    |
| Failsafe ~~ZFS~~ bootcode           | allanjude/imp | bootonce is done, now to the hard part (bootcode itself) |
| smbfs (client) v2 & v3          | !! | ?? |
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
| exFat | delphij / cem | [D27376](https://reviews.freebsd.org/D27376) |
| suspend/resume arm64 + riscv | mhorne | -- |
| low power idle/S0ix support (see bwidawsky's earlier work) | jhb?? | (perhaps needs a link to Ben's branch) |
| Intel Icelake HWPMC | allanjude + Alexander@NetApp / possibly mhorne | merged by mav@. Remaining problem is Alder Lake. |
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
| Intel SKL HDA sound controller (in X1 carbon 7th gen) [firmware](https://github.com/thesofproject) https://bugs.freebsd.org/242527 | emaste | (needed for mic, but mic on newer Framework laptop works fine) |
| An "ip" command similar to Cisco/Linux | cy | -- |
| OCI support for containers | dfr | -- |
| nullfs for single files / overlayfs | dfr | -- |
| native vt(4) backend for nvidia.ko | jhb | -- |
| dhcpcd | emaste | [D22012](https://reviews.freebsd.org/D22012), [freebsd-net thread](https://lists.freebsd.org/pipermail/freebsd-net/2019-October/054474.html) |
| tmux | ??? | if we don't get pkgbase then tmux in base as a panacea |

# Axe Candidates

Things we might like to deprecate for 14.0.  Further discussion may be required to reach consensus.

| Thing                           | Owner     | Committed / Review / Patch |
| --                              | --        | -- |
| Firewire support | imp | -- |
| armv6? | imp/manu | -- |
| arm SoC support review | imp | done by manu? |
| telnetd | adrian?? | ported: net/freebsd-telnetd |
| ftpd (for ~~13~~14) | emaste/allanjude | ported: ftp/freebsd-ftpd |
| smbfs v1 (last user of DES in the kernel) | emaste | Can't remove until there is a replacement |
| sendmail | bapt | dma now default |
| boot loader 4th support | imp | [PR257018](https://bugs.freebsd.org/bugzilla/show_bug.cgi?id=257018) solve first (lua/ZFS/... non-UEFI PXE loader too large) |
| NIS "crypto" | cem | -- |
| NIS | kaktus | Still has active users |
| remaining ATM support (netgraph) | brooks | -- |
| Lingering obsolete CAM drivers (FCP) (twe/twa) | imp | -- |
| publicwkey(5) | manu | [D30683](https://reviews.freebsd.org/D30683) [D30682](https://reviews.freebsd.org/D30682)|
| targ(4) CAM target driver | imp | -- |
| fingerd | ?? | -- |
| Security knob menu in installer | emaste | -- |
| 3dfx(4) | jhb | -- |
| syscons(4) (deprecation at least) | emaste / manu | -- |


# Legend
| Symbol | Meaning |
| -- | -- |
| ?? | Status is in question |
| !! | Needs a new owner |



