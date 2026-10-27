# Company Computer Networking and Data Management Catalog

A practical, support-focused catalog for IT professionals who keep business systems running: help desk technicians, desktop support specialists, network administrators, system administrators, and small-business IT teams.

This repository is a field guide to the technologies behind office connectivity, user access, shared data, backups, endpoint health, and everyday IT support. The focus is not abstract theory alone—it is the real work of keeping staff productive, devices connected, permissions correct, and business data available.

## Why this catalog exists

In most companies, the biggest IT issues are repetitive and recognizable:

- a workstation cannot reach the network
- Wi‑Fi is unstable in one office area
- a user cannot access a shared folder
- a printer is offline or stuck in a queue
- a VPN connection fails for remote users
- a server is slow or unavailable
- backups failed overnight
- account permissions are wrong after a role change

Strong IT support depends on understanding how the company’s systems connect and fail.

## What this catalog covers

- network basics and office connectivity
- computer and device support
- user identity, authentication, and permissions
- file storage, backups, recovery, and retention
- endpoint security and patching
- troubleshooting workflows in a business setting
- common IT support scenarios and operational habits

## Core IT support layers

| Layer | What it includes | Typical IT support tasks |
| --- | --- | --- |
| Network layer | switches, routers, Wi‑Fi, firewalls, VLANs, IP addressing, DNS, DHCP | connectivity checks, ISP issues, AP coverage, switch ports |
| Endpoint layer | desktops, laptops, printers, mobile devices, conference equipment | login issues, driver problems, slow devices, queue errors |
| Identity layer | users, groups, accounts, MFA, access policies | password resets, account lockouts, permission review |
| Data layer | file servers, NAS, cloud storage, shared drives, backups | restore testing, storage capacity, access problems |
| Security layer | patching, endpoint protection, access hygiene, audits | phishing response, MFA enforcement, policy validation |
| Operations layer | tickets, documentation, change control, escalation | triage, root cause analysis, incident communication |

---

## 1. Company network architecture

A business network is usually a combination of the following:

- local area network (LAN)
- wireless access points (WAPs)
- routers and internet connectivity
- switches and patching
- firewall and security rules
- VPN for remote users or branch offices
- internal services such as file servers, print servers, and identity services

### Typical office network components

- modem or ISP edge router
- firewall or secure gateway
- core or distribution switch
- access switches in office areas
- Wi‑Fi access points
- domain controllers or identity services
- file server or storage appliance
- printers and endpoint devices

### Common networking concepts

#### IP address
An IP address identifies a device on a network. A correct IP is required for communication on the LAN and beyond.

Examples:
- `192.168.1.20`
- `10.10.10.50`

Support relevance:
- no IP implies connectivity or DHCP problem
- duplicate IP can break traffic
- wrong subnet can isolate a machine from the rest of the office

#### Subnet mask
A subnet mask tells devices which part of the IP address is the network and which part is the host.

Why it matters:
- same-subnet devices can talk directly
- different subnets need a gateway
- misconfiguration often causes unusual “I can ping some things but not others” problems

#### Default gateway
A gateway is the device that forwards traffic from the local network to other networks such as the internet or another office site.

Support symptom:
- client has an IP but no internet access
- gateway is unreachable or wrong

#### DNS
DNS resolves names like `fileserver` or `mail.company.com` into IP addresses.

Common symptoms:
- users cannot reach internal services by name
- websites do not load
- email or login flows fail

#### DHCP
DHCP automatically assigns IP, subnet, gateway, and DNS information.

Typical support issues:
- no address lease issued
- duplicate or stale leases
- wrong DNS or gateway delivered
- rogue DHCP device on the network

#### Switches
Switches connect devices in a LAN and move traffic inside the local network.

Common issues:
- port disabled
- bad cable or patching
- wrong VLAN assignment
- switch port flapping

#### Routers and firewalls
Routers connect networks. Firewalls restrict or permit traffic based on policy.

Support tasks:
- validate interface status
- confirm default route exists
- review rule changes
- inspect VPN or remote access service behavior

#### Wi‑Fi
Wireless access is often the single largest source of user complaints.

Typical problems:
- weak signal
- roaming issues
- interference
- corrupted client profiles
- wrong SSID or encryption settings
- AP health or channel overlap

#### VPN
A VPN provides secure access for users working remotely or connecting between offices.

Common support checks:
- MFA status
- VPN profile health
- client certificate validity
- route configuration
- firewall or NAT behavior

#### VLAN
A VLAN divides traffic logically even if devices share the same physical switch.

Why it matters:
- guest Wi‑Fi stays isolated from production traffic
- voice and data can be separated
- server, admin, and user networks can be grouped cleanly

---

## 2. Data management and company information flow

A company’s data is usually spread across several locations and systems:

