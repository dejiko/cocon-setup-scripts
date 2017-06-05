# cocon-setup-scripts
for opencocon distribution

# How to prepare opencocon build environment

1. clone repository 

```$ git clone -b opencocon-v11 https://github.com/dejiko/cocon-setup-scripts.git
$ cd cocon-setup-scripts```

2. change setting file

Edit these setting files.

conf/bblayers.conf
Change PUT_MACHINE_NAME_IN_HERE to your target machine name.

conf/local.conf
'''
# Put machine name to :
MACHINE="cocon486"

# Using libc (currently glibc or musl) :
OPENCOCON_LIBC = "glibc"

# Kernel Version (As you need) :
LINUX_LIBC_HEADERS_VERSION = "4.10.42"
'''

3. run oebb.sh

```$ ./oebb.sh config primo81```


# How to build opencocon

```
$ . ./opencocon
$ bitbake [Package name]
```

to make CD image of opencocon x86/x64, do also [cocon-cdcreator](https://github.com/dejiko/cocon-cdcreator) after build.


# See also

[Original setup-scripts by Angstrom](https://github.com/Angstrom-distribution/meta-angstrom)
