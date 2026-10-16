# Experiment 4: Firewall and IDS Setup

## Objective

To configure firewall rules using **pfSense** and enable intrusion detection using **Snort** to monitor network traffic and identify suspicious activities.

## Procedure

### Step 1: Configure the pfSense network

Start the pfSense virtual machine and verify the WAN and LAN interface IP addresses. Confirm that the LAN interface is configured and accessible from the lab network.

![Step 1 Screenshot](images/ss1.png.jpeg)

### Step 2: Verify network connectivity and identify the target

Use `ifconfig` on Kali Linux to identify its network interface and IP address. Ping the target machine and perform an Nmap scan to check connectivity and identify open ports and services.

# Commands used :
```bash
ifconfig
ping <Target-IP> -c 4
nmap <Target-IP>
```

![Step 2 Screenshot](images/ss2.png.jpeg)

### Step 3: Configure firewall rules in pfSense

Log in to the pfSense web interface and navigate to **Firewall → Rules → LAN**. Configure firewall rules to allow required traffic, such as HTTP, HTTPS, and DNS, and block other traffic according to the lab requirements.

![Step 3 Screenshot](images/ss3.png.jpeg)

### Step 4: Enable Snort on the LAN interface

Open **Services → Snort → Interfaces** in pfSense. Configure Snort on the LAN interface and verify that its status indicates that the service is running.

![Step 4 Screenshot](images/ss4.png.jpeg)

### Step 5: Generate network traffic and check detection

Generate network traffic from Kali Linux by pinging the target machine. Perform the relevant connectivity tests and observe the traffic monitored by the configured security tools.

# Commands used :
```bash
nmap -p 1-1000 <Target-IP>
ping <Target-IP>
```

![Step 5 Screenshot](images/ss5.png.jpeg)

### Step 6: Examine Snort alerts

Navigate to **Services → Snort → Alerts** in pfSense. Review the alert log to identify recorded events, including ICMP ping detection alerts generated during the test.

![Step 6 Screenshot](images/ss6.png.jpeg)

## Result

The experiment demonstrated firewall rule configuration using **pfSense** and network traffic monitoring using **Snort**, with ICMP ping detection alerts observed in the alert log.
