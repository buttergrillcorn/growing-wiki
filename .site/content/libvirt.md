+++
title = "Libvirt"
author = ["James"]
date = 2026-01-02T20:01:00+00:00
draft = false
+++

## <span class="org-todo todo TODO">TODO</span> Content {#content}

Libvirt is technically an open-source API, daemon (libvirtd), and management tool.

The main goal for libvirt is to provide a single way to manage multiple different virtualisation
hypervisors. ( For example, [KVM](/kvm-kernel-based-virtual-machine/#what-is-it)/[QEMU](/qemu/#hardware-emulation) in [my use case](/setting-up-vm-for-enterprise-environment/#components-for-the-stack). )

My understanding is that it provides a universal/unified way of operating and using a VM.
So it's basically serving as an abstraction layer to make doing things easier. For example,
instead of running long commands to execute actions like starting a VM, you simple rely on
libvirt to "start" the VM regardless of the underlying technology.
