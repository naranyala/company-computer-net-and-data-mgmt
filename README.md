# Company Computer Networking and Data Management Catalog

A practical, detailed guide for IT support, systems administration, and digital operations in small-to-medium businesses (SMBs). This catalog is designed around the real-world responsibilities of keeping a company’s computers, network, users, and company data available, secure, and operational.

This is not just a theory document. It is a working knowledge base for:

- help desk technicians
- desktop support specialists
- network support engineers
- IT administrators
- junior system administrators
- office technology managers
- small-business IT operations teams

---

## 1. Purpose of this catalog

This repository focuses on the technologies and processes that keep a business running every day:

- office and remote networking
- endpoint protection and support
- user identity and access management
- file storage and shared data access
- backups, restore, and business continuity
- security basics for SMB environments
- support operations and troubleshooting

The aim is to provide a useful manual for solving the most common IT problems in a small-to-medium company without relying on vendor-specific memorization.

---

## 2. Why small-to-medium company IT is different

Unlike large enterprises, SMB environments often have:

- fewer IT specialists
- broader responsibilities for each technician
- mixed hardware and software vendors
- limited dedicated networking teams
- a need to support users across departments quickly
- tighter operational budgets
- greater reliance on practical troubleshooting and documentation

This means a strong SMB IT professional must be flexible and understand the full stack:

- physical networking
- desktop and laptop support
- identity and permissions
- file sharing and storage
- backups and disaster recovery
- cloud services and remote access
- security hygiene and escalation paths

---

## 3. The IT support model in a business environment

A typical SMB IT environment includes several layers working together:

| Layer | Description | Examples |
| --- | --- | --- |
| Access layer | User connectivity to the company systems | Wi‑Fi, Ethernet, VPN, printers, laptops |
| Network layer | Company communication backbone | switches, routers, firewalls, VLANs, ISP links |
| Identity layer | Who a user is and what they can do | AD, Entra ID, local accounts, MFA, group policy |
| Device layer | User hardware and support endpoints | desktops, laptops, phones, tablets, scanners |
| Data layer | Where business information lives | file servers, NAS, cloud shares, databases |
| Security layer | Protection and governance | endpoint protection, MFA, updates, access reviews |
| Operations layer | Continuous support and maintenance | ticketing, monitoring, backups, patching, documentation |

A stable company IT environment balances all of these layers. A problem in one layer can create symptoms in another.

---

## 4. Company network fundamentals

### 4.1 Network topologies used in SMBs

Most small businesses use a simplified version of a standard enterprise design:

- internet connection from ISP
- firewall or secure gateway
- one or more switches
- Wi‑Fi access points for office mobility
- VLANs for segmentation
- servers or hosted services for files, identity, and apps
- remote access through VPN or cloud secure access

Typical SMB layouts:

- single-site office network
- branch office + headquarters
- small office with cloud-first services
- hybrid model: local servers + Microsoft 365 / Google Workspace / SaaS apps

### 4.2 Common network components

#### Internet edge
The internet connection is usually where all traffic enters and exits the business.

Support concerns:
- ISP outages
- bandwidth saturation
- poor latency
- NAT and port forwarding issues
- firewall rule changes affecting business apps

#### Firewall
A firewall controls traffic between trusted and untrusted networks.

Common SMB tasks:
- open inbound rules for business applications
- allow VPN remote access
- review recent changes after outages
- ensure blocked ports are intentional
- monitor suspicious activity

#### Switches
Switches connect devices on the office LAN.

Common issues:
- bad cable or connector
- port disabled or failed
- VLAN mismatch
- spanning-tree or loop issues
- switch resource exhaustion

#### Access points and Wi‑Fi
Wi‑Fi is often the most frequent source of user complaints.

Typical concerns:
- weak signal in some office areas
- overlap or channel interference
- roaming issues between APs
- guest network separation
- unsupported devices or stale profiles
- poor placement or missing coverage planning

#### DHCP and DNS
These are essentials for making a network function without manual static configuration.

DHCP provides:
- IP address
- subnet mask
- default gateway
- DNS server addresses

DNS resolves:
- local names like `fileserver`
- mail systems
- internal applications
- internet names used by users

### 4.3 IP, subnet, and route basics

#### IP address
An IP address identifies a device on a network.

Examples:
- `192.168.10.15`
- `10.0.0.42`
- `172.16.5.10`

#### Subnet mask
A subnet mask separates the network portion and host portion of an IP address.

This matters because:
- devices on the same subnet can communicate directly
- devices on different subnets require a router or gateway
- wrong subnet values cause communication problems that can look random

#### Gateway
The default gateway allows traffic to leave the local LAN for the internet or another network.

