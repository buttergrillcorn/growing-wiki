+++
title = "KVM ( Kernel-based Virtual Machine )"
author = ["James"]
date = 2025-12-28T13:41:00+00:00
draft = false
+++

## What is it? {#what-is-it}

KVM ( Kernel-based Virtual Machine ) is a hypervisor built into the Linux kernel ( [source](https://wiki.archlinux.org/title/KVM) ).

It is basically a module in the Linux kernel that turns it into a "Type-1" hypervisor, so that the VM
runs **directly** on the hardware for better performance than if it were on the software layer.
