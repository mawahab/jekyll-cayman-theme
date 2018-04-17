---
layout:     post
title:      "Device tree"
date:       2018-04-17 11:26:00
author:     "MAW"
---
A device tree is a file that contains information about hardware devices in a tree structure format. This file is saved in device tree script (.dts file) and then compiled into a device tree blob (.dtb). The dtb is used by the kernel during boot to load drivers for each device contained in it. 
The device tree has not always been part of the kernel. It has been added in order to provide flexibility to provide a mean to specify hardware components more easily. Most of the boards have different address spaces for each component. 

[Link](https://elinux.org/Device_Tree_Reference).
