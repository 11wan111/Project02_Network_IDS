
## Virtual Machines

### What it is
**Virtual Machines (VMs)** are software-based emulations of physical computers, created using **Oracle VirtualBox**. This project uses three VMs: **Ubuntu 24.04 LTS**, **Kali Linux**, and **Metasploitable 2**.

### Why it is important to this project
VMs provide a safe, isolated environment for simulating attacks and testing Snort. **Ubuntu** runs Snort to detect threats, **Kali** launches attacks, and **Metasploitable** offers vulnerable services. The **Host-Only network** (`192.168.56.0/24`) ensures controlled traffic, showcasing virtualization and network security skills for this portfolio.

### Installation guide
1. **Install Oracle VirtualBox** on Windows 11:
   - Download from [virtualbox.org](https://www.virtualbox.org).
   - Run installer, follow prompts.
2. **Configure VMs**:
   - **Ubuntu 24.04 LTS** (`192.168.56.103`):
     - Download ISO from [ubuntu.com](https://ubuntu.com/download/server).
     - Create VM: 2GB RAM, 20GB disk, Host-Only Adapter.
     - Install via ISO, follow prompts.
   - **Kali Linux** (`192.168.56.102`):
     - Download ISO from [kali.org](https://www.kali.org/get-kali).
     - Create VM: 2GB RAM, 20GB disk, Host-Only + NAT Adapter.
     - Install via ISO, follow prompts.
   - **Metasploitable 2** (`192.168.56.104`):
     - Download from [sourceforge.net](https://sourceforge.net/projects/metasploitable).
     - Import VM, set Host-Only Adapter.
3. **Verify Network**:
   - Run `ifconfig` on each VM to confirm IPs.
   - Test connectivity: `ping 192.168.56.104` from Kali.

### Basic use case
- Launch VMs in VirtualBox.
- On Ubuntu, start Snort:
```bash
sudo snort -A console -c /etc/snort/snort.conf -i enp0s3