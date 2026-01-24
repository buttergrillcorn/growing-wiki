+++
title = "Learning Rocky Linux"
author = ["James"]
date = 2026-01-24T17:06:00+00:00
draft = false
+++

## <span class="org-todo todo TODO">TODO</span> Prerequisite {#prerequisite}

Before we dive right in with the package manager and system configurations. It is in our
best interest to first check that the installation is "correct".

We simply do a quick check on the state of RAM and CPU on our new VM.


### RAM check {#ram-check}

To check RAM, we can do something like:

```bash
free --human --total --wide
```

`free` is a simple command that is the standard way for checking memory usage.
In this case, I utilise three flags to help make the output to be visually clearer for myself.

-   `--human` makes the output to be, well, more **"human"** readable
-   `--total` will show the **total** of RAM + Swap
-   `--wide` simply makes the output to be **wider** (for my screen), totally unnecessary.


### CPU cores check {#cpu-cores-check}

As for checking the CPU cores, we can use `nproc`. What `nproc` does is basically to check
for the information regarding CPU core numbers, listed in `/proc/cpuinfo`. It will output
a number which represents the amount of CPU cores that is present.
