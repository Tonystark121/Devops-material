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

