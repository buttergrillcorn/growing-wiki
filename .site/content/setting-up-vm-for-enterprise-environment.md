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

sudo systemctl enable libvirtd.service    # This will also enable virtlogd.socket
                                          # and virtlocked.socket

sudo systemctl start libvirtd.service
```

And we will also need a copy of the ISO, we could do so by using the `wget` to
download a copy from [Rocky Linux](https://rockylinux.org/)'s website. In this case, I chose the minimal
version which is likely to be better for learning purpose as we don't require
"unnecessary" tools that the default ships with.

```bash
wget https://download.rockylinux.org/pub/rocky/10/isos/x86_64/Rocky-10.1-x86_64-minimal.iso ~/Download/
# This basically pulls the minimal version of ISO from their website
# and download it onto the "Download" folder in our home directory.
```


### Virsh {#virsh}

`Virsh` is the program we will use to manage our virtual machines in our terminal, without a GUI.
The command will be available as part of the `libvirt` library.

You can run an interactive terminal by simply running just `virsh`, which also has support for tab completion.


#### Storage **Pools** {#storage-pools}

To proceed with our installation of VM, we will need a specified location where our storage volume can be kept.
This is often called "virtual disks" or "virtual machine images" in other tools.

Pool locations can be:

-   directory
-   network filesystem
-   partition

Pools can also be **toggled** active or inactive and allocated for space.

<!--list-separator-->

-  Creating a new pool

    There are couple of different ways to create a new pool, depending on the type
    of pool you wish to use.

    ```bash
    virsh pool-define-as poolname /home/user/dir --targer /target/dir
    ```

    Next up, we will have to build and start the pool that we've created:

    ```bash
    virsh pool-build poolname
    virsh pool-start poolname
    virsh pool-autostart poolname
    ```


### Domain {#domain}

After the pool has been created and started successfully, we will need a domain.
A domain is basically the "virtual machine", think of it as an instance of a machine.

We can do this in two main ways, either graphically using `virt-manager` or in terminal with a CLI tool ( in this case, we will use `virt-install` ).

First, installed the package <span class="inline-src language-bash" data-lang="bash">`sudo pacman -S virt-install`</span>.

And then we will run the command like so ( with minor tweaks to the directories ):
This command does not only "install" but also defined the virtual hardware.

```bash
virt-install \
    --name rocky-node-01 \
    --memory 2048 \
    --vcpus 2 \
    --os-variant rocky10 \
    --disk pool=rocky,path=/home/dir/to/install-location,size=10 \
    --cdrom /home/dir/to/image/Rocky-10.1-x86_64-minimal.iso \
    --graphics=none
```

[^fn:1]: This is no longer part of the stack after [consideration](/virt-manager/#decision-and-shift)
