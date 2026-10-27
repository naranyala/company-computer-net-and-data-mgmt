# Company Computer Networking and Data Management Catalog

A practical, business-focused reference for small-to-medium company IT support, systems administration, and digital operations.

This catalog is designed for the people who keep company technology working every day: help desk staff, desktop support technicians, IT administrators, office technology managers, network support engineers, and small-business IT teams.

The focus is not abstract theory alone. It is the real work of supporting end users, managing office networks, protecting company data, maintaining access rights, troubleshooting devices, and keeping operations reliable.

---

## Why this catalog matters

In a small or medium business, IT usually touches everything:

- user computers and printers
- office Wi‑Fi and internet connectivity
- servers and shared storage
- user accounts, email, and access rights
- cloud tools and remote access
- backups and business continuity
- security, patching, and endpoint health

When the IT environment is healthy, the business runs smoothly. When it breaks, the impact is immediate.

---

## Scope of the catalog

This repository covers the core areas of company IT support:

- networking and internet connectivity
- workstation and laptop support
- user identity and access management
- file storage and shared folders
- backup and disaster recovery
- endpoint and security hygiene
- troubleshooting and support workflow
- documentation and operational discipline

---

## Typical SMB IT environment

A small-to-medium business IT environment often includes:

- ISP internet connection and edge router
- firewall and secure gateway
- LAN switches and Wi‑Fi access points
- laptops, desktops, and mobile devices
- printers, scanners, and office equipment
- Active Directory or cloud identity platform
- file server or NAS storage
- backup appliance or cloud backup service
- SaaS tools such as email, document storage, CRM, and ticketing

---

## Core layers of a business IT system

| Layer | Purpose | Typical components |
| --- | --- | --- |
| Access layer | User connectivity | Wi‑Fi, LAN, VPN, printers, devices |
| Network layer | Routing and communication | switches, routers, firewalls, VLANs, ISP |
| Identity layer | Authentication and access | accounts, MFA, groups, permissions |
| Device layer | Workstations and endpoints | laptops, desktops, mobile devices, scanners |
| Data layer | Storage and file access | file servers, NAS, cloud drives, databases |
| Security layer | Protection and governance | patching, endpoint protection, access reviews |
| Operations layer | Maintenance and support | monitoring, tickets, backups, documentation |

---

## 1. Network fundamentals for company IT

### 1.1 Office network design

A basic office network typically includes:

- modem or ISP router
- firewall or security appliance
- core switch and access switches
- Wi‑Fi access points
- VLANs for guest, voice, management, or server traffic
- user endpoints
- shared services such as file servers and printers

### 1.2 Common networking concepts

#### IP addressing
An IP address identifies a device on a network.

Examples:
- `192.168.10.20`
- `10.0.0.15`

Support relevance:
- no valid IP often means DHCP or link issue
- duplicate IPs can break connectivity
- wrong subnet can isolate a device from the rest of the office

#### Subnet mask
Tells devices how to determine the local network from the host portion of an address.

#### Default gateway
Allows a device to reach other networks, including the internet.

#### DNS
Converts names like `fileserver` or `mail.company.com` into IP addresses.

Common symptoms of DNS problems:
- websites fail to load
- file servers cannot be reached by name
- apps cannot resolve internal services
- email may fail or appear intermittent

#### DHCP
Automatically assigns network details to clients.

Common issues:
- no IP lease issued
- rogue DHCP server on the network
- stale lease after network changes
- gateway or DNS assigned incorrectly

#### Router and firewall
The router connects local traffic to other networks. The firewall enforces policy for inbound and outbound traffic.

#### Switches and ports
Switches connect devices within a LAN and provide physical access points.

Common issues:
- broken patch cable
- disabled switch port
- wrong VLAN assignment
- loop or broadcast storm conditions

#### Wi‑Fi
Wireless connectivity is often the most frequent source of user complaints in offices.

