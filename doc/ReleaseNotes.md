<a href="https://omniosce.org">
<img src="https://omniosce.org/OmniOSce_logo.svg" height="128">
</a>

# Release Notes for OmniOSce v11 r151034

## r151034ax (2021-04-14)
Weekly release for w/c 12th of April 2021.
> This update requires a reboot

# Changes

* `curl` updated to 7.76.1

* Changing the encryption key on a ZFS dataset with clones did not update
  the clones themselves, rendering them inaccessible.

<br>

---

## r151034av (2021-04-01)
Weekly release for w/c 29th of March 2021.
> This is a non-reboot update

# Security Fixes

* `curl` updated to 7.76.0, fixing
  [CVE-2021-22876](https://curl.se/docs/CVE-2021-22876.html),
  [CVE-2021-22890](https://curl.se/docs/CVE-2021-22890.html)

<br>

---

## r151034au (2021-03-25)
Weekly release for w/c 22th of March 2021.
> This is a non-reboot update

# Security Fixes

* `openssl` updated to 1.1.1k, fixing
  [CVE-2021-3449](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-3449),
  [CVE-2021-3450](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-3450)

* `openssh` updated to fix
  [CVE-2021-28041](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-28041)

<br>

---

## r151034as (2021-03-10)
Weekly release for w/c 8th of March 2021.
> This is a non-reboot update

# Security Fixes

* `git` has been updated to version 2.26.3, fixing
  [CVE-2021-21300](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-21300).

<br>

---

## r151034ap (2021-02-18)
Weekly release for w/c 15th of February 2021.
> This update requires a reboot

# Security Fixes

* `openssl` updated to 1.1.1j, fixing
  [CVE-2021-23840](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-23840),
  [CVE-2021-23841](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-23841).

* The legacy `openssl` 1.0.2 has also been patched to mitigate the above CVEs.

* All shipped `python` versions have been updated to address
  [CVE-2021-3177](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-3177).

# Other Changes

* Adding a second disk to an Azure instance caused a kernel panic.

<br>

---

## r151034ao (2021-02-11)
Weekly release for w/c 8th of February 2021.
> This is a non-reboot update

# Security Fixes

* `screen` updated to fix
  [CVE-2021-3156](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-3156).

<br>

---

## r151034am (2021-01-25)
Weekly release for w/c 25th of January 2021.
> This update requires a reboot

# Security Fixes

* It was possible for an unprivileged user, including one in a zone, to cause
  the system to panic.

* `sudo` updated to 1.9.5p2, fixing
  [CVE-2021-3156](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-3156).

* `socat` updated to fix a potential heap based buffer overflow.

# Other Changes

* Support for Active-Directory servers which enforce secure RPC
  (due to CVE-2020-1472).

* `gcc` has been updated so that the `-z assert-deflib` linker option works
  correctly for 64-bit objects.

* OpenJDK 8 has been updated to 1.8.282-b08

* ZFS `list -t bookmark` was not working for zvols.

* Add support for the `IA32_FEATURE_CONTROL` MSR in bhyve. This improves
  support for some guest operating systems.

* `pkg apply-hot-fix` could produce error messages during operation.

<br>

---

## r151034af (2020-12-10)
Weekly release for w/c 07th of December 2020.
> This update requires a reboot

# Security Fixes

* `openssl` updated to 1.1.1i, fixing
  [CVE-2020-1971](https://www.openssl.org/news/secadv/20201208.txt)

* `openssl 1.0` updated to fix
  [CVE-2020-1968](https://www.openssl.org/news/secadv/20200909.txt),
  [CVE-2020-1971](https://www.openssl.org/news/secadv/20201208.txt)

* `curl` updated to 7.74.0, fixing
  [CVE-2020-8284](https://curl.se/docs/CVE-2020-8284.html),
  [CVE-2020-8285](https://curl.se/docs/CVE-2020-8285.html),
  [CVE-2020-8286](https://curl.se/docs/CVE-2020-8286.html)

# Bug Fixes

* MacOS Big Sur clients would experience read hangs when accessing OmniOS
  SMB shares.

* In rare cases, a system could crash shortly after boot while maintaining
  ZFS user quota information (particularly if a zfs recv was running at
  the same time).

* The `pkg apply-hot-fix` command, in conjunction with the creation of a new
  boot environment, would sometimes leave extra origins configured in
  non-global zones. This caused problems for subsequent package updates.

* Compiling with `gcc -pg` did not produce a working profiling binary.

# Other Changes

* The Intel CPU microcode update for some Core (Gen. 11) Mobile processors
  has been removed as it was reported to cause problems on some platforms.

<br>

---

## r151034ac (2020-11-17)
Weekly release for w/c 16th of November 2020.
> This update requires a reboot

# Security Fixes

* Updated Intel processor microcode from Intel, fixing several security
  vulnerabilities.

# Other Changes

* `pkg` could backtrace when displaying licence information.

<br>

---

## r151034z (2020-10-26)
Weekly release for w/c 26th of October 2020.
> This is a non-reboot update

# Security Fixes

* OpenJDK 8 updated to 1.8.0.272, fixing
  [multiple CVEs](https://foojay.io/java-8/?quarter=102020&tab=cve&version=openjdk8u272).

<br>

---

## r151034y (2020-10-22)
Weekly release for w/c 19th of October 2020.
> This update requires a reboot

# Security Fixes

* Fix for
  [CVE-2020-27678](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-27678)
  - a pre-auth remote root exploit in PAM.

# Other Changes

* It should be possible to boot from a ZFS pool which has or has previously
  had a log device.

* 8-bit mode clear screen uses the wrong colour.

* System can panic with an error in the IP module.

<br>

---

## r151034w (2020-10-05)
Weekly release for w/c 5th of October 2020.
> This is a non-reboot update

# Other Changes

* Enhancement to `pkg` to allow for more detailed diagnostic messages
  via `-vv` in the event that an upgrade solution can't be found.

<br>

---

## r151034t (2020-09-15)
Weekly release for w/c 14th of September 2020.
> This update requires a reboot if bhyve is installed

# Security Fixes

* It was possible for a bhyve guest running under AMD SVM to execute some
  instructions against host physical memory -
  [CVE-2020-7467](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-7467)

<br>

---

## r151034r (2020-09-01)
Weekly release for w/c 31st of August 2020.
> This update requires a reboot

# Security Fixes

* It was theoretically possible to escape from a zone that has permission
  to create a bhyve instance -
  [CVE-2020-24718](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-24718)
  Note that in OmniOS only _bhyve_-branded zones have access to bhyve and this
  vulnerability does not enable escape from a bhyve virtual machine.

# Other Changes

* Fix for a ZFS-related panic -
  [13034 dnode_sync is careless with range tree](https://www.illumos.org/issues/13034)

* [12755 Double fault when booting under Amazon EC2](https://www.illumos.org/issues/12755)

* Various fixes for the `mlxcx` network driver; illumos issues
  [12980](https://www.illumos.org/issues/12980),
  [12987](https://www.illumos.org/issues/12987) and
  [12988](https://www.illumos.org/issues/12988)

* Better emulation for sendfile() in lx zones. In particular this fixes
  problems experienced with Python 3.8's pip command

* `crontab` has gained a `-u` option

* `/lib/svc/bin/smfcron` is provided to more easily create SMF services that
  add and remove cron jobs

<br>

---

## r151034q (2020-08-24)
Weekly release for w/c 24th of August 2020.
> This is a non-reboot update

# Security Fixes

* `curl` updated fixing
  * [CVE-2020-8231](https://curl.haxx.se/docs/CVE-2020-8231.html).

<br>

---

## r151034o (2020-08-10)
Weekly release for w/c 10th of August 2020.
> This is a non-reboot update

# Security Fixes

* OpenJDK 8 updated to 1.8.0.265, fixing multiple CVEs:
  * [CVE-2020-14556](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-14556)
  * [CVE-2020-14577](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-14577)
  * [CVE-2020-14578](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-14578)
  * [CVE-2020-14579](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-14579)
  * [CVE-2020-14581](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-14581)
  * [CVE-2020-14583](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-14583)
  * [CVE-2020-14593](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-14593)
  * [CVE-2020-14621](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-14621)

* Python 3.7 updated to 3.7.8, including fixes for:
  * [CVE-2019-18348](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-18348)
  * [CVE-2020-14422](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-14422)
  * [CVE-2020-20907](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-20907)

* Python 2.7 updated with fixes for:
  * [CVE-2020-20907](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-20907)
  * [CVE-2020-8492](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-8492)

<br>

---

## r151034n (2020-08-04)
Weekly release for w/c 3rd of August 2020.
> This is a non-reboot update

# Changes

* Update `pkg` to fix bugs with conditional dependency handling.

<br>

---

## r151034m (2020-07-27)
Weekly release for w/c 27th of July 2020.
> This update requires a reboot

# Fixes

* Fix for race in multi-threaded python applications using wrapped TLS sockets
* Update /etc/magic with pattern for Zstandard compressed files
* Fix for a crash in the xnf network driver when running under Xen or AWS

<br>

---

## r151034l (2020-07-20)
Weekly release for w/c 20th of July 2020.
> This update requires a reboot

# Fixes

 * Some 64-bit PCI devices were not programmed correctly
 * The `mlxcx` driver has been updated to fix several problems
 * Panic in `imc` driver on some systems with broken firmware
 * LX: `/proc/<pid>/exe` symlink was not always present
 * LX: Would occasionally see defunct processes with busy parents
 * LX: Improve support for networking setup in Void linux zones
 * loader could not read a ZFS pool which had a removed slog device
 * vioblk devices could hang under memory pressure
 * It was not possible to run bhyve in the global zone under a DEBUG kernel
   (although this is possible for testing, bhyve should always be run within a
    zone for proper protection)

# Other Changes

 * Added a `depend.ooceextra` facet to illumos packages to allow installation
   without reference to the omnios-extra repository
 * Updated curl to 7.71.1
 * Updated OpenJDK8 to 1.8.0\_262
 * Updated rsync to 3.2.2

<br>

---

## r151034i (2020-07-01)
Weekly release for w/c 29th of June 2020.
> This is a non-reboot update

# Security Fixes

* Curl updated fixing
  [CVE-2020-8169](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-8169),
  [CVE-2020-9177](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-9177)

<br>

---

## r151034h (2020-06-22)
Weekly release for w/c 22nd of June 2020.
> This update requires a reboot

# Security Fixes

* Intel microcode updated to 20200616.

# Other changes

* [12444 - Intel v1 chip topo needs rank information](https://www.illumos.org/issues/12444)
* LX: isatty() should return ENOTTY if not a TTY.

<br>

---

## r151034f (2020-06-08)
Weekly release for w/c 8th of June 2020.
> This is a non-reboot update

# Security Fixes

* `perl` updated to 5.30.3 fixing
  [CVE-2020-10543](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-10543),
  [CVE-2020-10878](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-10878)
  and
  [CVE-2020-12723](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-12723).

* `nghttp2` updated to 1.41.0 fixing
  [CVE-2020-11080](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-11080).

<br>

---

## r151034e (2020-06-01)
Weekly release for w/c 01st of June 2020.
> This is a non-reboot update

# Changes

* Fix bug in the `pkgdepend` package dependency generator.
  (Required to consistently build gate after 12708 is integrated)

* It was not always possible to specify cdrom device for KVM-branded zones.

<br>

---

## r151034d (2020-05-25)
Weekly release for w/c 25th of May 2020.
> This update requires a reboot

# Changes

* Update Intel CPU microcode to 20200520

* Update timezone data to 2020a

* The bhyve zone brand now supports `vnc=wait` to pause VM execution until
  a VNC client has connected

* KVM zone shutdown did not work reliably

* The bhyve and kvm zone brands now support multiple cdrom entries. These
  should be configured as properties named `cdrom0`, `cdrom1`, etc.

* The `default-recurse` pkg property was erroneously affecting the
  `pkg install` command; this has been fixed

* `pkg update` with a new boot environment could occasionally report
  _pkg: Unable to clone the current boot environment_

* `onu` to illumos-gate now works with installed zones

* Fix for a kernel panic when running an NFS client within an lx-branded zone

* Fix for regression in ftello64() behaviour

* Fix for (rare) crash in bhyve with some Linux guests

* Fix for potential lz4 compression failure in `vtfontcvt`

* Improve TSO support in vioif driver

<br>

---

Stable Release, 4th of May 2020

`uname -a` shows `omnios-r151034-f57f507df0`

r151034 release repository: https://pkg.omniosce.org/r151034/core

## Upgrade Notes

It is only possible to upgrade to this release from r151030 or r151032. If
starting from an earlier release, upgrade in stages following the guide at
https://omniosce.org/upgrade

## New features since r151032

### System Features

* OmniOS now supports running an NFS server in a native zone (i.e. _ipkg_,
  _lipkg_, _sparse_ or _pkgsrc_ brands). NFS sharing can be enabled by setting
  the `sharenfs` property on a dataset just as in the global zone.

* While it was previously possible to create an SMB share within a zone via
  the `sharemgr` command, it can now be done more easily via the `sharesmb`
  dataset property, as in the global zone (subject to doing the rest of the
  required setup for SMB such as configuring the idmap service).

* Support for overlay networks has been ported from Joyent SmartOS. An overlay
  is effectively an etherstub (virtual switch) that can be distributed across
  hosts. The
  [overlay(5) manual page](https://man.omnios.org/man5/overlay.5.html)
  provides a good overview of this new functionality. The current
  implementation in OmniOS supports sharing an overlay between two hosts
  using the _direct_ plugin and across multiple hosts using statically
  configured rules via the _files_ plugin.

* Improvements to the in-kernel SMB/CIFS support.

* The SMB client has been updated to version 3.02

* Support for SMBIOS 3.3 and decoding of additional information such as
  battery data.

* The OmniOS kernel is now built with mitigations against `swapgs` and `TAA`
  attacks.

* A new AMD temperature sensor driver is available.

* A new `fdinfo` directory is available under `/proc` for each process. This
  directory contains an entry for each of the process' open files and the
  entry contains information about the file. Refer to the
  [proc(4) manual page](https://man.omnios.org/man4/proc.4.html#fdinfo) for
  more details on the file format.

* LDAP group integration has been improved to support more LDAP schemas.

* The `gettimeofday()` function call performance has been significantly
  improved.

### Commands and Command Options

* `ps ww` has been updated to fix a regression introduced in r151032 where
  output would be truncated. The root user can now see all process arguments;
  non-root users are still restricted to seeing the first 4096 characters.

* A new `resize` command is available to set environment and terminal settings
  to the current window size (for supported terminals).

* The `watch` command is now available to monitor the output of a command
  over time.

* The `ssh-copy-id` command is provided to easily transfer a public ssh key
  to a remote system.

* `rdmsr` allows reading of a value from x86 model-specific registers.

* `pfiles` now shows the filesystem endpoints for door servers.

* `ptree` has been extended to support showing line-drawing characters and to
  better wrap output.

* `find -path` now operates correctly for paths starting with a "." character.

* A new `demangle` command has been added which can be used to decode a C++ or
  Rust encoded symbol name.

### Bhyve

* Additional bhyve firmware based on a newer version of the reference UEFI
  implementation is now available. This firmware supports UEFI only and does
  not currently support PCI pass-through. To switch to it, set the `bootrom`
  attribute of a bhyve zone to `BHYVE_RELEASE-2.70`.

* It is now possible to set a password for the bhyve VNC server.

* bhyve vioblk devices now support TRIM, although note that illumos guests
  cannot yet use this feature.

* The `bhhwcompat` command has been removed in this release since it no longer
  provides any useful diagnostics.

* In this release, bhyve has acquired multiple additional updates and fixes
  from upstream Joyent and FreeBSD.

### Zones

* On-demand VNICs are now supported for all zone brands via the `global-nic`
  zone configuration attribute. Previously `lx`, `kvm` and `bhyve` zones would 
  ignore this even if set.

### LX zones

* Prior to this release, executing a shared library in an LX zone could cause
  it to crash; this has been resolved.

* It is now possible to disable IPv6 within an LX zone by setting the
  `ipv6` attribute to the string `false`.

* Improved networking support within Ubuntu 18.04 LX zones.

* Support for running Void Linux images.

* The _lx(5)_ manual page has been updated to include details on the additional
  zone configuration settings available for LX zones.

* `MemAvailable` has been added to `/proc/meminfo`. In OmniOS this is always
  the same as `MemFree` and is provided for applications that expect to see
  it there.

### ZFS

* ZFS can now automatically recover from more situations when the root pool
  devices have moved.

* Support for ZFS trim - see the output of `zpool status -t` for details on
  whether it is supported for a particular pool.

* `zpool iostat` and `zpool status` improvements.

* Improved zpool import speed.

* Support for Direct I/O on ZFS filesystems.

### Package Management

* The packaging tools have been updated to run using Python 3.7 and the JSON
  parsing backend has been replaced by `rapidjson`. As a result the tools are
  faster and use significantly less memory.

### Hardware Support

* Support for Intel ixgbe X553.

* Support for cxgbe T5/T6 parts.

* Updated cxgbe firmware.

* Support for Mellanox ConnectX-4/5/6 NICs.

* Support for Intel I219 v10-v15.

* Support for additional Emulex fibre-channel cards.

### Loader

* New menu option to toggle the graphical console state before boot
 (only for non-UEFI boot).

* Improved menu option for selecting the desired KMDB behaviour before boot.

### Developer Features

* The `developer/gcc9` package is now available, supporting compiling
  objective-C and Go programs alongside C, C++ and Fortran.

* The default OmniOS userland compiler is now gcc 9 and produces 64-bit
  objects by default.

* It is possible to override the version lock for more system packages via
  IPS facets which allows administrators to downgrade these packages more
  easily if it becomes necessary.

* Additional commands have been added to mdb - `::refstr`, `::ps -s`.

* Slave PTYs now operate in a less standards-compliant but more commonly
  expected way. This resolves problems with third party software that does
  not anticipate the standards-compliant mode of operation.

* Perl is now shipped 64-bit only.
  Note that in order to continue building illumos-gate on OmniOS you must add
  `export BUILDPERL32='#'` to your .env file.

* The default Python 3 version is now 3.7 and all system packages have been
  updated to use this new version. Python 3.5 and all related modules have
  been deprecated and removed.

* `open(2)` now supports the `O_DIRECTORY` flag.

* The `fmemopen(3C)` and `open_memstream(3C)` functions are now available.

* Extensions to the Device Driver Interface (DDI) to improve the DMA cookie
  APIs.

* KCF and PKCS#11 now support SHA512\_224 and SHA512\_256.

### Deprecated features

* The Python `simplejson` module has been removed in this release. In its place
  there is a new `rapidjson` module which is both faster and less memory
  hungry.

* The `bhhwcompat` command has been removed.

* Python 2 is now end-of-life and will not receive any further updates. The
  `python-27` package is still available for backwards compatibility but will
  be maintained only on a best-efforts basis.

* OpenSSL 1.0.x is deprecated and reached end-of-support at the end of 2019.
  OmniOS has completely transitioned to OpenSSL 1.1.1 but retains the OpenSSL
  1.0.2 libraries for backwards compatibility. The 1.0.2 libraries are
  maintained solely on a best-efforts basis.

### Package changes ([+] Added, [-] Removed, [\*] Changed)

| Package | Old Version | New Version |
| :------ | :---------- | :---------- |
| compress/xz | 5.2.4 | 5.2.5
| ~~consolidation/sunpro/sunpro-incorporation~~ | 0.5.11 | _Removed_
| data/iso-codes | 4.3 | 4.4
| database/sqlite-3 | 3.29.0 | 3.31.1
| developer/build/automake | 1.16.1 | 1.16.2
| developer/build/gnu-make | 4.2.1 | 4.3
| developer/gcc7 | 7.4.0 | 7.5.0
| developer/gcc8 | 8.3.0 | 8.4.0
| **developer/gcc9** | _New_ | 9.3.0
| developer/gnu-binutils | 2.32 | 2.34
| developer/java/openjdk8 | 1.8.0.232.9 | 1.8.0.252.9
| developer/parser/bison | 3.4.2 | 3.5.3
| developer/versioning/git | 2.23.3 | 2.26.2
| developer/versioning/mercurial | 5.1.1 | 5.3.1
| **driver/cpu/mc** | _New_ | 0.5.11
| **driver/network/mlxcx** | _New_ | 0.5.11
| editor/vim | 8.1.1909 | 8.2.422
| file/gnu-coreutils | 8.31 | 8.32
| library/c++/sigcpp | 3.0.0 | 3.0.3
| library/expat | 2.2.8 | 2.2.9
| library/glib2 | 2.62.0 | 2.64.1
| library/gmp | 6.1.2 | 6.2.0
| library/libffi | 3.2.1 | 3.3
| library/libxml2 | 2.9.9 | 2.9.10
| library/ncurses | 6.1.20190921 | 6.2
| library/nghttp2 | 1.39.2 | 1.40.0
| library/nspr | 4.22 | 4.25
| library/nspr/header-nspr | 4.22 | 4.25
| library/pcre | 8.43 | 8.44
| library/pcre2 | 10.33 | 10.34
| library/perl-5/xml-parser | 2.44 | 2.46
| library/python-2/setuptools-27 | 41.2.0 | 46.1.3
| ~~library/python-3/asn1crypto-35~~ | 0.24.0 | _Removed_
| **library/python-3/asn1crypto-37** | _New_ | 1.3.0
| ~~library/python-3/attrs-35~~ | 19.1.0 | _Removed_
| **library/python-3/attrs-37** | _New_ | 19.3.0
| ~~library/python-3/cffi-35~~ | 1.12.3 | _Removed_
| **library/python-3/cffi-37** | _New_ | 1.14.0
| ~~library/python-3/cheroot-35~~ | 6.5.8 | _Removed_
| **library/python-3/cheroot-37** | _New_ | 8.3.0
| ~~library/python-3/cherrypy-35~~ | 18.2.0 | _Removed_
| **library/python-3/cherrypy-37** | _New_ | 18.5.0
| ~~library/python-3/contextlib2-35~~ | 0.6.0 | _Removed_
| ~~library/python-3/coverage-35~~ | 4.5.4 | _Removed_
| **library/python-3/coverage-37** | _New_ | 5.0.4
| ~~library/python-3/cryptography-35~~ | 2.7 | _Removed_
| **library/python-3/cryptography-37** | _New_ | 2.8
| ~~library/python-3/functools_lru_cache-35~~ | 1.5 | _Removed_
| ~~library/python-3/idna-35~~ | 2.8 | _Removed_
| **library/python-3/idna-37** | _New_ | 2.9
| **library/python-3/importlib-metadata-37** | _New_ | 1.5.2
| **library/python-3/jaraco-37** | _New_ | 1.0.0
| ~~library/python-3/jaraco.functools-35~~ | 1.20 | _Removed_
| **library/python-3/js-regex-37** | _New_ | 1.0.1
| ~~library/python-3/jsonrpclib-35~~ | 0.4.0 | _Removed_
| **library/python-3/jsonrpclib-37** | _New_ | 0.4.0
| ~~library/python-3/jsonschema-35~~ | 3.0.2 | _Removed_
| **library/python-3/jsonschema-37** | _New_ | 3.2.0
| ~~library/python-3/mako-35~~ | 1.1.0 | _Removed_
| **library/python-3/mako-37** | _New_ | 1.1.2
| ~~library/python-3/meson-35~~ | 0.51.2 | _Removed_
| **library/python-3/meson-37** | _New_ | 0.53.2
| ~~library/python-3/more-itertools-35~~ | 7.2.0 | _Removed_
| **library/python-3/more-itertools-37** | _New_ | 8.2.0
| ~~library/python-3/pep8-35~~ | 1.7.1 | _Removed_
| ~~library/python-3/ply-35~~ | 3.11 | _Removed_
| **library/python-3/ply-37** | _New_ | 3.11
| ~~library/python-3/portend-35~~ | 2.5 | _Removed_
| **library/python-3/portend-37** | _New_ | 2.6
| ~~library/python-3/prettytable-35~~ | 0.7.2 | _Removed_
| **library/python-3/prettytable-37** | _New_ | 0.7.2
| ~~library/python-3/pybonjour-35~~ | 1.1.1 | _Removed_
| **library/python-3/pybonjour-37** | _New_ | 1.1.1
| **library/python-3/pycodestyle-37** | _New_ | 2.5.0
| ~~library/python-3/pycparser-35~~ | 2.19 | _Removed_
| **library/python-3/pycparser-37** | _New_ | 2.20
| ~~library/python-3/pycurl-35~~ | 7.43.0.3 | _Removed_
| **library/python-3/pycurl-37** | _New_ | 7.43.0.5
| ~~library/python-3/pyopenssl-35~~ | 19.0.0 | _Removed_
| **library/python-3/pyopenssl-37** | _New_ | 19.1.0
| ~~library/python-3/pyrsistent-35~~ | 0.15.4 | _Removed_
| **library/python-3/pyrsistent-37** | _New_ | 0.16.0
| ~~library/python-3/pytz-35~~ | 2019.2 | _Removed_
| **library/python-3/pytz-37** | _New_ | 2019.3
| **library/python-3/rapidjson-37** | _New_ | 0.9.1
| ~~library/python-3/setuptools-35~~ | 41.2.0 | _Removed_
| library/python-3/setuptools-37 | 41.2.0 | 46.1.3
| ~~library/python-3/simplejson-35~~ | 3.16.0 | _Removed_
| ~~library/python-3/six-35~~ | 1.12.0 | _Removed_
| **library/python-3/six-37** | _New_ | 1.14.0
| ~~library/python-3/tempora-35~~ | 1.14.1 | _Removed_
| **library/python-3/tempora-37** | _New_ | 3.0.0
| ~~library/python-3/zc.lockfile-35~~ | 2.0 | _Removed_
| **library/python-3/zc.lockfile-37** | _New_ | 2.0
| **library/python-3/zipp-37** | _New_ | 3.1.0
| network/dns/bind | 9.11.11 | 9.11.18
| network/openssh | 8.0.1 | 8.2.1
| network/openssh-server | 8.0.1 | 8.2.1
| network/service/isc-dhcp | 4.4.1 | 4.4.2
| network/socat | 1.7.3.3 | 1.7.3.4
| runtime/java/openjdk8 | 1.8.0.232.9 | 1.8.0.252.9
| runtime/perl | 5.30.0 | 5.30.2
| ~~runtime/perl-64~~ | 5.30.0 | _Removed_
| ~~runtime/perl/manual~~ | 5.30.0 | _Removed_
| ~~runtime/python-35~~ | 3.5.8 | _Removed_
| runtime/python-37 | 3.7.4 | 3.7.7
| security/sudo | 1.8.28.1 | 1.8.31.1
| service/network/ntp | 4.2.8.13 | 4.2.8.14
| service/network/ntpsec | 1.1.7 | 1.1.8
| service/network/smtp/dma | 0.12 | 0.13
| shell/bash | 5.0.11 | 5.0.16
| shell/tcsh | 6.21.0 | 6.22.2
| shell/zsh | 5.7.1 | 5.8
| system/cpuid | 1.7.3 | 1.7.4
| system/data/hardware-registry | 0.5.11 | 2020.2.22
| system/library/g++-runtime | 8 | 9
| system/library/gcc-runtime | 8 | 9
| **system/library/gccgo-runtime** | _New_ | 9
| system/library/gfortran-runtime | 8 | 9
| **system/library/gobjc-runtime** | _New_ | 9
| system/library/mozilla-nss | 3.46 | 3.51
| system/library/mozilla-nss/header-nss | 3.46 | 3.51
| system/library/pcap | 1.9.0 | 1.9.1
| ~~system/library/python/libbe-35~~ | 0.5.11 | _Removed_
| **system/library/python/libbe-37** | _New_ | 0.5.11
| ~~system/library/python/solaris-35~~ | 0.5.11 | _Removed_
| **system/library/python/solaris-37** | _New_ | 0.5.11
| ~~system/library/python/zfs-35~~ | 0.5.11 | _Removed_
| **system/library/python/zfs-37** | _New_ | 0.5.11
| **system/microcode/amd** | _New_ | 201203
| **system/microcode/intel** | _New_ | 20191115
| **system/network/overlay** | _New_ | 0.5.11
| system/pciutils | 3.6.2 | 3.6.4
| system/pciutils/pci.ids | 2.2.20190911 | 2.2.20200222
| system/test/fio | 3.16 | 3.19
| system/virtualization/azure-agent | 2.2.42 | 2.2.46
| system/virtualization/open-vm-tools | 10.3.10 | 11.0.5
| **system/watch** | _New_ | 3.3.16
| **terminal/resize** | _New_ | 352
| terminal/screen | 4.6.2 | 4.8.0
| terminal/tmux | 2.9.1 | 3.0
| text/gnu-gettext | 0.20.1 | 0.20.2
| text/gnu-grep | 3.3 | 3.4
| text/gnu-sed | 4.7 | 4.8
| web/curl | 7.66.0 | 7.69.1