#### Routing
Routing allows devices to find the path to other destinations. In SMBs, this often happens automatically with simple router/firewall setups.

---

## 5. Data management in a company environment

Data management is the discipline of making sure information is:

- available when needed
- protected from loss
- shared only with the right people
- retained according to business needs
- recoverable in the event of failure

### 5.1 Where business data lives

In SMBs, business data may be stored in:

- local workstations
- file servers at the office
- NAS devices
- cloud storage platforms
- SaaS applications
- database servers
- backups and archives

### 5.2 Shared file access

File systems are often the most important business data layer. They support:

- department folders
- project files
- finance and HR data
- accounting records
- documentation and templates
- operations files used by staff daily

Common support tasks:
- adding a new shared folder
- reviewing permissions after role changes
- troubleshooting missing drive mappings
- resolving locked files or stale access links
- verifying storage capacity before outages

### 5.3 File permissions and least privilege

A big part of IT support is access management. Staff should only have the permissions they actually need.

Good model:
- groups rather than individual permissions where possible
- least privilege
- regular permission review
- clear ownership of shared folders
- documented approval for access changes

Bad model:
- broad access for convenience
- everyone in a shared admin group
- stale accounts keeping access after exit
- unmanaged permissions on critical folders

### 5.4 NAS and SAN

#### NAS
A NAS is a file-based storage appliance connected over the network.

Typical uses:
- shared user files
- backups
- media storage
- departmental file repositories
- internal server backups

#### SAN
A SAN is usually used for block-level storage, often by servers and VM hosts.

Typical uses:
- databases
- virtual machine storage
- enterprise applications
- high-availability storage backends

---

## 6. Identity and access management

Identity is central to company IT. If identity is wrong, users cannot do their work even when the network itself is healthy.

### 6.1 User lifecycle management

Support teams usually manage the full employee lifecycle:

- onboarding
- role changes
- access reviews
- offboarding

Onboarding examples:
- create account
- assign group membership
- set up email and portal access
- provision VPN rights
- install software or assign standard image
- map shared drives and printers

Offboarding examples:
- disable account
- remove device access
- revoke group permissions
- remove cloud tools
- recover company property
- archive or transfer data when necessary

### 6.2 Authentication and MFA

Authentication verifies the user is who they say they are.

Common SMB tools:
- Microsoft Entra ID / Azure AD
- Active Directory
- Google Workspace identity services
- local accounts on device and service layers

MFA is often required for:
- remote access
- admin accounts
- cloud email
- VPN
- finance and HR systems

Support issues include:
- lost phone or stale device enrollment
- users not receiving approval prompts
- MFA lockout after policy changes
- authenticator app setup errors

### 6.3 Groups and role-based access control

Role-based access control (RBAC) reduces complexity and risk.

Examples:
- All Staff
- Accounting Team
- HR Team
- IT Admins
- Managers
- Site A Users

When access is assigned properly, support becomes much easier.

---

## 7. Endpoint support and device lifecycle

The endpoint is the user-facing part of IT support. It includes laptops, desktops, mobile devices, printers, scanners, and conference hardware.

### 7.1 Device inventory

A useful SMB environment tracks:

- device name
- owner
- department
- location
- model and serial
- warranty status
- OS version
- software installed
- support status

This matters for replacements, troubleshooting, asset audits, and security verification.

### 7.2 Workstations and laptops

Common issues:
- slow startup
- software conflicts
- driver issues
- login profile corruption
- patching delays
- hardware failures
- malware or unwanted software

### 7.3 Printers and scanners

Printers are often overlooked but are a major part of business operations.

Typical support topics:
- queue stuck
- wrong IP assignment
- driver mismatch
- print spooler issues
- offline status after port changes
- shared printer configuration

### 7.4 Mobile devices

SMB support often includes:
- company phones
- tablets
- employee personal devices with BYOD policy
- email clients
- MDM enrollment
- device access restrictions

---

## 8. Backup, restore, and business continuity

A company cannot function reliably without backup and recovery planning.

### 8.1 Backup fundamentals

Backups protect against:
- ransomware
- accidental deletion
- hardware failure
- software corruption
- user mistakes
- power failure or environmental issues

Good backup design includes:
- what to back up
- where it is stored
- how often it runs
- how long it is retained
- whether it is encrypted
- whether restores are tested regularly

### 8.2 Recovery metrics

- RPO: Recovery Point Objective — the amount of data loss acceptable
- RTO: Recovery Time Objective — how quickly recovery must happen

These two values guide backup frequency and recovery process design.

### 8.3 Backup targets

Typical targets:
- local NAS or appliance
- cloud backup service
- external disk rotation
- virtual machine backup tools
- SaaS data backup services