Typical concerns:
- low signal strength
- dead zones
- channel overlap
- poor AP placement
- roaming issues
- guest network isolation problems

#### VLANs
VLANs separate traffic logically even when devices share the same physical switch.

Examples:
- management VLAN
- staff VLAN
- guest Wi‑Fi VLAN
- server VLAN
- voice VLAN

### 1.3 Connectivity troubleshooting checklist

When a user says “I can’t access the internet,” check:

- device is connected to Wi‑Fi or wired LAN
- IP address is valid
- gateway is reachable
- DNS answers correctly
- user is not using a blocked VPN route
- firewall is not blocking the connection
- ISP service is healthy

---

## 2. Endpoints and workstation support

Most day-to-day IT support revolves around endpoints.

### 2.1 Common endpoint categories

- desktops
- laptops
- tablets
- mobile phones
- printers
- scanners
- conference room hardware
- thin clients or kiosk devices

### 2.2 Typical desktop and laptop problems

- slow boot or startup
- application crashes
- drivers not working
- patching issues
- user profile corruption
- missing permissions
- storage space consumption
- malware or unexpected software installation

### 2.3 Printer support

Printers are a major source of office tickets.

Common issues:
- queue stuck
- printer offline
- wrong IP address or hostname
- driver mismatch
- print spooler failure
- switch port or Wi‑Fi connectivity issue

### 2.4 Mobile device support

Support often includes:

- email configuration
- MFA enrollment
- VPN setup
- mobile device management
- lost or stolen device process
- remote wipe and access revocation

---

## 3. Identity and access management

### 3.1 User identity basics

A user identity is how a person is recognized in the company’s digital systems.

Examples:
- Active Directory
- Microsoft Entra ID
- Google Workspace accounts
- local accounts
- service accounts

### 3.2 Onboarding

Typical onboarding steps:

- create account
- assign company email
- provide access to shared resources
- assign correct groups
- install required software
- configure VPN or remote access
- map printers and shared drives
- verify user is ready to work

### 3.3 Offboarding

Offboarding is critical for security:

- disable account
- revoke access to shared drives
- remove SaaS licenses
- transfer or archive data if required
- collect company equipment
- verify no lingering access remains

### 3.4 Permissions and groups

Permissions should be controlled and reviewed regularly.

Best practices:
- group-based access whenever possible
- least privilege approach
- periodic permission review
- document access approval
- remove stale rights after role changes

### 3.5 MFA and authentication support

Common support cases:
- approval not reached
- new phone or device enrollment
- app resets
- lockout due to repeated failed attempts
- user cannot access VPN or email after policy changes

---

## 4. Shared data and file management

### 4.1 Where company data usually lives

- file servers
- NAS devices
- department shared folders
- cloud storage such as OneDrive, SharePoint, Google Drive
- databases and business applications
- email archives and collaboration platforms

### 4.2 Shared folder design

A well-structured shared data model includes:

- HR and payroll folders
- finance and accounting data
- project and operational documents
- shared templates and forms
- archived records and retention storage

### 4.3 File permission model

Recommended approach:

- assign permissions through groups
- avoid over-broad access
- audit folders with sensitive data
- document who owns each share
- review access regularly

### 4.4 Support issues in data access

- user cannot open a folder
- file is read-only unexpectedly
- share mapping is broken
- permission inherited unexpectedly
- file server is offline or slow
- user has wrong department access

---

## 5. Backup, storage, and continuity

### 5.1 Backup fundamentals

Backups protect company data against:

- hardware failure
- ransomware or malware attacks
- accidental deletion
- software corruption
- user mistakes
- natural disasters or power outages

### 5.2 What to back up

Common business data to back up:

- file shares
- server data
- virtual machines
- databases
- email data
- cloud storage content
- endpoint data where required

### 5.3 Backup design questions

- What is being backed up?
- Where is it stored?
- How often does it run?
- How long is it retained?
- What happens if the backup target fails?
- Has a restore been tested recently?

