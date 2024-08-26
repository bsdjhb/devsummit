FreeBSD 15.0 Planning
===
 
# :heavy_check_mark: Completed

Things that have been committed to the tree.

| Thing                     | Owner    | Committed / Review / Patch |
| --                        | --       | -- |
| arm64 Branch Target Identification | andrew   |  [d09a64e15d8f](https://cgit.freebsd.org/src/commit/?id=d09a64e15d8fad6588b9aad62979f20afa8441df)  |
| arm64 bhyve             | andrew | [47e073941f4e](https://cgit.freebsd.org/src/commit/?id=47e073941f4e7ca6e9bde3fa65abbfcfed6bfa2b) |
| single step AMD CPUs in bhyve | jhb Bojan | [e3b4fe645e50](https://cgit.freebsd.org/src/commit/?id=e3b4fe645e50bfd06becb74e52ea958315024d5f), [ca96a942cafb](https://cgit.freebsd.org/src/commit/?id=ca96a942cafb58476e10e887240e594e7923a6e8) |
| DDB pretty-print with CTF | markj Bojan | [c21bc6f3c242](https://cgit.freebsd.org/src/commit/?id=c21bc6f3c2425de74141bfee07b609bf65b5a6b3) |
| Cross kldxref                   | jhb | [0299afdff145](https://cgit.freebsd.org/src/commit/?id=0299afdff145e5d861797fe9c2de8b090c456fba) |
| copy_file_range(2) in install(1) | mmatuska | [5a50d52f112a](https://cgit.freebsd.org/src/commit/?id=5a50d52f112a86ebd0696da6564c7c7befa27f5d) |
| NVMe-oF/TCP            | jhb | [a8089ea5aee5](https://cgit.freebsd.org/src/commit/?id=a8089ea5aee578e08acab2438e82fc9a9ae50ed8) |
| per-file nullfs                 | dfr | [521fbb722c3](https://cgit.freebsd.org/src/commit/?id=521fbb722c33663cf00a83bca70ad7cb790687b3) (doesn't support sockets) |
| Port of the 9p filesystem | dfr | [e97ad33a89a7](https://cgit.freebsd.org/src/commit/?id=e97ad33a89a78f55280b0485b3249ee9b907a718) |
| NVMe Reset / Recovery Improvements | imp | [aa41354349c1](https://cgit.freebsd.org/src/commit/?id=aa41354349c16ea7220893010df78b47d67d0f74) |

# :airplane: Have

Things that already exist out of tree and can be upstreamed in the next 2 years / before the next release (perhaps needing work to get to an upstreamable state)

| Thing                     | Owner    | Committed / Review / Patch |
| --                        | --       | -- |
| copy_file_range() in mv(1) | pjd | [D45243](https://reviews.freebsd.org/D45243) |
| better copy_file_range() fallback/wrapper | pjd | [D45243](https://reviews.freebsd.org/D45243) |
| arm64 SVE                 | andrew   | [D43306](https://reviews.freebsd.org/D43306) |
| amd64/arm64 rescue kernel | markj / Klara | |
| iovec wrappers         | brooks | |
| Hardware watchpoints in bhyve guests | jhb Bojan | |
| Inline function tracing with dtrace | markj Christos | |
| GSoC: squashfs                       | chuck | |
| Improvments to Powerd on multicore laptops | cperciva | (talk to gallatin@) |
| Assorted CHERI pre-reqs (ABI bits) | brooks | |
| Hierarchical ratelimits in ZFS | pjd | [16205](https://github.com/openzfs/zfs/pull/16205) |
| simple library ABI checker | brooks | prototype [D44271](https://reviews.freebsd.org/D44271) |
| Graphical installer | khorben | [D44279](https://reviews.freebsd.org/D44279) [D44670](https://reviews.freebsd.org/D44670) [D44671](https://reviews.freebsd.org/D44671) [D44672](https://reviews.freebsd.org/D44672) [D44673](https://reviews.freebsd.org/D44673) [D44674](https://reviews.freebsd.org/D44674) [D45000](https://reviews.freebsd.org/D45000) |
|bhyve direct Linux loader|robn|(see [post to freebsd-virtualization](https://lists.freebsd.org/archives/freebsd-virtualization/2024-May/002112.html))|

# 🚧 In Progress

| Thing            | Owner | Status |
| --               | --    | --     |
| AMD IOMMU driver | kib   |        |
| certctl rewrite  | des   | [D42320](https://reviews.freebsd.org/D42320) |
| DRM back in base | manu  | 90% done |
| devd events for disk errors additional info | imp | 75% |
| Modularize default TCP stack | jtl | Code done; needs UX support to make it easy for users to use |
| UnionFS that actually works! (overlayfs) | olce | Starting (roadmap exists) |
| Standards-compliant, practical scheduling priorities | olce | 75% |
| SO_SPLICE        | Klara / markj | just starting |
| rootless bhyve   | markj | in progress
| kboot support for amd64    | imp    | Late Summer 2024 80% |
| Lua 5.4.7 update for flua and boot loader | imp | release in coming weeks, looks "boring" |
| Integrate loader command line editing from my GSoC student's code | imp | git rebased branch available, need assistance |
| riscv64 bhyve | br | [boots FreeBSD in simulator](https://wiki.freebsd.org/riscv/bhyve) |

# 💸 Need

Things that someone needs in the next two years to support a product or service

| Thing                  | Owner     | Committed / Review / Patch / Status |
| --                     | --        | -- |
| new ELF kernel dump format         | jhb markj | |
| bsdinstall support for pkgbase | emaste manu? | |
| Integrate pkgbase into release and so processes | re, so | can we please have a makefile per package|
| pkg groups | bapt | |
| Poudriere support for toolchain-less jails | allanjude | |
| External toolchain support          | brooks | |
| Pre-commit CI src, doc                  | lwhsu imp bofh | `make ci` WIP. Need to integrate with oth|
| Improve `make ci` to make it useful for committers | imp, bofh| |
| Improve `make ci` to make it useful for things like landing github pull requests | imp | |
| Pre-commit CI ports                | lwhsu will check with bapt and decke | bofh seems have some PoC|
| Universal Flash Storage driver | loos | Needed for some embedded deploys, but more universal in the future. Coming to Intel platforms soon. Also useful for LinuxBoot. |
| DTrace's `-C` (capital C) to work again | antranigv, markj | PR not submitted yet, just run `dtrace -c` and see many include |
| Refined bsd-user support for release process | imp, dfr, cperciva  | 32 on 64 issues, update very old qemu-bsd-user-static port |
| refine bsd-user binfmt etc to be jail friendly | cperciva, imp | Colin would like to have per-jail settings for these things |
| bsd-user + poudriere support for RISCV | imp, mhorne, jrtc27 | Package building totally broken, but basic stuff works, needs work so we can have riscv pacakges again |
| github runner for pull requests | imp | Possible ways out of cirrus-ci hole |
| github actions for quality of experience for external contributors | imp | Need help here |
| S0ix low idle | obiwac, jhb | |
| Native inotify(2) | tcberner | Many ports need this |
| What OpenSSL version should 15.0 ship with | gtetlow | run newer version in main to get soak time |
| don't ship OpenSSL FIPS | gtetlow | The module is not validated, don't let people get fooled |

# 🥺 Want 🙏

Things that would be nice to have but aren't critical

| Thing                           | Owner     | Committed / Review / Patch / Status |
| --                              | --        | -- |
| cleanup `make -s` | jhb | clean up warnings and keep it under control 🔥 |
| TPM support (GELI, ZFS)         | allanjude tsoome | -- |
| ZFS encrypted boot support      | tsoome allanjude | UEFI only |
| smbfs replacement (v2 or better)| emaste jhixson | -- |
| virtio-fs | ??? asomers | imp says patches exist |
| Updates to syscall table generation in Lua (libification of makesyscalls.lua) | imp | |
| Streamlined installer (single disk, better defaults, i.e. mash enter until done)           | emaste brd | |
| extend per-file nullfs for sockets/fifos | dfr | |
| more container support (OCI)   | dfr | need volunteers. Containerd port needs maintainer. Official images/repo |
| MINIMAL kernel                  | imp  | in progress |
| Boot loader support for devmatch | imp manu | PCI and USB |
| rewrite config(8) (in lua?)      | imp kevans |  |
| merge devmatch and devd (lib-ification) | imp | meena would like to help with this |
| scheduler and VFS documentation coverage | mhorne, olce | |
| Scheduling on non-uniform cores (P, E) | olce, mkarels | I think others are interested |
| finish kernel doc (man section 9) audit | mhorne | |
| reduce the GIANT hacks | jhb imp | |
| Better i18n support for vt(4) (CJK fonts, unicode fonts display (i.e., emoji), input method)|fanchung| Have a [IME PoC](https://wiki.freebsd.org/SummerOfCode2021Projects/InputMethodInFreeBSDVirtualTerminal) in GSoC'21 | 
| tarfs as root                 | imp | |
| overlayfs (for tarfs)         | Klara / allanjude | |
| Support for rust in the kernel | brooks | |
| Support for rust in userland | brooks | |
| netlink for ZFS (zfsd/zed) | allanjude | |
| netlink to replace devd socket | bapt | has Kernel part |
| UCLification of login. conf | meena | allanjude has the beginnings of a patch: [D25365](https://reviews.freebsd.org/D25365) |
| libxo for remaining network tools | meena |can I ask people ping phil@ on proposed new tags |
| hierarchical dynamic login classes | ngor, meena | |
| arm64 support for gve(4), needed by arm64 instance of GCE  | delphij, kibab (lwhsu's pushing them)|
| Remove MAC "label" limitations | allanjude des | use OSD? Build on bapt's per-jail mechanism used for mac_do |
| PID namespaces for jails | pjd dfr allanjude | which other namespaces might you want? |
|Import dhcpcd into base|| Initial (dated) version here: [D22012](https://reviews.freebsd.org/D22012)|
| netlink access to jail vnet | dfr | |
| ability to wire file content in memory while hashing | sjg (wants) | for mac_veriexec |
| update flua to have more standard bindings, more 'common' bindings and some FreeBSD system calls. | markj, imp | boot loader also uses Lua, so some care is needed here. |
| priv(1) | pjd | ability to reduce process' privileges |
| rctl | dfr, pjd? | current rctl does not work well for resource limiting jails |

# 🗑️ Axe Candidates 🪓

Things we might like to deprecate.  Further discussion may be required to reach consensus.

| Thing                           | Owner     | Committed / Review / Patch |
| --                              | --        | -- |
| Firewire 🔥                     | imp       | later rather than sooner (do we strip out disk support sooner has a GIANT locked CAM driver)   |
| armv6                           | imp/manu  |    |
| i386 kernel | imp | timing? |
| powerpc, powerpcsce kernel| imp | |
| PS3 🎮| imp | nobody uses (we need ps5 port!)|
| powerpc64, powerpc64le (whole powerpc platform) | | https://bugs.freebsd.org/271826 FreeBSD is disastrously slow on PowerMac G5... |
| SoC support review              | imp/manu/mhorne |    |
| ftpd                            | allanjude |    |
| Remove consumers of DES         | des?
| sendmail 📮                       | bapt?     |    |
| bootloader forth support 🔪     | imp/stevek |   |
| warn if booting installer in EFI, but requesting BIOS install | | |
| NIS server components            | ~~des?~~    | Still using so please add to ports (chuck) |
| publicwkey(5)                    | manu | [D30683](https://reviews.freebsd.org/D30683) [D30682](https://reviews.freebsd.org/D30682) |
| targ(4) CAM target driver | imp |  |
| fingerd | ?? | meena would like to volunteer for this |
| 3dfx(4) & `*_isa` | jhb |  |
| syscons(4) (deprecation at least) | emaste / manu |  |
| review ethernet drivers (100mbps, obscure 1/10 gbps) | brooks |  |
| review CAM drivers (pms(4),hpt*, siis, mvs, etc) | imp | |
| ACPI-safe timer | cperciva | [00d061855deb](https://cgit.freebsd.org/src/commit/?id=00d061855deb93df5d709c8a794985ebb55012f8)|
| freebsd-update | cperciva | once pkgbase is ready |
| 32bit platforms (kernels, keep compat32)    | jhb | |
| arm\*soft removal (support for building a full soft system, which is all that remains after I removed the libsoft hack builds and ld.so support) | imp | |
| support for swapping out kernel stacks | markj | [6aa98f78cc6e](https://cgit.freebsd.org/src/commit/?id=6aa98f78cc6e527b801cabddf6881ab5c9256934) |
| support for !SMP amd64 kernels | markj | consensus? +1 +1 |

# Legend
| Symbol | Meaning |
| -- | -- |
| ?? | Status is in question |
| !! | Needs a new owner |