### 8.4 Disaster recovery

A small business disaster recovery plan may include:
- restoring a failed server
- re-establishing Wi‑Fi connectivity
- re-creating user accounts and group access
- restoring shared data drives
- reconnecting VPN or remote access
- restoring email and core SaaS tools

The key is to prioritize business-critical services first.

---

## 9. Security for small and medium businesses

Security is not “just for large companies.” SMBs are often targeted because they may have weaker defenses and more limited IT resources.

### 9.1 Essential controls

- strong password policy or passkeys
- MFA for admin and remote access
- endpoint protection
- patch management
- software inventory
- user access reviews
- secure remote access with policy checks
- backup verification
- monitoring and alerting

### 9.2 Common threats

- phishing emails
- password reuse
- stolen credentials
- ransomware attacks
- unpatched devices
- unauthorized software installs
- stale user accounts
- public Wi‑Fi misuse

### 9.3 Security operations for SMBs

Even in smaller businesses, a limited but consistent process helps:

- verify alerts quickly
- isolate compromised systems
- disable suspicious accounts
- review recent changes
- preserve evidence before cleanup
- document lessons learned

---

## 10. IT support operations and service culture

IT support in a small or medium company is not only about fixing technical issues. It is also about keeping people productive and maintaining trust.

### 10.1 Ticketing and triage

Common triage questions:
- one user or many users?
- one site or several?
- is the problem local or remote?
- is it a network, identity, endpoint, or data issue?
- what changed recently?

### 10.2 Documentation

Good IT support requires clear documentation.

A solid note should include:
- date and time
- affected user and device
- location
- symptom or error
- troubleshooting steps
- outcome
- any configuration or access changes

This helps with repeat issues and reduces repeated effort.

### 10.3 SLAs and priorities

Small businesses may not always have formal SLAs, but they still need prioritization:

- critical operations and security incidents first
- executive or finance systems next
- office productivity tools after that
- non-urgent requests later

### 10.4 Change management

Any system change should ideally include:
- reason for change
- who approved it
- expected impact
- rollback or fallback plan
- verification after deployment

---

## 11. Common small-business IT scenarios

### 11.1 User cannot access the internet

Check:
- Wi‑Fi or cable connected
- valid IP address assigned
- DHCP working
- gateway reachable
- DNS answering correctly
- firewall rule blocking traffic
- ISP or upstream outage

### 11.2 User cannot reach company file share

Check:
- account is active
- share permissions are correct
- mapping is valid
- network path is available
- DNS resolves the file server
- VPN is connected for remote users

### 11.3 Printer shows offline

Check:
- printer has valid IP or hostname
- network cable or Wi‑Fi signal is stable
- queue is stuck
- driver is compatible
- print server or print spooler is healthy
- switch port is not disabled

### 11.4 VPN fails for remote users

Check:
- user credentials and MFA status
- certificate or client configuration
- allowed network ranges
- firewall or route policy
- endpoint health and client logs

### 11.5 Backup failed overnight

Check:
- disk space on backup target
- credential validity
- backup window and schedule
- connectivity to offsite or cloud target
- restore test status
- retention policy and log entries

### 11.6 New employee cannot work on day one

Check:
- account created
- correct groups assigned
- device joined or enrolled
- VPN access available
- email and communication tools active
- standard software installed
- printer and file share access assigned

---

## 12. Troubleshooting workflow for SMB IT teams

A good troubleshooting process prevents guesswork.

### Step 1: Define the problem
Ask:
- what is failing exactly?
- who is affected?
- did this start recently?
- what changed last?

### Step 2: Check the basics
- power status
- network connection
- IP configuration
- gateway and DNS
- account state
- application status

### Step 3: Narrow the scope
- one user or many?
- one site or multiple?
- one service or many?
- local or remote access?

### Step 4: Test likely causes
Useful examples:
- `ping`
- `tracert` / `traceroute`
- `nslookup` or `dig`
- `ipconfig /all`
- `arp -a`
- verifying firewall rules
- checking switch port health
- reviewing backup logs

### Step 5: Apply the smallest correct fix
Fix the likely cause without unnecessary system-wide changes.

### Step 6: Validate and document
Confirm the issue is resolved and record the work done.

---

## 13. Practical tools for SMB support teams

### Network and connectivity tools
- `ping`
- `tracert` / `traceroute`
- `nslookup`
- `ipconfig`
- `arp`
- `netstat`
- Wi‑Fi analyzer tools
- switch management interface
- firewall administration console

### Endpoint tools
- device management portal
- patch management console
- remote support software
- antivirus / endpoint detection tools
- software inventory tools

### Data and backup tools
- backup software dashboard
- restore validation reports
- storage health monitoring
- cloud sync and storage reporting

