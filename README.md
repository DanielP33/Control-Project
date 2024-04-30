# Control Project
This project is a comprehensive control system deployed across multiple AWS instances, featuring Ubuntu-based Control Center overseeing Debian, Red Hat Linux, Windows Server 2022, and Windows 11 Client machines, each configured with specific security groups, services, and platforms tailored to their respective roles.
Note: They are all in the save availability zone.

## Control Center

### Operating System: 
- Ubuntu

### Platform: 
- AWS

### Security Group:
**Inbound:**
- RDP (3389) from my IP address
- SSH (22) from my IP address

**Outbound:**
- All traffic Anywhere.

### Elastic IP: 
- 34.193.213.145

### Machine Type: 
- m5.large

### Storage: 
- 30

### Base Services:
- New Relic
- Wazuh
- UPTIME ROBOT
- PagerDuty
- Splunk

## Debian Linux 1

### Operating System: 
- Debian

### Platform: 
- AWS

### Security Group:
**Inbound:**
- SSH (22) from my IP address
- SSH (22) from 172.31.19.15 (Control Machine)

**Outbound:**
- All traffic Anywhere.

### Elastic IP: 
- None

### Machine Type: 
- t2.micro

### Storage: 
- 30G

### Base Services:
- HTTP
- NGINX

## Red Hat Linux 1

### Operating System: 
- Red Hat

### Platform: 
- AWS

### Security Group:
**Inbound:**
- SSH (22) from my IP address
- SSH (22) from 172.31.19.15 (Control Machine)

**Outbound:**
- All traffic Anywhere.

### Elastic IP: 
- None

### Machine Type: 
- t2.micro

### Storage: 
- 30G

### Base Services:
- HTTPS
- APACHE

## Windows Server 2022

### Operating System: 
- Windows Server 2022

### Platform: 
- AWS

### Security Group:
**Inbound:**
- RDP (3389) from my IP address

**Outbound:**
- All traffic Anywhere.

### Elastic IP: 
- None

### Machine Type: 
- c5.large

### Storage: 
- 30G

### Base Services:
- HTTP
- HTTPS
- IIS

## Windows 11 Client

### Operating System: 
- Windows 11

### Platform: 
- AWS

### Security Group:
**Inbound:**
- RDP (3389) from my IP address

**Outbound:**
- All traffic Anywhere.

### Elastic IP: 
- None

### Machine Type: 
- c5.large

### Storage: 
- 64G

### Base Services:
- None
