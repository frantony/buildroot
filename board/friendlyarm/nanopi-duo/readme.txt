NanoPi Duo

http://www.friendlyarm.com/index.php?route=product/product&product_id=197
http://wiki.friendlyarm.com/wiki/index.php/NanoPi_Duo

Intro
=====

This default configuration will allow you to start experimenting with the
buildroot environment for the NanoPi Duo. With the current configuration
it will bring-up the board, and allow access through the serial console.

How to build it
===============

Configure Buildroot:

    $ make friendlyarm_nanopi_duo_defconfig

Compile everything and build the SD card image:

    $ make

How to write the SD card
========================

Once the build process is finished you will have an image called "sdcard.img"
in the output/images/ directory.

Copy the bootable "sdcard.img" onto an SD card with "dd":

  $ sudo dd if=output/images/sdcard.img of=/dev/sdX
