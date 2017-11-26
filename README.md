etup-scripts

for opencocon distribution

# How to prepare opencocon build environment

1. clone repository 

	$ git clone -b opencocon-v10 https://github.com/dejiko/cocon-setup-scripts.git
	$ cd cocon-setup-scripts

2. change setting file

Edit these setting files.

* conf/bblayers.conf

Change PUT_MACHINE_NAME_IN_HERE to your target machine name.

* conf/local.conf

** Put machine name to :

	MACHINE="cocon486"

Machine name is currently cocon486 (x86 PC), coconx64 (x64 PC), raspberrypi (Raspberry Pi 1, untested on v10), ac100 (Dynabook AZ,experimental)


** Using libc (currently glibc or musl) :

	OPENCOCON_LIBC = "musl"

** Kernel Version (As you need) :

	LINUX_LIBC_HEADERS_VERSION = "4.4.93"

3. run oebb.sh

	$ ./oebb.sh config cocon486

# How to build opencocon

	$ . ./opencocon
	$ bitbake opencocon-image initramfs-crusoe-image


To make CD image of opencocon x86/x64, run also [cocon-cdcreator](https://github.com/dejiko/cocon-cdcreator) after build.


# See also

[Original setup-scripts by Angstrom](https://github.com/Angstrom-distribution/meta-angstrom)

