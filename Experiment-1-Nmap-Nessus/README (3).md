# Experiment 1: Scanning for Vulnerabilities using Nmap and Nessus

## Objective

To use Nmap to identify open ports and Nessus to scan for known vulnerabilities on a test machine.

## Procedure

### Step 1: Configure the Kali Linux and Metasploitable machines

Open the Kali Linux virtual machine as the attacker machine and the Metasploitable virtual machine as the target machine. Configure the network adapter of both virtual machines to Host-only Adapter so that they can communicate with each other within the isolated lab network.

![Step 1 Screenshot](images/Step_1.jpeg)

### Step 2: Check the IP address and verify connectivity
# Commands used :
```bash
ifconfig
ping <Metasploitable-IP>
```
![Step 2 Screenshot](images/Step_2.jpeg)


### Step 3: Perform a basic Nmap scan

# Commands used :
```bash
nmap <Metasploitable-IP>
```
The scan output can be used to understand the exposed services on the target.

![Step 3 Screenshot](images/Step_3.jpeg)

### Step 4: Download Nessus

Download the Nessus vulnerability scanner required for performing vulnerability assessment of the target machine.

![Step 4 Screenshot](images/Step_4.jpeg)

### Step 5: Install and configure Nessus

Install Nessus on the system and complete the required initial setup. After installation, open the Nessus web interface and prepare it for vulnerability scanning.

![Step 5 Screenshot](images/Step_5.jpeg)

### Step 6: Scan the target and review the vulnerabilities

Configure Nessus to scan the Metasploitable target and review the scan results after completion. The dashboard displays the vulnerabilities detected on the target along with their severity levels.

![Step 6 Screenshot](images/Step_6.jpeg)

## Result

The experiment was successfully performed using Nmap and Nessus. Nmap was used to identify the open ports and services on the Metasploitable target, while Nessus was used to assess the target for known vulnerabilities and display the detected security issues.
