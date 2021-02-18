# squid-with-http-violations
#### Recompiled Squid 3.5 rpm-package for CentOS 7 that allows to override HTTP headers (with --enable-http-violations option)

USAGE
1. Remove previously installed Squid and erase all dependencies:
```sh
yum autoremove squid
```
2. Install rpm (if needed):
```sh
yum install rpm
```
3. Reinstall dependencies:
```sh
yum install perl-Compress-Raw-Bzip2 perl-Compress-Raw-Zlib perl-DBI perl-Digest perl-Digest-MD5 perl-IO-Compress perl-Net-Daemon perl-PlRPC
```
4. Download from /RPMS/x86_64/ following packages and run:
```sh
rpm -i squid-migration-script-3.5.20-17.el7.5.x86_64.rpm
rpm -i squid-3.5.20-17.el7.5.x86_64.rpm
```
5. Finally, type
```sh
squid -v
```
to make sure that '--enable-http-violations' option exists in current installation.

Furthermore, you may recompile/rebuild rpm package by yourself using /SOURCES and /SPECS from here to add or remove options or even download specific src-rpm version to do that with rpmdevtools.
