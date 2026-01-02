+++
title = "Setting up VM for enterprise environment"
author = ["James"]
date = 2025-12-28T13:36:00+00:00
draft = false
+++

## The Enterprise Virtualization Stack {#the-enterprise-virtualization-stack}

I will need to set up my instance of Virtual Machine in a way that sort of replicates a professional enterprise environment as closely as possible.

So instead of using a third-party application like [VirtualBox](https://www.virtualbox.org/), I will instead go for the native Linux virtualisation stack.


### Components for the stack {#components-for-the-stack}

-   [KVM ( Kernel-based Virtual Machine )](/kvm-kernel-based-virtual-machine/#what-is-it) - Handles the heavy lifting of CPU and memory
-   [QEMU](/qemu/#hardware-emulation) - The "hands and feet" of the VM, providing the emulated hardware ( think USB ports and network cards, etc )
-   [Libvirt](/libvirt/#security) - The "engine" or "nervous system" of the VM; The API that controls the brain and body.
-   [Virt-manager](/virt-manager/#decision-and-shift) - The "user interface" you interact with.&nbsp;[^fn:1]


## Infrastructure Setup {#infrastructure-setup}

I will be using `virt-install` to ensure the environment is reproducible.


### Preparation {#preparation}

Before that, we need to make sure that [Libvirt](/libvirt/#security) is installed and `libvirtd` is running.

```bash
sudo pacman -S libvirt

sudo systemctl start libvirtd
```

And we will also need a copy of the ISO, we could do so by using the `wget` to
download a copy from [Rocky Linux](https://rockylinux.org/)'s website. In this case, I chose the minimal
version which is likely to be better for learning purpose as we don't require
"unnecessary" tools that the default ships with.

```bash
wget https://download.rockylinux.org/pub/rocky/10/isos/x86_64/Rocky-10.1-x86_64-minimal.iso
```

[^fn:1]: This is no longer part of the stack after [consideration](/virt-manager/#decision-and-shift)