- workstations and laptops
- shared file servers
- NAS devices
- cloud services such as OneDrive or SharePoint
- email and collaboration platforms
- database servers and application storage
- backup appliances and archive systems

### File servers and shared storage
A file server hosts the shared data users need to access every day.

Typical tasks:
- checking share availability
- validating permissions
- monitoring disk usage
- restoring files from backup
- verifying performance during business hours

### Permissions and access control
The right access model is essential to operational stability.

Best practice:
- assign permissions through groups
- follow least privilege
- remove stale access when roles change
- review access regularly

### NAS and SAN
- NAS: network-attached storage, commonly used for file-based sharing
- SAN: storage area network, typically used by servers and applications with block-level storage

Support concerns:
- capacity warnings
- failed drives
- degraded RAID status
- snapshots and backups not completing

### Backup and restore
Backups protect against accidental deletion, malware, hardware failure, or outages.

Key backup questions:
- what is being backed up?
- where is it stored?
- how often does it run?
- how long is it retained?
- has a restore been tested recently?

### Recovery terminology

- RPO: Recovery Point Objective; how much data loss is acceptable
- RTO: Recovery Time Objective; how long recovery may take

These values help determine backup frequency, redundancy, and recovery planning.

### Cloud storage and collaboration
Modern businesses commonly use:

- OneDrive
- SharePoint
- Google Drive
- Dropbox
- SaaS document platforms

Support issues include:
- sync errors
- file conflicts
- quota limits
- expired sharing links
- permission mismatches

---

## 3. Identity, access, and user support

User access is central to business operations. If the identity layer fails, users cannot log in, access files, or use the right services.

### User accounts and authentication
Common problems:
- disabled account
- expired password
- lockout after repeated failed sign-ins
- MFA approval issues
- stale account remaining after employee departure

### Groups and permissions
Groups are the most common way to assign access consistently.

Good practice:
- team-based groups
- standard access templates
- removal of excess rights
- periodic access review

### MFA and security checks
Multi-factor authentication helps secure login flows, but it can also generate support work.

Typical ticket causes:
- authenticator not available
- lost device
- approval not received
- user changed phone number
- silent policy update requiring re-registration

### Onboarding and offboarding
IT support is often measured by how smoothly user lifecycle changes happen.

Onboarding includes:
- account creation
- email setup
- device delivery
- VPN setup
- software installation
- access to shared drives and printers

Offboarding includes:
- disabling accounts
- reviewing permissions
- collecting equipment
- removing SaaS access
- verifying data retention and compliance requirements

---

## 4. Endpoint and workstation support

Most day-to-day support work happens at the endpoint layer.

### Workstations and laptops
Common issues:
- slow startup
- application conflicts
- bad drivers
- patching issues
- profile corruption
- login failures

### Printers and scanners
Printers are an almost universal source of office support problems.

Typical causes:
- wrong IP or hostname
- queue stuck
- driver mismatch
- spooler service issue
- switch or patch cable fault
- Wi‑Fi print device connectivity issue

### Mobile devices
Support often includes smartphones and tablets.

Areas of support:
- email setup
- MFA enrollment
- mobile device management
- lost device process
- VPN configuration
- secure wipe and access revocation

---

## 5. Security and governance basics

IT support is not just “fixing computers.” It is also about protecting business systems and maintaining operational discipline.

### Essential security habits
- least privilege access
- patching and update compliance
- strong MFA enforcement
- secure remote access
- software inventory
- device inventory
- log review and alert triage
- change tracking and documentation

### Support practices that create risk
- granting broad access “just to solve the issue”
- shared local admin accounts without accountability
- undocumented changes
- ignoring alerts that seem minor
- no validation of restore or backup process

---

## 6. Real-world troubleshooting workflow

A reliable support process is more important than guessing.

### Step 1: Determine the scope
Ask:
- one user or many?
- one office or multiple offices?
- one service or many?
- local network issue or remote user issue?

### Step 2: Check the basics
- device is powered on
- network cable or Wi‑Fi connection is active
- DHCP has assigned an IP
- gateway is reachable
- DNS resolves names
- username and password are valid
- required service is online

### Step 3: Classify the problem
Possible categories:
- connectivity problem
- device configuration issue
- access or permissions issue
- storage or file share issue
- service outage
- security policy issue

### Step 4: Test the likely cause
Useful checks:
- `ping`
- `tracert` / `traceroute`
- `nslookup` / `dig`
- `ipconfig /all`
- switch port status
- firewall rule review
- shared folder permission check
- VPN connection state

### Step 5: Document clearly
Support notes should include:
- when the issue started
- affected user or department
- device name and location
- error message or symptom
- tests performed
- changes made and their result

