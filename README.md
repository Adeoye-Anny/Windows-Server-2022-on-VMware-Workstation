# Windows Server 2022 Virtual Machine

![Windows-Server-2022_1_](https://github.com/user-attachments/assets/55e47307-0665-409d-8da9-f8fb30f8a162)


## 3.0 What I Did and Why

I created a dedicated VM to host Windows Server 2022 so I could practice server administration without affecting my main computer.

After creating the virtual machine, the next step I performed was installing Windows Server 2022 on it. This installation forms the foundation for all Active Directory, DNS, DHCP, and domain configuration tasks in my lab.

Link to Download Windows Server 2022 -[Download Windows Server 2022](https://www.microsoft.com/en-us/evalcenter/download-windows-server-2022)


## 3.1 Booting the VM and Starting Windows Setup

1. I powered on the VM from VMware Workstation by clicking Power on this virtual machine.
2. The VM automatically detected the ISO file I attached earlier and booted into the Windows Server installation environment.
3. The Windows Setup screen appeared with language and region selection options.


## 3.2 Selecting Language and Installation Preferences

1. On the first setup page I selected:
   * Language: English (United States)
   * Time and currency format: English
   * Keyboard layout: US
2. I clicked Next and then selected Install Now to begin installation.


## 3.3 Choosing the Windows Server 2022 Edition

1. I was presented with a list of available editions. I selected:
      Windows Server 2022 Standard (Desktop Experience)
   
2. I chose this version because the Desktop Experience provides a GUI, which is ideal for demonstrating system administration tasks and Active Directory labs.
3. I clicked Next.


## 3.4 Accepting License Terms

1. I reviewed the Microsoft Software License Terms as required.
2. I selected I accept the license terms.
3. I clicked Next to continue installation.


## 3.5 Choosing Installation Type

1. I selected Custom: Install Windows only (advanced) to install a fresh copy of Windows Server on the virtual disk created earlier.
2. This option ensures the VM receives a clean installation with no existing configurations.


## 3.6 Creating and Selecting the Virtual Disk Partition

1. I was shown the virtual disk I created (typically 60 GB).
2. Since it was unallocated space, I clicked New to create a primary partition for the OS.
3. I used the full disk capacity for simplicity in this lab.
4. After the partition was created automatically, I selected the Primary partition and clicked Next.


## 3.7 Copying Files and Completing Installation

1. Windows Server setup began copying files to the disk. The process included:
   * Copying Windows files
   * Installing features
   * Applying settings
   * Preparing files for installation
2. This process took several minutes depending on the host machine’s hardware.
3. Once installation finished, the VM automatically restarted.


## 3.8 Setting the Administrator Password

1. After rebooting, the OS displayed the first-time setup screen asking me to create a password for the Administrator account.
2. I set a strong password that meets Windows complexity requirements (uppercase, lowercase, numbers, symbols).
3. I clicked Finish.


## 3.9 Logging into Windows Server 2022 for the First Time

1. Once installation completed, I pressed Ctrl + Alt + Delete inside VMware.
2. I entered the Administrator password I created earlier.
   <img width="1920" height="1036" alt="image" src="https://github.com/user-attachments/assets/a141a44d-aee9-4b8f-acae-76fcd68cbe90" />
3. Windows Server loaded into the Desktop Experience interface.
4. Server Manager launched automatically, confirming that the OS installed successfully.
   <img width="1920" height="1036" alt="image" src="https://github.com/user-attachments/assets/1cafee73-5402-4b3e-96cb-e225a84c3303" />



## 3.10 Initial Server Configuration Tasks I Performed

Right after installation, I completed standard post-installation tasks:

1. Renamed the Server
   * I renamed the server to DC01 to reflect its future role as a domain controller.
2. Assigned Static IP Address
   Before configuring Active Directory, I set a static IPv4 address through Network and Sharing Center, including:
   
   * IP address
   * Subnet mask
   * Default gateway
   * Preferred DNS pointing to the server itself

4. Installed VMware Tools
   * I installed VMware Tools to improve performance, enable copy/paste, and allow resolution scaling.



Installation Completed
At this point, Windows Server 2022 was fully installed and configured, and the VM was ready for the next stage:
Installing Active Directory Domain Services (AD DS).




