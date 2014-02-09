update_desinfect
================

A small bash script to automagically update a Desinfec't image

The script is currently intended to be used for PXE boot. But you can easily
add a mkisofs command to the end of the script for creating a iso.
Patches welcome!

The script can be run from a daily cron job to supply your technicians with an
up to date virus definitions to boot on client computers.

Please report bugs/feature requests via github.

Purchase Desinfec't
===================

To get a copy of Desinfec't you'll have to purchase ct't 10/2013 you can get it
from Heise's online shop: http://shop.heise.de/katalog/ct-10-2013

Sample pxelinux.cfg entry
=========================

	LABEL desinfect
    	menu label Desinfect
    	kernel desinfect/casper/vmlinuz
    	append initrd=desinfect/casper/initrd.lz boot=casper netboot=nfs nfsroot=$yourbootserver:/data/boot/desinfect/ splash quiet -- debian-installer/language=de console-setup/layoutcode?=de

Donations
=========

If you found this little script useful and have some coins to spare I'd really
appreciate a donation to 1AZnusXgiYf5SxUDtBi4G2sAwcwXaSCeTH
