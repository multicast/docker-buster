# stretch

![Pulls](https://img.shields.io/docker/pulls/mkovac/stretch.svg)
![Stars](https://img.shields.io/docker/stars/mkovac/stretch.svg)

The [Debian](https://debian.org/) [Stretch](https://wiki.debian.org/DebianStretch)
[container image](https://hub.docker.com/r/mkovac/stretch/) with few handy
utilities, utf8 locales...

This image is built daily and in case of any security update, the list of
packages is updated, commited and this triggers update of docker-hub image
and all dependant images.

## Quick Usage

Run prebuilt:

    $ docker run --rm -ti mkovac/stretch bash

Or you can clone & build, run `bash` to explore:

    $ git clone https://github.com/multicast/docker-stretch
    $ cd docker-stretch
    $ docker build -t stretch .
    $ docker run --rm -ti stretch bash

Since the image is intended to be used as base image, I suppose more common usage
would be in your own `Dockerfile` in the form:

    FROM mkovac/stretch:latest
    ...

## Build-time options

You can `export` environment variables found in the following list:

  * `ftp_proxy`
  * `http_proxy`
  * `https_proxy`

The values for these variables will not end up in the resulting image.

## Run-time options

You can define environment variables via `--env` argument found in the following list:

  * `ftp_proxy`
  * `http_proxy`
  * `https_proxy`
  * `BASE_DEBUG`
      * zero to higher numbers - to get more and more verbose
  * `BASE_NOEXIT`
      * set to 1 not to exit on startup errors

# Packages

    Desired=Unknown/Install/Remove/Purge/Hold
    | Status=Not/Inst/Conf-files/Unpacked/halF-conf/Half-inst/trig-aWait/Trig-pend
    |/ Err?=(none)/Reinst-required (Status,Err: uppercase=bad)
    ||/ Name                       Version                        Architecture Description
    +++-==========================-==============================-============-===============================================================================
    ii  adduser                    3.115                          all          add and remove users and groups
    ii  apt                        1.4.9                          amd64        commandline package manager
    ii  apt-utils                  1.4.9                          amd64        package management related utility programs
    ii  base-files                 9.9+deb9u9                     amd64        Debian base system miscellaneous files
    ii  base-passwd                3.5.43                         amd64        Debian base system master password and group files
    ii  bash                       4.4-5                          amd64        GNU Bourne Again SHell
    ii  bsdutils                   1:2.29.2-1+deb9u1              amd64        basic utilities from 4.4BSD-Lite
    ii  ca-certificates            20161130+nmu1+deb9u1           all          Common CA certificates
    ii  coreutils                  8.26-3                         amd64        GNU core utilities
    ii  curl                       7.52.1-5+deb9u9                amd64        command line tool for transferring data with URL syntax
    ii  dash                       0.5.8-2.4                      amd64        POSIX-compliant shell
    ii  debconf                    1.5.61                         all          Debian configuration management system
    ii  debian-archive-keyring     2017.5+deb9u1                  all          GnuPG archive keys of the Debian archive
    ii  debianutils                4.8.1.1                        amd64        Miscellaneous utilities specific to Debian
    ii  di                         4.34-2+b1                      amd64        advanced df like disk information utility
    ii  diffutils                  1:3.5-3                        amd64        File comparison utilities
    ii  dpkg                       1.18.25                        amd64        Debian package management system
    ii  e2fslibs:amd64             1.43.4-2                       amd64        ext2/ext3/ext4 file system libraries
    ii  e2fsprogs                  1.43.4-2                       amd64        ext2/ext3/ext4 file system utilities
    ii  etckeeper                  1.18.5-1                       all          store /etc in git, mercurial, bzr or darcs
    ii  findutils                  4.6.0+git+20161106-2           amd64        utilities for finding files--find, xargs
    ii  gcc-6-base:amd64           6.3.0-18+deb9u1                amd64        GCC, the GNU Compiler Collection (base package)
    ii  git                        1:2.11.0-3+deb9u4              amd64        fast, scalable, distributed revision control system
    ii  git-man                    1:2.11.0-3+deb9u4              all          fast, scalable, distributed revision control system (manual pages)
    ii  gpgv                       2.1.18-8~deb9u4                amd64        GNU privacy guard - signature verification tool
    ii  grep                       2.27-2                         amd64        GNU grep, egrep and fgrep
    ii  gzip                       1.6-5+b1                       amd64        GNU compression utilities
    ii  hostname                   3.18+b1                        amd64        utility to set/show the host name or domain name
    ii  init-system-helpers        1.48                           all          helper tools for all init systems
    ii  joe                        4.4-1                          amd64        user friendly full screen text editor
    ii  less                       481-2.1                        amd64        pager program similar to more
    ii  libacl1:amd64              2.2.52-3+b1                    amd64        Access control list shared library
    ii  libapt-inst2.0:amd64       1.4.9                          amd64        deb package format runtime library
    ii  libapt-pkg5.0:amd64        1.4.9                          amd64        package management runtime library
    ii  libattr1:amd64             1:2.4.47-2+b2                  amd64        Extended attribute shared library
    ii  libaudit-common            1:2.6.7-2                      all          Dynamic library for security auditing - common files
    ii  libaudit1:amd64            1:2.6.7-2                      amd64        Dynamic library for security auditing
    ii  libblkid1:amd64            2.29.2-1+deb9u1                amd64        block device ID library
    ii  libbz2-1.0:amd64           1.0.6-8.1                      amd64        high-quality block-sorting file compressor library - runtime
    ii  libc-bin                   2.24-11+deb9u4                 amd64        GNU C Library: Binaries
    ii  libc-l10n                  2.24-11+deb9u4                 all          GNU C Library: localization files
    ii  libc6:amd64                2.24-11+deb9u4                 amd64        GNU C Library: Shared libraries
    ii  libcap-ng0:amd64           0.7.7-3+b1                     amd64        An alternate POSIX capabilities library
    ii  libcomerr2:amd64           1.43.4-2                       amd64        common error description library
    ii  libcurl3:amd64             7.52.1-5+deb9u9                amd64        easy-to-use client-side URL transfer library (OpenSSL flavour)
    ii  libcurl3-gnutls:amd64      7.52.1-5+deb9u9                amd64        easy-to-use client-side URL transfer library (GnuTLS flavour)
    ii  libdb5.3:amd64             5.3.28-12+deb9u1               amd64        Berkeley v5.3 Database Libraries [runtime]
    ii  libdebconfclient0:amd64    0.227                          amd64        Debian Configuration Management System (C-implementation library)
    ii  liberror-perl              0.17024-1                      all          Perl module for error/exception handling in an OO-ish way
    ii  libexpat1:amd64            2.2.0-2+deb9u2                 amd64        XML parsing C library - runtime library
    ii  libfdisk1:amd64            2.29.2-1+deb9u1                amd64        fdisk partitioning library
    ii  libffi6:amd64              3.2.1-6                        amd64        Foreign Function Interface library runtime
    ii  libgcc1:amd64              1:6.3.0-18+deb9u1              amd64        GCC support library
    ii  libgcrypt20:amd64          1.7.6-2+deb9u3                 amd64        LGPL Crypto library - runtime library
    ii  libgdbm3:amd64             1.8.3-14                       amd64        GNU dbm database routines (runtime version)
    ii  libgmp10:amd64             2:6.1.2+dfsg-1                 amd64        Multiprecision arithmetic library
    ii  libgnutls30:amd64          3.5.8-5+deb9u4                 amd64        GNU TLS library - main runtime library
    ii  libgpg-error0:amd64        1.26-2                         amd64        library for common error values and messages in GnuPG components
    ii  libgssapi-krb5-2:amd64     1.15-1+deb9u1                  amd64        MIT Kerberos runtime libraries - krb5 GSS-API Mechanism
    ii  libhogweed4:amd64          3.3-1+b2                       amd64        low level cryptographic library (public-key cryptos)
    ii  libidn11:amd64             1.33-1                         amd64        GNU Libidn library, implementation of IETF IDN specifications
    ii  libidn2-0:amd64            0.16-1+deb9u1                  amd64        Internationalized domain names (IDNA2008) library
    ii  libk5crypto3:amd64         1.15-1+deb9u1                  amd64        MIT Kerberos runtime libraries - Crypto Library
    ii  libkeyutils1:amd64         1.5.9-9                        amd64        Linux Key Management Utilities (library)
    ii  libkrb5-3:amd64            1.15-1+deb9u1                  amd64        MIT Kerberos runtime libraries
    ii  libkrb5support0:amd64      1.15-1+deb9u1                  amd64        MIT Kerberos runtime libraries - Support library
    ii  libldap-2.4-2:amd64        2.4.44+dfsg-5+deb9u2           amd64        OpenLDAP libraries
    ii  libldap-common             2.4.44+dfsg-5+deb9u2           all          OpenLDAP common files for libraries
    ii  liblz4-1:amd64             0.0~r131-2+b1                  amd64        Fast LZ compression algorithm library - runtime
    ii  liblzma5:amd64             5.2.2-1.2+b1                   amd64        XZ-format compression library
    ii  libmount1:amd64            2.29.2-1+deb9u1                amd64        device mounting library
    ii  libncurses5:amd64          6.0+20161126-1+deb9u2          amd64        shared libraries for terminal handling
    ii  libncursesw5:amd64         6.0+20161126-1+deb9u2          amd64        shared libraries for terminal handling (wide character support)
    ii  libnettle6:amd64           3.3-1+b2                       amd64        low level cryptographic library (symmetric and one-way cryptos)
    ii  libnewt0.52:amd64          0.52.19-1+b1                   amd64        Not Erik's Windowing Toolkit - text mode windowing with slang
    ii  libnghttp2-14:amd64        1.18.1-1                       amd64        library implementing HTTP/2 protocol (shared library)
    ii  libp11-kit0:amd64          0.23.3-2                       amd64        library for loading and coordinating access to PKCS#11 modules - runtime
    ii  libpam-modules:amd64       1.1.8-3.6                      amd64        Pluggable Authentication Modules for PAM
    ii  libpam-modules-bin         1.1.8-3.6                      amd64        Pluggable Authentication Modules for PAM - helper binaries
    ii  libpam-runtime             1.1.8-3.6                      all          Runtime support for the PAM library
    ii  libpam0g:amd64             1.1.8-3.6                      amd64        Pluggable Authentication Modules library
    ii  libpcre3:amd64             2:8.39-3                       amd64        Old Perl 5 Compatible Regular Expression Library - runtime files
    ii  libperl5.24:amd64          5.24.1-3+deb9u5                amd64        shared Perl library
    ii  libpopt0:amd64             1.16-10+b2                     amd64        lib for parsing cmdline parameters
    ii  libprocps6:amd64           2:3.3.12-3+deb9u1              amd64        library for accessing process information from /proc
    ii  libpsl5:amd64              0.17.0-3                       amd64        Library for Public Suffix List (shared libraries)
    ii  libpython-stdlib:amd64     2.7.13-2                       amd64        interactive high-level object-oriented language (default python version)
    ii  libpython2.7-minimal:amd64 2.7.13-2+deb9u3                amd64        Minimal subset of the Python language (version 2.7)
    ii  libpython2.7-stdlib:amd64  2.7.13-2+deb9u3                amd64        Interactive high-level object-oriented language (standard library, version 2.7)
    ii  libreadline7:amd64         7.0-3                          amd64        GNU readline and history libraries, run-time libraries
    ii  librtmp1:amd64             2.4+20151223.gitfa8646d.1-1+b1 amd64        toolkit for RTMP streams (shared library)
    ii  libsasl2-2:amd64           2.1.27~101-g0780600+dfsg-3     amd64        Cyrus SASL - authentication abstraction library
    ii  libsasl2-modules-db:amd64  2.1.27~101-g0780600+dfsg-3     amd64        Cyrus SASL - pluggable authentication modules (DB)
    ii  libselinux1:amd64          2.6-3+b3                       amd64        SELinux runtime shared libraries
    ii  libsemanage-common         2.6-2                          all          Common files for SELinux policy management libraries
    ii  libsemanage1:amd64         2.6-2                          amd64        SELinux policy management library
    ii  libsepol1:amd64            2.6-2                          amd64        SELinux library for manipulating binary security policies
    ii  libslang2:amd64            2.3.1-5                        amd64        S-Lang programming library - runtime version
    ii  libsmartcols1:amd64        2.29.2-1+deb9u1                amd64        smart column output alignment library
    ii  libsqlite3-0:amd64         3.16.2-5+deb9u1                amd64        SQLite 3 shared library
    ii  libss2:amd64               1.43.4-2                       amd64        command-line interface parsing library
    ii  libssh2-1:amd64            1.7.0-1+deb9u1                 amd64        SSH2 client-side library
    ii  libssl1.0.2:amd64          1.0.2s-1~deb9u1                amd64        Secure Sockets Layer toolkit - shared libraries
    ii  libssl1.1:amd64            1.1.0k-1~deb9u1                amd64        Secure Sockets Layer toolkit - shared libraries
    ii  libstdc++6:amd64           6.3.0-18+deb9u1                amd64        GNU Standard C++ Library v3
    ii  libsystemd0:amd64          232-25+deb9u11                 amd64        systemd utility library
    ii  libtasn1-6:amd64           4.10-1.1+deb9u1                amd64        Manage ASN.1 structures (runtime)
    ii  libtinfo5:amd64            6.0+20161126-1+deb9u2          amd64        shared low-level terminfo library for terminal handling
    ii  libudev1:amd64             232-25+deb9u11                 amd64        libudev shared library
    ii  libunistring0:amd64        0.9.6+really0.9.3-0.1          amd64        Unicode string library for C
    ii  libustr-1.0-1:amd64        1.0.4-6                        amd64        Micro string library: shared library
    ii  libuuid1:amd64             2.29.2-1+deb9u1                amd64        Universally Unique ID library
    ii  localepurge                0.7.3.4                        all          reclaim disk space by removing unneeded localizations
    ii  locales                    2.24-11+deb9u4                 all          GNU C Library: National Language (locale) data [support]
    ii  login                      1:4.4-4.1                      amd64        system login tools
    ii  lsb-base                   9.20161125                     all          Linux Standard Base init script functionality
    ii  mawk                       1.3.3-17+b3                    amd64        a pattern scanning and text processing language
    ii  mime-support               3.60                           all          MIME files 'mime.types' & 'mailcap', and support programs
    ii  mount                      2.29.2-1+deb9u1                amd64        tools for mounting and manipulating filesystems
    ii  multiarch-support          2.24-11+deb9u4                 amd64        Transitional package to ensure multiarch compatibility
    ii  ncurses-base               6.0+20161126-1+deb9u2          all          basic terminal type definitions
    ii  ncurses-bin                6.0+20161126-1+deb9u2          amd64        terminal-related programs and man pages
    ii  net-tools                  1.60+git20161116.90da8a0-1     amd64        NET-3 networking toolkit
    ii  openssl                    1.1.0k-1~deb9u1                amd64        Secure Sockets Layer toolkit - cryptographic utility
    ii  passwd                     1:4.4-4.1                      amd64        change and administer password and group data
    ii  perl                       5.24.1-3+deb9u5                amd64        Larry Wall's Practical Extraction and Report Language
    ii  perl-base                  5.24.1-3+deb9u5                amd64        minimal Perl system
    ii  perl-modules-5.24          5.24.1-3+deb9u5                all          Core Perl modules
    ii  procps                     2:3.3.12-3+deb9u1              amd64        /proc file system utilities
    ii  psmisc                     22.21-2.1+b2                   amd64        utilities that use the proc file system
    ii  python                     2.7.13-2                       amd64        interactive high-level object-oriented language (default version)
    ii  python-minimal             2.7.13-2                       amd64        minimal subset of the Python language (default version)
    ii  python2.7                  2.7.13-2+deb9u3                amd64        Interactive high-level object-oriented language (version 2.7)
    ii  python2.7-minimal          2.7.13-2+deb9u3                amd64        Minimal subset of the Python language (version 2.7)
    ii  readline-common            7.0-3                          all          GNU readline and history libraries, common files
    ii  sed                        4.4-1                          amd64        GNU stream editor for filtering/transforming text
    ii  sensible-utils             0.0.9+deb9u1                   all          Utilities for sensible alternative selection
    ii  sysvinit-utils             2.88dsf-59.9                   amd64        System-V-like utilities
    ii  tar                        1.29b-1.1                      amd64        GNU version of the tar archiving utility
    ii  tzdata                     2019b-0+deb9u1                 all          time zone and daylight-saving time data
    ii  ucf                        3.0036                         all          Update Configuration File(s): preserve user changes to config files
    ii  unzip                      6.0-21+deb9u1                  amd64        De-archiver for .zip files
    ii  util-linux                 2.29.2-1+deb9u1                amd64        miscellaneous system utilities
    ii  whiptail                   0.52.19-1+b1                   amd64        Displays user-friendly dialog boxes from shell scripts
    ii  xtail                      2.1-5.1+b1                     amd64        like "tail -f", but works on truncated files, directories, more
    ii  zlib1g:amd64               1:1.2.8.dfsg-5                 amd64        compression library - runtime
