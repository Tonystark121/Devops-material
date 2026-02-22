Life before Virtualization:
    * To run app/services, each required its own physical server(Server in data center).
    * One server could only run one service at a time.(Date isolation)
    * Server are always over-provisioned to handle peak loads. and most of the time, resources are under-utilized.
    * Huge cap expense and op expense to maintain physical servers.

Virtualization -> Enter VMwares, Hyper-V, KVM:
    * Virtualization allows multiple virtual servers to run on a single physical server.
    * Each VM has its own OS, libraries, and dependencies.
    * Better resource utilization as multiple VMs can share the same physical resources.
    * Easier to manage and deploy new services as VMs can be created, cloned, and migrated easily.

    Hardware -> Hypervisor(Host OS) -> Multiple Guest OS(Each running its own services)

Termminologies:
    * Host OS: The physical server's operating system that runs the hypervisor.
    * Guest OS: The operating systems running inside the virtual machines.
    * VM (Virtual Machine): An emulation of a computer system that runs on top of the host OS.
    * Hypervisor: Software that creates and manages virtual machines by abstracting the physical hardware.
    * Snapshot: A saved state of a VM at a specific point in time, allowing for easy rollback.

Type of Hypervisors:
    * Type 1 (Bare-metal): Runs directly on the physical hardware. Examples: VMware ESXi, Microsoft Hyper-V, Xen. Run as a Base OS. Mostly for Production.
    * Type 2 (Hosted): Runs on top of a host operating system. Examples: VMware Workstation, Oracle VirtualBox. Runs as Software Application. Mostly for Development and Testing.


👍👍👍👍👍👍 Thumb Rule -> If you want to automate something make sure you know how to do it manually.


Steps to create VM:
    1. Install Hypervisor on Host OS. (Oracle VitualBox, VMware Workstation for Type 2; VMware ESXi, Microsoft Hyper-V for Type 1)
    2. Iso file -> centos, ubuntu
    3. Login tool -> Git bash and putty
    2. Create a new VM and allocate resources (CPU, RAM, Disk).
    3. Install Guest OS on the VM.
    4. Install necessary drivers and tools for better performance.
    5. Configure network settings for the VM.
    6. Install required applications and services on the Guest OS.
    7. Take a snapshot of the VM for future reference.



Linux:
    1. intro to linux
    2. Basic commands in linux
    3. understanding file in linux
    4. Files and redirection
    5. Users & Group
    6. Sudo
    7. Software Management
    8. Services & process
    9. Good to know commands 
    10. Server Management


Basically we will be focusing 4 areas in Linux:
    1. Commands
    2. Files
    3. Sofware Management
    4. Server Management

Linux -> Open source OS/Kernal
In 1984, The GNU project and Free Software Foundation
    Creates Open source version of UNIX utilities
    Create the General Public License (GPL)
        Software License enforcing open source principles.
In 1991, Linus Torvalds
    Creates Open Source, Unix like Kernal released Under the GPL
    Port Some GNU Utilities, Solicits assistance online

Today, 
    Linux Kernal + GNU utilities = complete Open source unix like OS.
    Packaged for targated audiances as distribution.

Linux Principles:
    1. Everything is file (including hardware)
    2. Small single purpose programs. (one thing at a time.)
    3. Ability to chain program together for complex operation.
    4. Avoid Captive User interface.(make less user interation)
    5. Configured data stored in text file. (we don't need to go to setting change things. just edit file and things are done.)

Why Linux:
    1. Open source
    2. Community Support
    3. Support Wide range of Hardware
    4. Customization
    5. Most servers runs on linux
    6. Automation
    7. Security


Popular Linux distros:
    1. Ubuntu
    2. Linux Mint
    3. Arch Linux
    4. Fedora
    5. Debian 
    6. Open Suse

Popular Server Linux OS
    1. Red Hat Enterprise Linux (not open source)
    2. Ubuntu Server
    4. CentOS
    4. Suse Enterprise Linux

Most used Linux distros currently in IT industry.
    1. RPM based : RHEL, CentOS, Oracle, Amazon Linux
    2. Debian based : Ubuntu Server, Kali Server.
        the major difference b/w to family of linux is packing method of softwares.

Some Important Libraries:
    1. Home Directories -> /root, /home/username
    2. User Executible -> /bin, /usr/bin, /usr/local/bin
    3. System Executible -> /sbin, /usr/sbin, /usr/local/sbin
    4. Other Mountpoints -> /media, /mnt
    5. Configuration -> /etc
    6. Temporary Files -> /tmp
    7. Kernels & Bootloaders -> /boot
    8. Server Data -> /var, /srv
    9. System Information -> /proc, /sys
    10. Shared Libraries -> /lib, /usr/lib, /usr/local/lib


###### Commands and File System

cd / -> root director
pwd -> gives present working directory
ls -> list of all items in that directory
cd -> get us back to main directory
/sbin -> contains executable cmd by root user.

three things in Linx Commands -> Commads options arguments 
1. grep rajeev(text to find) fileName 
    Linux is case sensitive
2. grep Rajeev(text to find) fileName 
3. if want all use grep -i text filename
4. if we want to search in all directory
    grep -i rajeev * -> this will search in each file in folder, not in folders in folder
5. cp a/notes.txt b/readme.txt -> copy a file from source to destination
6. grep -iR rajeev * -> this will search in each file in folder, also in folders in folder
7. grep -R SELINUX /etc/* -> find word SELINUX in everthing inside /etc folder
8. to open any file in vim editor -> vim filePath
9. grep -vi rajeev /etc/* -> do not find anything which contain rajeev.
10. less fileName -> opens reader mode of file, also can search /keyword
11. more fileName -> opens reader mode too with some effect. use and see.
12. head fileName -> shows first 10 lines
13. head -n fileName -> shows first n lines
14. tail is opposite to head. one imp use tail -f fileName which shows dynamic contain and latest changes which help to keep track of logs.
15. cat /etc/passwd -> contain all info related to user
16. sed '/rajeev/ranjan/g' * -> this will replace all rajjev to ranjan present anywhere in the folder. this will not change it
        if you want to change use sed -i '/rajeev/ranjan/g' *