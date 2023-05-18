FreeBSD 15.0 Planning
===
 
# :heavy_check_mark: Completed

Things that have been committed to the tree.

| Thing                     | Owner    | Committed / Review / Patch |
| --                        | --       | -- |


# :airplane: Have

Things that already exist out of tree and can be upstreamed in the next 2 years / before the next release (perhaps needing work to get to an upstreamable state)

| Thing                     | Owner    | Committed / Review / Patch |
| --                        | --       | -- |
| kboot support for amd64    | imp    | |
| NVMe-oF/TCP            | jhb | |
| copy_file_range() in mv and install | pjd | |
| better copy_file_range() fallback/wrapper | pjd | |
| arm64 Branch Target Identification | andrew   |    |
| arm64 SVE                 | andrew   |    |
| amd64/arm64 rescue kernel | markj / Klara | |
| arm64 bhyve             | andrew | |
| iovec wrappers         | brooks | |
| single step AMD CPUs in bhyve | jhb Bojan | |
| Hardware watchpoints in bhyve guests | jhb Bojan | |
| DDB pretty-print with CTF | jhb Bojan | 
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
| Cross kldxref                   | brooks / jhb | (kevans has a kind of hacky prototype or two) |
| merge devmatch and devd (lib-ification) | imp | |
| scheduler and VFS documentation coverage | mhorne | |
| reduce the GIANT hacks | jhb imp | |
|Better i18n support for vt(4) (CJK fonts, unicode fonts display (i.e., emoji), input method)|fanchung| Have a [IME PoC](https://wiki.freebsd.org/SummerOfCode2021Projects/InputMethodInFreeBSDVirtualTerminal) in GSoC'21 | 
| tarfs as root                 | imp | |
| Support for rust in the kernel | brooks | |
| Support for rust in userland | brooks | |
| netlink for ZFS (zfsd/zed) | allanjude | |
| netlink to replace devd socket | ?? | |


# 🗑️ Axe Candidates 🪓

Things we might like to deprecate.  Further discussion may be required to reach consensus.

| Thing                           | Owner     | Committed / Review / Patch |
| --                              | --        | -- |
| Firewire:fire:                  | imp       |    |
| armv6                           | imp/manu  |    |
| SoC support review              | imp/manu/mhorne |    |
| ftpd                            | allanjude |    |
| Remove consumers of DES         | des?
| sendmail                        | bapt?     |    |
| bootloader forth support 🔪     | imp/stevek |   |
| NIS server components            | des?    | |
| publicwkey(5)                    | manu | [D30683](https://reviews.freebsd.org/D30683) [D30682](https://reviews.freebsd.org/D30682) |
| targ(4) CAM target driver | imp |  |
| fingerd | ?? |  |
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