### 5.4 Recovery objectives

- RPO: Recovery Point Objective — how much data loss is acceptable
- RTO: Recovery Time Objective — how quickly restoration must happen

### 5.5 Types of storage targets

- local NAS appliance
- offsite or cloud backup service
- external disk rotation
- virtualization backup tools
- SaaS retention tools

### 5.6 Disaster recovery

Disaster recovery planning includes:

- restoring failed servers
- recovering file shares
- re-establishing email and identity access
- restoring remote access and office connectivity
- validating business-critical systems first

---

## 6. Security basics for small and medium companies

SMBs are often targeted because they may have weaker defenses and fewer specialized staff.

### 6.1 Basic security controls

- strong password policies
- MFA on critical systems
- patching and software updates
- antivirus and endpoint protection
- user access review
- secure Wi‑Fi settings
- least privilege access
- backup verification
- logging and alert review

### 6.2 Common security issues

- phishing attempts
- password reuse
- stale accounts
- unpatched operating systems
- local admin rights for too many users
- insecure remote access
- poor backup testing
- employees downloading unapproved software

### 6.3 Security operations checklist

- verify user access after role changes
- monitor alerts for suspicious activity
- review firewall logs periodically
- check endpoint protection status
- confirm backups succeed and are restorable
- verify patch status on critical devices

---

## 7. Servers, virtualization, and infrastructure basics

Even small companies may run basic server infrastructure.

### 7.1 Standard server roles

- domain controller or identity service
- file server
- print server
- database server
- application server
- backup server
- virtual machine host

### 7.2 Virtualization concepts

Virtual machines allow a business to run several systems on fewer physical servers.

Support tasks include:

- VM health checks
- storage usage review
- snapshot management
- host resource monitoring
- VM backup and restore verification

### 7.3 Server health checks

- CPU utilization
- RAM usage
- storage capacity
- service health
- event logs
- uptime and unexpected restarts

---

## 8. Cloud services and SaaS in company IT

Modern businesses rely heavily on cloud tools.

### 8.1 Common cloud services

- Microsoft 365 / Outlook / SharePoint / OneDrive
- Google Workspace
- cloud storage solutions
- file collaboration tools
- customer relationship systems
- ticketing and project systems

### 8.2 Cloud support concerns

- failed sync
- storage quotas
- stale sharing links
- MFA or sign-in issues
- permission mismatches
- downtime or service outages

### 8.3 Hybrid environments

Many companies use both local infrastructure and cloud services.

Examples:
- local file server + cloud email
- Azure AD / Entra ID with local domain services
- on-prem login with cloud productivity apps
- remote access through VPN and cloud identity tools

---

## 9. Monitoring, maintenance, and proactive support

A reliable IT environment is not just reactive. It includes proactive monitoring.

### 9.1 Monitoring activities

- uptime checks
- disk usage monitoring
- backup success verification
- firewall event review
- internet connectivity checks
- endpoint health checks
- certificate expiry monitoring
- service availability monitoring

### 9.2 Maintenance windows

Regular maintenance includes:

- patching and updates
- reboot scheduling for devices or services
- backup validation
- access review
- hardware health review
- software inventory cleanup

### 9.3 Preventive support mindset

The best IT teams reduce ticket volume by doing small things early:

- keep devices updated
- review storage before it fills up
- monitor backups daily
- document changes
- confirm remote access after policy updates
- review network health before users experience outages

---

## 10. Help desk and IT support operations

### 10.1 Ticketing workflow

A basic support workflow should include:

- ticket creation
- issue classification
- owner assignment
- triage and investigation
- corrective actions
- user communication
- validation of resolution
- closure and documentation

### 10.2 Triage questions

- One user or multiple users?
- One office or multiple locations?
- One service or many services?
- Was there a recent change?
- Is it an identity, device, network, or data issue?

### 10.3 Documentation best practices

Good notes include:

