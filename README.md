update_desinfect
================

A small bash script to automagically update a Desinfec't image

The script is currently intended to be used for PXE boot. But you can easily
add a mkisofs command to the end of the script for creating a iso.
Patches welcome!

The script can be run from a daily cron job to supply your technicians with an
up to date virus definitions to boot on client computers.

Please report bugs/feature requests via github.

Sample pxelinux.cfg entry
=========================

	LABEL desinfect
    	menu label Desinfect
    	kernel desinfect/casper/vmlinuz
    	append initrd=desinfect/casper/initrd.lz boot=casper netboot=nfs nfsroot=$yourbootserver:/data/boot/desinfect/ splash quiet -- debian-installer/language=de console-setup/layoutcode?=de
