# 🧰 LPIC-1 Objective 102.2: Install a Boot Manager

## 📚 Introduction
This lab focuses on selecting, installing, and configuring a Linux boot manager. You'll work hands-on with GRUB Legacy and GRUB 2, simulate dual-boot environments, and perform bootloader recovery from a broken configuration. This lab is vital for understanding how a Linux system starts and how to control and repair that process.

## 1️⃣ Providing Alternative Boot Locations and Backup Boot Options

🔸 Open /etc/grub.d/40_custom in a text editor

🔸 Add a custom menu entry to define a backup boot configuration

🔸 Rebuild the GRUB configuration with grub-mkconfig

🔸 Reboot and test the new menu entry

## 2️⃣ Install and Configure a Boot Loader such as GRUB Legacy

🔸 Install GRUB Legacy using your package manager

🔸 Edit /boot/grub/menu.lst to create a new boot entry

🔸 Add a boot entry pointing to the appropriate root and kernel

🔸 Install GRUB Legacy to the MBR using grub-install

🔸 Reboot and test the GRUB Legacy configuration

## 3️⃣ Perform Basic Configuration Changes for GRUB 2

🔸 Edit /etc/default/grub to modify boot parameters like timeout and default entry

🔸 Update values such as GRUB_TIMEOUT, GRUB_DEFAULT, and GRUB_CMDLINE_LINUX

🔸 Regenerate the GRUB configuration using grub-mkconfig

🔸 Optionally, set a specific default entry with grub-set-default

## 4️⃣ Interact with the Boot Loader

🔸 Reboot the system and press e to edit a GRUB menu entry

🔸 Modify the linux line to append a boot parameter like single

🔸 Boot with the modified entry using Ctrl + X or F10

🔸 If GRUB is broken, boot into a Live CD

🔸 Mount the root partition and system directories

🔸 Chroot into the mounted system

🔸 Reinstall GRUB to the disk

🔸 Regenerate GRUB configuration

🔸 Exit chroot and reboot the system

## 🧠 What I Learned
In this lab, I learned how to install, configure, and troubleshoot GRUB boot loaders on a Linux system. I practiced editing GRUB 2 settings, adding custom boot entries, and recovering from boot failures using chroot and a Live CD. This gave me a deeper understanding of the Linux boot process and system recovery techniques.
