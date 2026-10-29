# 🔐 Cybersecurity Lab Environment Setup

Building a virtual cybersecurity lab for ethical hacking and authorized security testing.

---

# 📌 Project Overview

This project involves creating a cybersecurity practice environment using Oracle VirtualBox and Kali Linux. The lab provides a virtual platform for learning network security, reconnaissance, vulnerability assessment, and security-tool usage.

A dedicated virtual network helps organize the lab and makes it possible to introduce additional virtual machines for future authorized exercises.

# 🎯 Objectives

The key objectives of this project are to:

- Install and configure VirtualBox.
- Set up Kali Linux as a virtual machine.
- Configure a dedicated NAT Network.
- Check network addressing and connectivity.
- Test DNS resolution.
- Save a clean virtual machine snapshot.
- Record the configuration and testing process.
- Prepare the environment for future cybersecurity exercises.

# 🛡️ Purpose of the Lab

The lab provides a controlled environment for cybersecurity learning and authorized testing.

Possible future activities include:

- Network reconnaissance
- Port scanning
- Vulnerability assessment
- Packet analysis
- Web security testing
- Security-tool experimentation

**Important:** Only test systems that you own or have explicit permission to assess.

## 🏗️ Lab Architecture

The environment uses a host computer running VirtualBox, with Kali Linux operating inside a virtual machine.

Additional virtual machines may be connected to the same lab network for future exercises, provided the network is configured appropriately.

## ⚙️ Lab Configuration

| Component | Configuration |
|---|---|
| Host Operating System | Enter your actual OS |
| Host RAM | Enter your actual RAM |
| Processor | Enter your actual processor |
| Hypervisor | Oracle VirtualBox |
| Security Operating System | Kali Linux |
| Kali Linux RAM | Enter the allocated RAM |
| Virtual Network | NAT Network |
| Network Address | Enter your configured subnet |
| Kali IP Address | Enter your actual VM IP |
| Default Gateway | Enter your actual gateway |
| DNS Server | Enter your configured DNS |
| Future VM Range | Based on your lab subnet |

# 🪜 Lab Setup Procedure

## Step 1 – Prepare the Virtual Machine Files

Obtain the Kali Linux virtual-machine image from the official Kali Linux website. If the downloaded package is compressed, extract it using a suitable archive utility.

## Step 2 – Install VirtualBox

Install Oracle VirtualBox on the host computer. It provides the virtualization platform required to create and manage the Kali Linux VM.

## Step 3 – Configure the NAT Network

Create a dedicated NAT Network in VirtualBox and configure its network prefix and DHCP settings according to your lab requirements.

Record the actual network name, subnet, and other settings so they can be reproduced later.

A NAT Network can allow connected virtual machines to communicate with each other while providing outbound network connectivity.

## Step 4 – Import Kali Linux

Import or create the Kali Linux virtual machine in VirtualBox.

Review the VM's memory allocation and network adapter settings. Attach the adapter to the NAT Network created for this lab.

If required, configure a shared folder for transferring files between the host and virtual machine.

## Step 5 – Check Kali Linux Networking

Inspect the network configuration inside Kali Linux and verify the assigned IPv4 address, subnet, gateway, and DNS settings.

Use the following command to inspect the network interfaces:

```bash
ip a
```

Record the values returned by your own system rather than copying example addresses from another lab.

## Step 6 – Create a Clean Snapshot

Once the virtual machine is configured and working correctly, create a snapshot in VirtualBox.

Give the snapshot a descriptive name, such as `Clean Kali - Network Setup`.

A snapshot provides a convenient recovery point before future experiments or configuration changes.

# 🔎 Lab Verification

Use these commands to check the lab. Replace example addresses with values from your own configuration.

| Test | Command | Purpose |
|---|---|---|
| Inspect IP address | `ip a` | Review interface addresses |
| Check gateway | `ping <gateway-ip>` | Test gateway reachability |
| Check Internet | `ping 8.8.8.8` | Test external IP connectivity |
| Check DNS | `nslookup networkwalks.com` | Test domain resolution |
| Check Nmap | `nmap --version` | Display installed Nmap version |

Example commands using placeholders:

```bash
ip a
ping <gateway-ip>
ping 8.8.8.8
nslookup networkwalks.com
nmap --version
```

Use only the tests you actually performed, and record the real results in your documentation.

# 🐞 Problems Encountered & Solutions

Document the problems that occurred during your own setup and how you resolved them.

## Problem 1 – Network Connectivity

**Possible issue:** The virtual machine cannot access the network after its network settings are changed.

**Troubleshooting approach:**

1. Review the VirtualBox network adapter configuration.
2. Confirm that the correct NAT Network is selected.
3. Inspect the IP address and default gateway.
4. Test connectivity and DNS resolution separately.
5. Review the network connection settings if the problem continues.

## Problem 2 – Virtual Machine Startup

**Possible issue:** The virtual machine fails to start because of virtualization settings or resource constraints.

**Troubleshooting approach:**

1. Review the error message displayed by VirtualBox.
2. Check whether hardware virtualization is enabled when required.
3. Verify that sufficient memory is available.
4. Review the VM configuration and try starting it again.


# 💡 What I Learned

### 1. Virtualization

Learned how a hypervisor can run a separate operating system inside a virtual machine.

### 2. Virtual Networking

Developed an understanding of virtual network adapters and how NAT Network supports communication between connected virtual machines.

### 3. IP Configuration

Practiced inspecting IP addresses, gateways, subnet information, and DNS settings.

### 4. Connectivity Testing

Learned to use basic command-line tools to investigate network reachability and name resolution.

### 5. Snapshot Recovery

Understood how snapshots can help preserve a working baseline before future lab experiments.

### 6. Technical Documentation

Learned the importance of recording configuration details, test results, screenshots, and troubleshooting steps.

# 🔐 Security & Ethical Use

This laboratory is intended for educational purposes and authorized cybersecurity practice.

Security testing must only be conducted on systems that you own or have explicit permission to test. Do not scan, exploit, or access unauthorized systems.

# 🔗 Tools & Resources

- **7-Zip:** https://www.7-zip.org/download.html
- **VirtualBox:** https://www.virtualbox.org/wiki/Downloads
- **Kali Linux:** https://www.kali.org/get-kali/

# 👤 Author

**Mohit Sonawane**  
Cybersecurity Intern – NETWORKWALKS  
Batch B084B

**LinkedIn Post:** https://lnkd.in/p/dxM5aMsE

**GitHub Repository:** https://github.com/mohitsonawane21/NETWORKWALKS-MOHIT-WK1-PM1-CYBERSECURITY-LAB-SETUP

---

## 📌 Project Information

- **Program:** Cybersecurity at NETWORKWALKS
- **Week:** 01
- **Project:** Cybersecurity & Penetration-Testing Lab Setup
- **Batch:** B084B
- **Author:** Mohit Sonawane
- **Repository:** GitHub

## About

A virtual cybersecurity lab built with VirtualBox and Kali Linux to support cybersecurity learning, networking practice, and authorized security-testing exercises.