### Step 6: Verify resolution
Before closing a ticket, confirm:
- the original issue is gone
- the user can access the needed resource
- the fix did not cause a new problem
- documentation is updated

---

## 7. Common IT support scenarios

### User cannot access the internet
Check:
- Wi‑Fi or LAN link state
- DHCP lease and IP validity
- gateway reachability
- DNS resolution
- firewall or VPN policy
- ISP outage or upstream issue

### User cannot reach a shared file server
Check:
- DNS resolution
- network path
- server availability
- correct permissions
- VPN or remote access state
- mapped drive definition

### Office Wi‑Fi is unstable
Check:
- AP location and coverage
- channel interference
- roaming behavior
- switch port and AP health
- client DHCP behavior
- recent configuration changes

### Printer is offline
Check:
- printer IP or hostname
- switch port status
- print server availability
- queue state
- driver version
- IP conflict or network disconnect

### New employee cannot start work on day one
Check:
- active account
- correct access groups
- device enrollment or domain join
- email and VPN setup
- required software
- printer and shared drive access

### Backup failed overnight
Check:
- destination storage free space
- credentials and connectivity
- job log details
- retention policy
- failed restore test
- snapshot or appliance health

---

## 8. Tools and common commands

### Windows commands
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

### Linux / Unix commands
- `ip addr`
- `ifconfig`
- `ping`
- `traceroute`
- `nslookup` or `dig`
- `ss -tulpn`
- `df -h`
- `du -sh`
- `mount`

### Operational checks
- verify backup completion logs
- review failed job history
- inspect retention windows
- validate restore jobs
- monitor storage capacity and growth

---

## 9. Quick reference glossary

### Active Directory
A directory service used to manage users, computers, and permissions in Windows environments.

### DHCP
Automatic IP assignment for network clients.

### DNS
Name resolution service that maps hostnames to IP addresses.

### Endpoint
Any device connected to the network, such as a laptop, workstation, or mobile device.

### Firewall
A security control that filters traffic between networks and systems.

### NAS
Network-attached storage used for shared file access.

### VPN
A secure tunnel used by remote users or branch offices to access internal networks.

### Ticket
A tracked work item that documents a user issue, resolution steps, and outcome.

### Patch
A software update that fixes problems or closes vulnerabilities.

### Snapshot
A restore point captured at a specific time.

### Permission
A rule that determines whether a user or group can access a resource.

### Authentication
The process of verifying a user or device identity.

### RTO / RPO
Recovery time objective and recovery point objective; core business continuity measures.

---

## 10. Learning roadmap for business IT support

### Phase 1: Networking basics
Learn:
- IP addressing and subnets
- DNS and DHCP
- gateways and routes
- Wi‑Fi basics
- switches and VLANs
- firewall fundamentals

### Phase 2: User and device support
Learn:
- desktops and laptops
- login and profile issues
- printer support
- VPN troubleshooting
- mobile device basics

### Phase 3: Storage and data management
Learn:
- file permissions
- backup scheduling and restore testing
- retention policies
- NAS and cloud storage access
- capacity monitoring

### Phase 4: Security and operations
Learn:
- MFA enforcement
- account lockout investigation
- access review and clean-up
- patch compliance
- incident communication and documentation

---

## 11. Support mindset to remember

The best IT support professionals solve problems with structure.

They ask:
- what changed?
- who is affected?
- which service is failing?
- which layer is responsible?
- is this a network, identity, endpoint, or data issue?
- what is the safest quick fix?
- how do we confirm it is actually resolved?

This mindset is what separates reactive troubleshooting from dependable IT operations.

---

## 12. Quick summary

Company computer networking and data management are the backbone of successful business IT support. The goal is to keep users connected, devices healthy, access rights appropriate, and business data protected.

The most valuable skills in this field are:

- understanding network basics
- diagnosing common endpoint issues
- managing identity and access
- handling file storage and backups
- validating service recovery
- communicating clearly with users and stakeholders

These skills keep the business running reliably and efficiently.

---

## Final note

This catalog is meant to be a practical operational reference for company IT support work. It is organized around the realities of modern business environments: office networking, access control, shared data, endpoint reliability, and resilient data protection.

If you keep the following principles in mind, your IT support work will be far more effective:

- know the network
- know the data path
- know who can access what
- know how to restore service safely
- document what happened and how it was fixed

That combination is the foundation of reliable company technology operations.

---

## Suggested repository use

This README can serve as a general knowledge base for:

- onboarding new IT support staff
- documenting common support workflows
- creating troubleshooting checklists
- building internal training material
- organizing knowledge around network, permissions, and data systems

If you want, this catalog can also be expanded with:

- a network diagram section
- a troubleshooting decision tree
- a support ticket template
- an equipment inventory checklist
- a backup and disaster-recovery checklist
- a glossary of common vendor tools and products