- date and time
- affected user and device
- location and office/site
- issue description
- troubleshooting steps taken
- findings and root cause
- final fix
- validation evidence

---

## 11. Change management and governance

### 11.1 Change control

Every significant change should be documented.

Examples:
- firewall update
- switch replacement
- Wi‑Fi configuration change
- server patching
- user permission change
- backup policy change

Recommended change record:

- reason for change
- who approved it
- when it happened
- expected impact
- rollback plan
- verification after change

### 11.2 Governance basics

A business should maintain:

- IT asset inventory
- device ownership records
- network documentation
- backup policy and restore test history
- permission review schedule
- contact list for critical vendors and providers

---

## 12. Asset management and lifecycle

### 12.1 Inventory should include

- device name
- owner
- department
- location
- serial number
- model
- warranty
- purchase date
- software version
- support status

### 12.2 Lifecycle planning

Businesses should plan for:

- computer replacement cycles
- printer replacement
- UPS or power protection checks
- network equipment refresh
- storage upgrade planning
- software renewal dates

---

## 13. Remote access and business continuity

### 13.1 VPN and remote support

Remote troubleshooting is essential for modern IT support.

Common remote support tasks:

- VPN diagnosis
- device remote assistance
- cloud service sign-in issues
- workstation remote management
- firewall and route validation for remote users

### 13.2 Business continuity ideas

Support teams should think about:

- access to critical services during outage
- emergency communication method
- remote work readiness
- offline workarounds for essential tasks
- backup restore testing before a real incident

---

## 14. Common IT support scenarios

### User cannot access the internet
Check:

- Wi‑Fi or cable connection
- IP address and subnet
- gateway reachability
- DNS resolution
- ISP or outage issue
- firewall or VPN blocking traffic

### User cannot reach file share
Check:

- account is active
- file server is online
- DNS resolves the share name correctly
- share permissions are correct
- VPN is connected if remote
- mapping or drive letter is valid

### Printer is offline
Check:

- printer IP is valid
- cable or wireless connection is healthy
- queue is stuck
- print server is healthy
- printer driver matches installed version
- switch port status is stable

### New employee cannot work on day one
Check:

- account created and active
- email and identity access configured
- correct group membership
- device is enrolled or domain joined
- required software installed
- printer and shared drive access assigned

### Backup failed overnight
Check:

- storage target free space
- connection to backup target
- credentials valid
- backup logs for failed job
- retention policy and schedule
- restore validation status

### VPN fails for remote user
Check:

- MFA status
- VPN profile or client version
- certificate validity
- route or firewall policy
- service outage or endpoint issue

---

## 15. Troubleshooting workflow

A disciplined troubleshooting approach reduces guesswork.

### Step 1: Define the symptom
Ask:

- what exact problem is occurring?
- who is affected?
- when did it start?
- what changed recently?

### Step 2: Check the basics

- power and physical connectivity
- network cable or Wi‑Fi state
- valid IP assignment
- gateway and DNS status
- account status and permissions
- backup or service health

### Step 3: Reduce the scope

- is it one user or many?
- is it one office or all locations?
- is it local, remote, or cloud-based?

### Step 4: Validate likely causes

Useful tools:

- `ping`
- `tracert` / `traceroute`
- `nslookup` or `dig`
- `ipconfig /all`
- `arp -a`
- firewall logs
- switch port status
- event logs
- backup logs

### Step 5: Apply the smallest correct fix

Avoid broad changes when a focused repair is enough.

### Step 6: Verify and document

Before closing a ticket, confirm:

- issue is resolved
- user can access the required service
- no new problems were caused
- the change was logged

---

## 16. Common IT tools and commands

### Windows

- `ipconfig /all`
- `ping <hostname>`
- `tracert <hostname>`
- `nslookup <domain>`
- `arp -a`
- `netstat -an`
- `route print`
- `systeminfo`
- `tasklist`
- `services.msc`
- `diskpart`
- `getmac`

