+++
title = "Virt-manager"
author = ["James"]
date = 2026-01-02T20:25:00+00:00
draft = false
+++

## <span class="org-todo todo TODO">TODO</span> What is Virt-manager? {#what-is-virt-manager}

Virt-manager or Virtual Machine Manager, is essentially the GUI that the user will be interacting with to
manage the [Libvirt](/libvirt/#security) API.

This means that you can use buttons, sliders and menus instead of writing XML code or long commands.


## Do we need this? ( For [my plan](/12-weeks-action-plan-for-my-career-change/#week-11-12-interview-drill) ) {#do-we-need-this--for-my-plan-12-weeks-action-plan-for-my-career-change-dot-md}


### Advantage of using Virt-manager {#advantage-of-using-virt-manager}

Virt-manager is simply an UI for [Libvirt](/libvirt/#security); it generates the XML code and sends it to `libvirtd` without
it's own "logic".

A GUI will provide immediate visual feedback and this is very helpful for a beginner. You will be
more likely to spot any error that may occur as well as the reason or source of the error.

Virt-manager actually has an "XML" tab, where you are able to see the update to XML code upon changing a setting. This is a very useful way to learn the syntax without guessing.


### My worry {#my-worry}

I worry that having a GUI will add an unnecessary "abstraction layer" to my learning process.
I would prefer to learn the XML code and CLI commands straightaway, which I believe is more
likely to be the case in a professional enterprise environment or work setting.


### Decision and shift {#decision-and-shift}

I think it is probably better for me to go down the "harder" route, replacing GUI "point and click" with:

-   Learning and using `virsh` commands.
-   Manually edit and define the XML code.
