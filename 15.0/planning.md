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


# :airplane: Have

Things that already exist out of tree and can be upstreamed in the next 2 years / before the next release (perhaps needing work to get to an upstreamable state)

| Thing                     | Owner    | Committed / Review / Patch |
| --                        | --       | -- |
| kboot support for amd64    | imp    | |
| NVMe-oF/TCP            | jhb | [D44731](https://reviews.freebsd.org/D44731) |
| copy_file_range() in mv and install | pjd | |
| better copy_file_range() fallback/wrapper | pjd | |
| arm64 SVE                 | andrew   |    |
| amd64/arm64 rescue kernel | markj / Klara | |
| iovec wrappers         | brooks | |
| Hardware watchpoints in bhyve guests | jhb Bojan | |
| Integrate loader command line editing from my GSoC student's code | imp | Needs assistance |
| Inline function tracing with dtrace | markj Christos | |
| GSoC: squashfs                       | chuck | |



# 💸 Need

Things that someone needs in the next two years to support a product or service

| Thing                  | Owner     | Committed / Review / Patch / Status |
| --                     | --        | -- |
| new ELF kernel dump format         | jhb markj | |
| finish pkgbase                     | emaste | |
| Poudriere support for toolchain-less jails | allanjude brd | |
| External toolchain support          | brooks | |
| Pre-commit CI src, doc                  | lwhsu imp bofh | |
| Pre-commit CI ports                | lwhsu will check with bapt and decke | |
| Local & cloud developer CI                 | bofh lwhsu | |
| Other CI Improvements                    | lwhsu | |
| Universal Flash Storage driver | loos | Needed for some embedded deploys, but more universal in the future. Coming to Intel platforms soon. |

# 🥺 Want

Things that would be nice to have but aren't critical

| Thing                           | Owner     | Committed / Review / Patch / Status |
| --                              | --        | -- |
| TPM support (GELI, ZFS)         | allanjude | -- |
| smbfs replacement (v2 or better)| emaste jhixson | -- |
| 9pfs client                     | bkumara, khng / Juniper        | -- |
| overlayfs                        | thj / Klara | |
| Updates to syscall table generation in Lua (libification of makesyscalls.lua) | imp | |
| Streamlined installer (single disk, better defaults, i.e. mash enter until done)           | emaste brd | |
| per-file nullfs                 | dfr | |
| more container support         | emaste | co-op student |
| MINIMAL kernel                  | imp  | |
| Boot loader support for devmatch | imp manu | |
| rewrite config(8) (in lua?)      | imp kevans | |
| merge devmatch and devd (lib-ification) | imp | meena would like to help with this |
| scheduler and VFS documentation coverage | mhorne | |
| reduce the GIANT hacks | jhb imp | |
|Better i18n support for vt(4) (CJK fonts, unicode fonts display (i.e., emoji), input method)|fanchung| Have a [IME PoC](https://wiki.freebsd.org/SummerOfCode2021Projects/InputMethodInFreeBSDVirtualTerminal) in GSoC'21 | 
| tarfs as root                 | imp | |
| Support for rust in the kernel | brooks | |
| Support for rust in userland | brooks | |
| netlink for ZFS (zfsd/zed) | allanjude | |
| netlink to replace devd socket | bapt | has Kernel part |
| UCLification of login. conf | meena | allanjude has the beginnings of a patch: [D25365](https://reviews.freebsd.org/D25365) |
| lixo for remaining network tools | meena | |
| hierarchical dynamic login classes | ngor, meena | |


# 🗑️ Axe Candidates 🪓

Things we might like to deprecate.  Further discussion may be required to reach consensus.

| Thing                           | Owner     | Committed / Review / Patch |
| --                              | --        | -- |
| Firewire 🔥                     | imp       |    |
| armv6                           | imp/manu  |    |
| SoC support review              | imp/manu/mhorne |    |
| ftpd                            | allanjude |    |
| Remove consumers of DES         | des?
| sendmail                        | bapt?     |    |
| bootloader forth support 🔪     | imp/stevek |   |
| NIS server components            | des?    | |
| publicwkey(5)                    | manu | [D30683](https://reviews.freebsd.org/D30683) [D30682](https://reviews.freebsd.org/D30682) |
| targ(4) CAM target driver | imp |  |
| fingerd | ?? | meena would like to volunteer for this |
| 3dfx(4) & `*_isa` | jhb |  |
| syscons(4) (deprecation at least) | emaste / manu |  |
| review ethernet drivers (100mbps, obscure 1/10 gbps) | brooks |  |
| review CAM drivers (pms(4) etc) | imp | |
| ACPI-safe timer | cperciva | |
| freebsd-update | cperciva | once pkgbase is ready |
| 32bit platforms (kernels, keep compat32)    | jhb | |
| arm\*soft removal (support for building a full soft system, which is all that remains after I removed the libsoft hack builds and ld.so support) | imp | |

# Legend
| Symbol | Meaning |
| -- | -- |
| ?? | Status is in question |
| !! | Needs a new owner |