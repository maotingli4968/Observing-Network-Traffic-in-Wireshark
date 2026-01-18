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

<p align="center">
  <img src="https://github.com/user-attachments/assets/9d426fdb-3b20-4dab-8a51-8f693fee9a5b"
       alt="image"
       width="700" />
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/7cc9d3ce-10f2-42e9-bf73-3a7ce99e6ceb"
       alt="image"
       width="700" />
</p>


- Replace 10.0.0.5 with the Linux VM’s private IP.
- Accept the security prompt with <b>yes</b>, then enter the password.
-  This generates SSH traffic, which can be observed in Wireshark.

<p align="center">
  <img src="https://github.com/user-attachments/assets/030fd0c7-7126-43e2-87d3-d00a12f4faa8"
       alt="image"
       width="700" />
</p>


<b>Run Commands Over SSH</b>

Once connected, your prompt changes to the Linux VM. Run commands such as:

- id → Shows user information
 <p align="center">
  <img src="https://github.com/user-attachments/assets/0229a5f1-7cf9-4239-9503-b48f4c6003cb"
       alt="image"
       width="700" />
</p>

- hostname → Displays the Linux VM hostname
<p align="center">
  <img src="https://github.com/user-attachments/assets/15dec095-ffd6-4dc0-bb13-663dffedf94f"
       alt="image"
       width="700" />
</p>

- uname -a → Prints OS details
  <p align="center">
  <img width="975" height="42" alt="image" src="https://github.com/user-attachments/assets/e6ea39fa-dbe3-4679-8b23-1ab76002fe23" />

       
- Each keystroke and command generates SSH traffic.
- In Wireshark, you can see TCP packets with source/destination ports (random port ↔ 22).
- The payload is encrypted and unreadable, demonstrating SSH security.

<img width="975" height="199" alt="image" src="https://github.com/user-attachments/assets/daf6b88e-90cd-4abe-80ff-22ea60e98030" />

<b>Exit SSH Session</b> 

To end the session, type:
 
<img width="725" height="172" alt="image" src="https://github.com/user-attachments/assets/9c06d789-f524-4b9b-bb5a-7d5298365b6a" />

This sends a TCP reset packet, closing the connection. The prompt returns to the Windows VM, and Wireshark shows the termination traffic. 

<img width="975" height="88" alt="image" src="https://github.com/user-attachments/assets/ff57e1f5-698c-4684-8707-9c69d58dc12e" />

<b>Observe DNS Traffic</b>

Set the Wireshark filter to dns. In PowerShell, run:

```powershell
nslookup disney.com
nslookup pixar.com
```

Wireshark captures the DNS requests and replies, showing how hostnames are resolved to IP addresses. DNS uses UDP port 53

<img width="975" height="331" alt="image" src="https://github.com/user-attachments/assets/1342f958-0e3b-4c86-a700-46f5f91e1106" />

















  














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
