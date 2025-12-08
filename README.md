# Windows Server 2022 Virtual Machine

![Windows-Server-2022_1_](https://github.com/user-attachments/assets/55e47307-0665-409d-8da9-f8fb30f8a162)


## What I Did and Why
I created a dedicated VM to host Windows Server 2022 so I could practice server administration without affecting my main computer.

## Steps I Performed
1. I opened VMware Workstation and selected Create a New Virtual Machine.
2. I chose Custom (advanced) to manually allocate system resources like RAM and CPU.
3. I attached the Windows Server 2022 ISO file.
4. I configured:
    * 8GB RAM for smooth AD DS operations
    * 2 CPU cores
    * 60GB virtual disk with NVMe controller
5. I selected NAT networking so the server could access the internet through my host machine.
6. I finalized the setup and powered on the VM.
