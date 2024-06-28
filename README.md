# Parrot-OSHome-lab-vm-setup
Parrot OS Setup on VMware
# Setting Up a Parrot OS Virtual Machine on VMware Workstation

This guide provides a step-by-step process to create and configure a Parrot OS VM on VMware Workstation.

## Table of Contents
1. [Prerequisites](#prerequisites)
2. [Download Parrot OS](#download-parrot-os)
3. [Create a New Virtual Machine](#create-a-new-virtual-machine)
4. [Configure the VM Settings](#configure-the-vm-settings)
5. [Install Parrot OS](#install-parrot-os)
6. [Post-Installation Steps](#post-installation-steps)
7. [Troubleshooting](#troubleshooting)

## Prerequisites

- VMware Workstation installed on your system.
- Minimum 20 GB of free disk space.
- Minimum 4 GB of RAM.
- An active internet connection.

## Download Parrot OS

1. Go to the [Parrot OS download page](https://www.parrotsec.org/download/).
2. Choose the appropriate edition (Home or Security) and click the download link for the `.iso` file.

   ![Download Parrot OS](images/parrot-os-download.png)

## Create a New Virtual Machine

1. Open VMware Workstation and click on `Create a New Virtual Machine`.

   ![Create New VM](images/create-new-vm.png)

2. Choose `Typical (recommended)` and click `Next`.

   ![Typical Installation](images/typical-installation.png)

3. Select `Installer disc image file (iso)` and browse to the downloaded Parrot OS `.iso` file. Click `Next`.

   ![Select ISO](images/select-iso.png)

## Configure the VM Settings

1. Name your virtual machine (e.g., `Parrot OS`) and choose a location for storing the VM files. Click `Next`.

   ![Name and Location](images/name-location.png)

2. Set the disk size. It is recommended to allocate at least 20 GB. Choose `Store virtual disk as a single file` and click `Next`.

   ![Disk Size](images/disk-size.png)

3. Review the hardware settings. You can customize these settings by clicking `Customize Hardware...`. It's recommended to assign at least 2 GB of RAM and 2 CPU cores. Click `Finish` to complete the setup.

   ![Hardware Settings](images/hardware-settings.png)

## Install Parrot OS

1. Start the virtual machine. Parrot OS installer should boot up. Choose the `Install` option.

   ![Install Parrot OS](images/install-parrot-os.png)

2. Follow the on-screen instructions to complete the installation. You'll be prompted to select your language, time zone, and keyboard layout.

   ![Language Selection](images/language-selection.png)

3. Create a new user and set a password during the installation process.

   ![User Setup](images/user-setup.png)

4. Partition the disk. For simplicity, you can choose `Guided - use entire disk`. Confirm the changes and proceed with the installation.

   ![Partition Disk](images/partition-disk.png)

5. After the installation completes, restart the VM. Remove the installation media if prompted.

   ![Restart VM](images/restart-vm.png)

## Post-Installation Steps

1. Once the VM restarts, log in with your new user credentials.
2. Install VMware Tools for better performance and additional functionality.
   - In VMware Workstation, go to `VM` > `Install VMware Tools`.
   - Follow the instructions to mount the VMware Tools ISO.
   - Open a terminal and run the following commands to install the tools:
     ```bash
     sudo apt update
     sudo apt install open-vm-tools-desktop
     ```
   - Restart the VM to apply the changes.

   ![VMware Tools Installation](images/vmware-tools-install.png)

## Troubleshooting

- **VM doesn't boot**: Make sure the ISO is correctly linked and the VM is configured to boot from the ISO.
- **Slow performance**: Check that you've allocated sufficient resources (CPU, RAM) and installed VMware Tools.
- **Network issues**: Ensure the VM's network adapter is set to `Bridged` or `NAT`.

gnome-screenshot -f images/PARROT-OS-HOMESCREEN.png
