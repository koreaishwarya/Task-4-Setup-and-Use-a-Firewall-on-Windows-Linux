# Task 4: Set up and Use a Firewall on Windows/Linux

## Overview

This project demonstrates the configuration and testing of basic firewall rules using Windows Defender Firewall and UFW (Uncomplicated Firewall) on Linux. The objective is to understand how firewalls control network traffic by allowing or blocking connections based on predefined security rules.

## Objective

* Configure firewall rules to allow or block network traffic.
* Block inbound traffic on a specific port (Port 23 - Telnet).
* Allow SSH traffic on Linux (Port 22).
* Test firewall rules and verify their effectiveness.
* Understand the role of firewalls in network security.

## Tools Used

* Windows Defender Firewall
* UFW (Uncomplicated Firewall)
* Command Prompt / PowerShell
* Linux Terminal

## Steps Performed

### Windows Firewall

1. Opened Windows Defender Firewall with Advanced Security.
2. Reviewed existing inbound firewall rules.
3. Created a new inbound rule to block TCP Port 23 (Telnet).
4. Tested connectivity to confirm the port was blocked.
5. Removed the test rule to restore the original configuration.

### Linux UFW Firewall

1. Checked the current firewall status using UFW.
2. Added a rule to block TCP Port 23 (Telnet).
3. Added a rule to allow TCP Port 22 (SSH).
4. Verified active firewall rules.
5. Tested connectivity to the blocked port.
6. Removed the test rule after verification.

## Commands Used

### Check Firewall Status

```bash
sudo ufw status verbose
```

### Block Telnet Port 23

```bash
sudo ufw deny 23/tcp
```

### Allow SSH Port 22

```bash
sudo ufw allow 22/tcp
```

### View Active Rules

```bash
sudo ufw status numbered
```

### Delete a Rule

```bash
sudo ufw delete <rule_number>
```

## Results

| Rule             | Action    |
| ---------------- | --------- |
| Port 23 (Telnet) | Blocked   |
| Port 22 (SSH)    | Allowed   |
| Existing Rules   | Unchanged |

The firewall successfully blocked unauthorized Telnet traffic while allowing secure SSH connections.

## Key Learnings

* Firewalls are essential for controlling network access.
* Rules can be configured to allow or deny traffic on specific ports.
* Blocking unused or insecure services reduces attack surfaces.
* SSH should be explicitly allowed when remote administration is required.
* Regular firewall monitoring enhances system security.

## Conclusion

This task provided hands-on experience with configuring and managing firewall rules on Windows and Linux systems. By blocking Telnet traffic and allowing SSH access, the exercise demonstrated how firewalls protect systems from unauthorized network access and improve overall cybersecurity.
