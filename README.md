# Local Nmap Scanning & Pentesting Lab Setup (WSL2 + Docker)

This repository details the configuration steps to set up a sandboxed penetration testing lab on a Windows host using Windows Subsystem for Linux (WSL 2) running Kali Linux as the attacking machine and Docker to host the target: Metasploitable2.

Using a dedicated Docker bridge network (`pentest-net`), we ensure the vulnerable target container is isolated from the Windows host while remaining fully accessible to the Kali Linux tools.

## Prerequisites

- Windows 10/11 with WSL 2 enabled.
- Kali Linux WSL instance installed.
- Sudo/Root privileges within Kali Linux.

---

## Lab Setup Procedure

Follow these steps within your Kali Linux terminal to provision the lab.

### Step 1: Install and Initialize Docker in WSL 2

Update your Kali package index and install Docker, alongside Nmap for the attacking toolset. Ensure the Docker daemon is running.

```bash
# Update Kali package index and install required tools
sudo apt update && sudo apt install -y docker.io nmap

# Start the Docker daemon
sudo service docker start