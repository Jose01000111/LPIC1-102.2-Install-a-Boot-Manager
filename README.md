# 🧰 LPIC-1 Objective 102.2: Install a Boot Manager

## 📚 Introduction
This lab focuses on selecting, installing, and configuring a Linux boot manager. You'll work hands-on with GRUB Legacy and GRUB 2, simulate dual-boot environments, and perform bootloader recovery from a broken configuration. This lab is vital for understanding how a Linux system starts and how to control and repair that process.

I’ve included some helpful links to guide you through the lab and for studying afterward:

[Objective 102.2 Install a Boot Manager](https://www.lpi.org/our-certifications/exam-101-102-objectives/#102.2_Install_a_boot_manager)

---

[Objective 102.2 NOTES](https://1drv.ms/w/c/354f1c8d534fbced/EelLXY620NJCqMo5GQiSvrMBq1a8zwt668jKiaQA884hcg?e=owkp2e)

---

[Lab 102.2](https://1drv.ms/w/c/354f1c8d534fbced/EXJLyL2oIGNPnosS478POZMBvzmj7GEiSSXWhS_IbBMWWQ?e=Ehnyi4)

---

## 1️⃣ Providing Alternative Boot Locations and Backup Boot Options

🔸 Open /etc/grub.d/40_custom in a text editor

![t3wrw98](https://github.com/user-attachments/assets/e0ffbad5-88c4-4099-ae96-b0559dabb59d)

🔸 Add a custom menu entry to define a backup boot configuration

![E8sW2MX](https://github.com/user-attachments/assets/b5269069-f577-405f-9aee-e35db6817ce2)

🔸 Rebuild the GRUB configuration with grub-mkconfig

🔸 Reboot and test the new menu entry

![xSfOZDU](https://github.com/user-attachments/assets/8debc02d-8885-4aaf-a491-6717503bef01)

## 2️⃣ Install and Configure a Boot Loader such as GRUB Legacy

🔸 Install GRUB Legacy using your package manager

🔸 Edit /boot/grub/menu.lst to create a new boot entry

🔸 Add a boot entry pointing to the appropriate root and kernel

🔸 Install GRUB Legacy to the MBR using grub-install

🔸 Reboot and test the GRUB Legacy configuration

![xSfOZDU](https://github.com/user-attachments/assets/f8daf4b9-951c-41c3-846a-1a4bbc607fd6)

## 3️⃣ Perform Basic Configuration Changes for GRUB 2

## ⚠️ I didn’t perform Step 3 (mounting the installed system) on my main Rocky Linux VM to avoid accidentally breaking it.  
## 🛡️ Instead, I documented the process carefully to practice later on a safe test VM or snapshot.

🔸 Edit /etc/default/grub to modify boot parameters like timeout and default entry

![8uocCcO](https://github.com/user-attachments/assets/76910a40-d3c3-4dad-ba88-5eb67ba9334f)

🔸 Update values such as GRUB_TIMEOUT, GRUB_DEFAULT, and GRUB_CMDLINE_LINUX

![ReUI828](https://github.com/user-attachments/assets/68883787-e18f-4ca4-b484-cc74e1e26989)

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
