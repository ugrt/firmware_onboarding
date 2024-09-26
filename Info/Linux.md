# Linux (Ubuntu)
Ubuntu is one of the most popular Linux distributions with plenty of documentation and help available online. It can be run in a virtual machine (VM), using WSL, or installed directly on your computer and dual-booted alongside Windows.

## Using a Virtual Machine
A virtual machine allows you to run a different OS that shares resources with the host OS (like Windows). You are able to see and interact with the OS as if you were actually running it directly on your device, but it requires higher performance compared to running it directly.

Canonical, the Ubuntu creators, have created instructions on [installing a Ubuntu VM using Oracle VM VirtualBox Manager](https://ubuntu.com/tutorials/how-to-run-ubuntu-desktop-on-a-virtual-machine-using-virtualbox#1-overview). 

Here is a video if you prefer:

**[How to install Ubuntu 22.10 LTS in VirtualBox 2024](https://www.youtube.com/watch?v=hYaCCpvjsEY)**

<iframe width="420" height="315"
src="https://www.youtube.com/watch?v=hYaCCpvjsEY">
</iframe> 

## Using WSL
Windows Subsystem for Linux (WSL) allows you to run Ubuntu or another Linux distribution in the Windows terminal itself. Unlike a VM, it is a shell environment, meaning you do not see a graphical desktop, but you can still install and run programs via terminal just like the VM.

Instructions on installing WSL are on [Microsoft's WSL Documentation](https://learn.microsoft.com/en-us/windows/wsl/install).

## Dual Booting
Canonical has also made instructions on how to [install Ubuntu Desktop](https://ubuntu.com/tutorials/install-ubuntu-desktop#1-overview) which includes how to dual boot alongside Windows. This means Ubuntu is running directly on your machine, same as Windows, which is better for performance since it can use all resources but requires relaunching your PC so you can launch Ubuntu instead of Windows.

**Be careful** not to overwrite your current Windows files when installing Ubuntu. This will require [creating a new partition](https://ubuntu.com/tutorials/install-ubuntu-desktop#manual-partitioning) or installing Ubuntu on a different storage device than Windows.

If you are worried about installing over Windows, WSL or a VM are the safer options.