### Linux / Unix

- `ip addr`
- `ifconfig`
- `ping`
- `traceroute`
- `dig`
- `ss -tulpn`
- `df -h`
- `du -sh`
- `mount`
- `journalctl`

### Operational checks

- verify backup status and logs
- inspect failed jobs
- check disk utilization and room for growth
- confirm patching status
- review access logs and firewall events
- validate restore tests

---

## 17. Frequently missing but important topics

These are the areas that often make a README truly comprehensive for SMB IT support:

- cabling and physical patching basics
- UPS and power protection
- rack and server room organization
- vendor and ISP escalation process
- procurement and equipment lifecycle
- license tracking and software compliance
- remote support and endpoint management
- SaaS administration and user provisioning
- backup restore testing and validation
- cybersecurity awareness training
- audit readiness and access reviews
- escalation matrix and ownership model
- emergency communication plan for outages
- user communication templates for incidents

These are the details that turn a basic technology list into a realistic operational catalog.

---

## 18. IT support glossary

### Active Directory
A directory service used to manage users, computers, and permissions in Windows environments.

### DNS
Domain Name System; resolves names into IP addresses.

### DHCP
Dynamic Host Configuration Protocol; automatically assigns network settings.

### VLAN
Virtual local area network; logically separates traffic inside a network.

### Firewall
A network control that filters traffic based on policy.

### NAS
Network-attached storage used for shared file access.

### SAN
Storage area network for block-based storage used by servers and apps.

### VPN
Virtual private network for secure remote or inter-site connectivity.

### MFA
Multi-factor authentication; adds an additional sign-in verification step.

### RPO
Recovery Point Objective; acceptable loss of data.

### RTO
Recovery Time Objective; acceptable recovery time.

### CMDB
Configuration management database; system inventory and configuration tracking.

### Ticket
A tracked support request or incident record.

### Patch
A software update that fixes defects or closes vulnerabilities.

---

## 19. Learning roadmap for business IT support

### Beginner level

- networking basics
- IP addressing and DHCP
- DNS and basic routing
- printer and desktop support
- file share permissions and user lifecycle

### Intermediate level

- Wi‑Fi troubleshooting
- firewall basics
- Active Directory or cloud identity
- backup and restore fundamentals
- VPN support
- endpoint security

### Advanced level

- virtualization and storage design
- network segmentation and VLAN planning
- patching automation
- monitoring and alerting
- business continuity planning
- incident response coordination

---

## 20. Recommended SMB support checklist

Use this as a practical operating checklist:

- network and internet connectivity verified
- DHCP and DNS healthy
- user account active and permissions correct
- file access and shared storage available
- endpoint patched and protected
- backup status confirmed
- change documented and approved
- issue verified as resolved before closure

---

## 21. Final principle: support with structure

The most effective IT support teams are not just reactive technicians. They are structured problem solvers who understand:

- how the network works
- how users access business systems
- how files and backups are protected
- how identity and permissions affect productivity
- how to verify a fix before closing a ticket
- how to document and improve the environment over time

This is the difference between ad hoc troubleshooting and reliable business technology operations.

---

## 22. Summary

Company computer networking and data management are foundational capabilities in modern business operations.

For a small-to-medium business, the real goal is to maintain:

- stable connectivity
- reliable endpoint support
- correct user access
- protected and accessible data
- backup and recovery readiness
- secure and well-managed business systems

This catalog is intended to serve as a practical, detailed reference for that work.

---

## 23. Suggested future repository sections

To make this project even richer, the next sections could include:

- network diagram examples
- troubleshooting decision tree
- common SMB hardware inventory spreadsheet
- onboarding checklist for new employees
- offboarding checklist for leaving staff
- backup validation checklist
- security hygiene checklist
- change log template
- support ticket template
- disaster recovery planning template

These additions would turn this repository into a true operational playbook for company IT support.