### Business operations tools
- ticketing system
- asset tracking spreadsheet or CMDB
- documentation portal
- change log and approval process

---

## 14. Recommended SMB architecture patterns

### Pattern A: Simple office network
- ISP router
- firewall
- managed switch
- Wi‑Fi access points
- one or two file servers
- standard endpoint management
- cloud email and backup

### Pattern B: Hybrid office + cloud-first
- local LAN and firewall
- cloud identity and productivity platforms
- limited local file services
- SaaS backup and remote access
- endpoint management for all devices

### Pattern C: Small branch office setup
- branch firewall and VPN
- core office services accessible remotely
- local print and file sharing
- central backup and identity management

---

## 15. Typical support responsibilities in SMB IT

A SMB IT specialist may regularly handle:

- user setup and password resets
- Wi‑Fi and printer issues
- laptop repair and replacement coordination
- server reboot and health checks
- office internet troubleshooting
- shared folder permission problems
- vendor coordination for ISP, hardware, or internet issues
- patching and antivirus oversight
- backup job monitoring
- user onboarding and offboarding
- access review and business continuity testing

This is why broad technical understanding matters so much in smaller companies.

---

## 16. Common standards and best practices

### Standard software and equipment
A well-run small company often uses a manageable standard:

- standard laptop and desktop models
- limited device types for easier support
- standard application stack
- consistent patching schedule
- approved security tools
- limited custom workarounds

### Asset management
Track:
- who owns the device
- where it is located
- when it was deployed
- software license status
- support warranty status
- replacement lifecycle

### Access review cadence
Perform periodic reviews of:
- departmental file permissions
- admin rights
- shared mailbox access
- VPN access
- cloud storage sharing
- former employee access remains

---

## 17. Governance and documentation checklist

A company IT team should keep track of:

- network diagrams
- device inventory
- IP address ranges
- switch and AP inventory
- backup schedule and restore test results
- firewall rule set and change log
- user access review records
- software licensing and support status
- business continuity contacts
- escalation procedures

---

## 18. Learning path for SMB IT support

### Level 1: Fundamentals
- networking basics
- IP addressing and DHCP
- DNS and gateway concepts
- laptop and printer troubleshooting
- basic file permissions

### Level 2: Business operations
- backup and restore planning
- identity and MFA support
- remote access troubleshooting
- Wi‑Fi troubleshooting
- inventory and documentation

### Level 3: System support
- server basics
- virtualization or VM support
- storage concepts
- patching and endpoint management
- policy enforcement and security basics

### Level 4: Business continuity and governance
- DR planning
- access review and audits
- service continuity documentation
- vendor coordination and escalation
- operational improvement and cost control

---

## 19. Glossary for SMB IT support

### LAN
Local Area Network; network inside the office or site.

### WAN
Wide Area Network; connecting offices or external sites.

### VLAN
Virtual local area network; segmentation inside the same switch infrastructure.

### DHCP
Dynamic Host Configuration Protocol; automatic IP assignment.

### DNS
Domain Name System; translates names to IPs.

### VPN
Virtual Private Network; encrypted remote or inter-site access.

### RPO
Recovery Point Objective; acceptable amount of data loss.

### RTO
Recovery Time Objective; acceptable restoration time.

### Endpoint
Any connected user device such as a laptop, desktop, printer, or phone.

### CMDB
Configuration Management Database; inventory and configuration tracking.

### Ticket
A tracked support request or incident record.

### Patch
A software update that fixes defects or closes vulnerabilities.

### MFA
Multi-factor authentication; adds an extra verification step.

---

## 20. Final guidance for practical IT support

The most effective SMB IT support teams follow a simple operating principle:

- know the business context
- understand the network path
- validate the user and device state
- confirm permissions and access
- protect business data
- test recovery before it is needed
- document everything clearly

The best IT support professionals are not just “fixers.” They are operational partners who keep company technology aligned with real business needs.

---

## 21. Summary

Company computer networking and data management are the backbone of dependable business operations. In a small-to-medium company, this area includes:

- connectivity and network health
- workstation and mobile support
- user accounts and permissions
- secure access and MFA
- safe file sharing and storage
- backup and restore strategy
- security hygiene and monitoring
- clear troubleshooting and operational documentation

This is the foundation of reliable IT support in any growing business.

---

## 22. Suggested future additions

This catalog can continue to grow with:

- a basic network diagram section
- common SMB equipment list
- standard operating procedure templates
- troubleshooting decision trees
- hardware inventory form
- backup checklist
- security audit checklist
- onboarding/offboarding checklist
- end-user support guide

If you want, this repository can be expanded into a more complete operational handbook for business IT support and systems administration.

