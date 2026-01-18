<p align="center">
<img width="1605" height="624" alt="image" src="https://github.com/user-attachments/assets/7efc7e92-7b7b-419f-9b85-712d037a2070" />
/>
</p>

<h1>Remote Desktop – Observing Network Traffic in Wireshark</h1>
This tutorial outlines the process of observing network traffic in Wireshark.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines / Compute)
- Remote Desktop Protocol (RDP)
- WireShark (Protocol Analyzer / Packet Sniffer)


<h2>Operating Systems Used </h2>
- Windows 10 Pro (Remote VM)
- Ubuntu Linux (Remote VM)


<h2>Post-Install Configuration Objectives</h2>

- Two running virtual machines created in Lab 2 Part 1:
    - Windows 10 VM
    - Ubuntu Linux VM

- Both VMs must be powered on and accessible in the Azure Portal
- Public IP address of the Windows VM for RDP connection
- Private IP address of the Linux VM for SSH testing
- WireShark installed on the Windows VM

<h2>Configuration Steps</h2>
 <b>Log Back Into the Windows VM</b>

- Ensure both VMs are running in the Azure Portal.
- Copy the public IP of the Windows VM.
- Open Remote Desktop (Windows built-in or Microsoft Remote Desktop for Mac).
- Reconnect using your credentials

<b>Start Wireshark and Capture SSH Traffic</b>

- Inside the Windows VM, open Wireshark and select the Ethernet adapter (not loopback).
- Start a packet capture and filter by typing ssh to display only SSH traffic.
- SSH typically uses TCP port 22



<p align="center">
  <img src="https://github.com/user-attachments/assets/86c4c421-5bcb-4e16-8612-40071551ce9a"
       alt="image"
       width="700" />
</p>


<b>Connect to Linux VM via SSH</b>

Open PowerShell in the Windows VM and connect to the Linux VM using SSH:

<b>ssh labuser@10.0.0.5</b>








Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
