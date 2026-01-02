+++
title = "Libvirt"
author = ["James"]
date = 2026-01-02T20:01:00+00:00
draft = false
+++

## <span class="org-todo todo TODO">TODO</span> Content {#content}

Libvirt is technically an open-source API, daemon (libvirtd), and management tool.

The main goal for Libvirt is to provide a single way to manage multiple different virtualisation
hypervisors. ( For example, [KVM](/kvm-kernel-based-virtual-machine/#what-is-it)/[QEMU](/qemu/#hardware-emulation) in [my use case](/setting-up-vm-for-enterprise-environment/#components-for-the-stack). )

My understanding is that it provides a universal/unified way of operating and using a VM.
So it's basically serving as an abstraction layer to make doing things easier. For example,
instead of running long commands to execute actions like starting a VM, you simple rely on
Libvirt to "start" the VM regardless of the underlying technology.


## How does it relate to [my plan](/12-weeks-action-plan-for-my-career-change/#week-11-12-interview-drill)? {#how-does-it-relate-to-my-plan--12-weeks-action-plan-for-my-career-change-dot-md}

The "Enterprise Perspective", if you will.


### Automation Compatibility {#automation-compatibility}

Modern tools like [Terraform](/terraform/#content), [Ansible](/ansible/#content) and [Vagrant](/vagrant/#content) does not interact with [QEMU](/qemu/#hardware-emulation) or [KVM](/kvm-kernel-based-virtual-machine/#what-is-it) directly.
This is where the Libvirt API comes in handy. Libvirt will be the interface that your
code will use.


### Virtualisation Agnosticism {#virtualisation-agnosticism}
