# Company IT Support, Networking, and Data Management Catalog

A practical, business-focused reference for IT support, systems administration, help desk operations, endpoint management, networking, and business data protection in small-to-medium organizations.

This catalog is designed for IT support professionals, help desk technicians, desktop support specialists, network administrators, junior systems administrators, and operational technology staff who want to improve service quality, reduce downtime, strengthen security, and demonstrate professional competence in day-to-day business technology operations.

It is intentionally written in a way that is useful for both real-world support work and portfolio development. It highlights not only technical knowledge, but also operational discipline, troubleshooting capability, business awareness, and professional communication.

---

## Why this catalog matters

In a small or medium business, technology is not an isolated department; it is part of every business function.

When IT is healthy, employees can work without disruption. When IT fails, productivity, security, customer service, and compliance all suffer.

This catalog addresses the practical questions that matter in the workplace:

- How do users connect to the network and get to their resources?
- How do we troubleshoot a device, printer, VPN, or shared drive?
- How do we protect business data and recover from failures?
- How do we secure identities and control user access?
- How do we maintain a reliable support process while documenting work professionally?

---

## Portfolio value for IT professionals

This repository is structured to support both technical learning and professional positioning.

It reflects the kind of work employers expect from capable IT support staff, including:

- troubleshooting PCs, laptops, mobile devices, and printers
- supporting office connectivity, Wi‑Fi, and LAN services
- managing identity, MFA, permissions, and account lifecycle
- maintaining file access, data storage, and backup operations
- supporting cloud tools and SaaS platforms
- documenting incidents, changes, and recurring problems
- improving service reliability and user experience
- maintaining a secure and organized digital environment

This makes the catalog valuable as a portfolio artifact, personal study guide, internal knowledge base, or operational reference for SMB IT teams.

---

## Scope of the catalog

This repository covers the core areas of practical business IT support:

- network connectivity and office infrastructure
- workstation and endpoint support
- identity and access management
- shared file systems and data access
- backup, restore, and business continuity
- endpoint security and patching
- cloud services and SaaS support
- troubleshooting and help desk workflows
- documentation, governance, and operational maturity

---

## Typical SMB IT environment

A small-to-medium business technology environment often includes:

- ISP internet connection and edge router
- firewall or secure gateway
- LAN switches and Wi‑Fi access points
- laptops, desktops, and mobile devices
- printers, scanners, and shared office equipment
- Active Directory, Entra ID, or cloud identity platform
- file server or NAS storage
- backup appliance or cloud backup service
- SaaS applications such as email, document storage, CRM, ticketing, and project tools

This environment is where IT support professionals operate every day: keeping systems available, users productive, and business data protected.

---

## Business IT layers

| Layer | Purpose | Typical components |
| --- | --- | --- |
| Access layer | User connectivity | Wi‑Fi, LAN, VPN, printers, endpoints |
| Network layer | Routing and communication | switches, routers, firewalls, VLANs, ISP |
| Identity layer | Authentication and access | accounts, MFA, groups, permissions |
| Device layer | Workstations and endpoints | laptops, desktops, tablets, scanners |
| Data layer | Storage and file access | file servers, NAS, cloud storage, databases |
| Security layer | Protection and governance | patching, endpoint security, access reviews |
| Operations layer | Maintenance and support | monitoring, tickets, backups, documentation |

---

## 1. Core responsibilities of IT support staff

IT support professionals are responsible for much more than fixing isolated technical issues. They are the operational backbone of digital reliability in the workplace.

### 1.1 Primary responsibilities

- support end users with hardware, software, and access issues
- troubleshoot network, Wi‑Fi, and connectivity problems
- manage user accounts, permissions, and access rights
- maintain endpoint health, patching, and security posture
- support file access, printing, and shared data services
- coordinate with vendors for network or equipment issues
- ensure backups and restore capabilities remain operational
- document incidents, changes, and recurring issues
- maintain service continuity during outages or business disruptions

### 1.2 Quality expectations

A strong IT support professional is expected to:

- communicate clearly with non-technical users
- think systematically instead of guessing
- work efficiently under time pressure
- prioritize urgent business impact
- document findings and resolutions
- maintain confidentiality for sensitive business systems
- learn quickly and adapt as environments evolve

---

## 2. Network fundamentals for company IT

### 2.1 Office network design

A typical office network includes:

- modem or ISP router
- firewall or security appliance
- core switch and access switches
- Wi‑Fi access points
- VLANs for guest, voice, server, or management traffic
- user endpoints
- shared services such as servers, printers, and cloud gateways

### 2.2 Core networking concepts

#### IP addressing
IP addresses identify devices on a network.

Examples:
- 192.168.10.20
- 10.0.0.15
- 172.16.5.10

Support relevance:
- no valid IP often means DHCP or link failure
- duplicate IPs can break connectivity
- incorrect subnet values can isolate systems from the business network

#### Subnet masks
A subnet mask determines which portion of the IP address is the network and which is the host.

This matters because:
- devices on the same subnet can communicate directly
- devices on different subnets require a gateway
- incorrect subnet settings create confusing communication problems

#### Default gateway
The default gateway is the path for traffic leaving the local network to reach external destinations, such as the internet.

#### DNS and name resolution
DNS resolves names such as fileserver or mail.company.com into IP addresses.

Common symptoms of DNS problems:
- websites fail to load
- internal apps stop resolving
- file servers cannot be reached by name
- email and authentication workflows become inconsistent

#### DHCP
DHCP automatically assigns network configuration details, including:

- IP address
- subnet mask
- default gateway
- DNS server addresses

Common issues:
- no lease assigned
- stale or duplicate lease entries
- wrong gateway or DNS values delivered
- rogue DHCP server on the network

#### Routers and firewalls
The router connects local networks to other networks. The firewall enforces network security policy and controls traffic.

Support tasks:
- validate routes and default paths
- review recent firewall changes
- confirm VPN or remote access policy is correctly applied
- verify ISP and upstream service health

#### Switches and ports
Switches connect devices inside the office LAN.

Common issues:
- bad patch cable
- disabled ports
- wrong VLAN assignment
- loop or broadcast storms
- failed port or switch hardware

#### Wi‑Fi
Wi‑Fi is a frequent source of office complaints.

Typical concerns:
- weak signal in some areas
- AP overlap or channel interference
- roaming issues between access points
- guest network isolation problems
- poor access point placement or coverage gaps
- stale device profiles after changes

#### VLANs
VLANs separate traffic logically within the same physical network.

Examples:
- staff VLAN
- guest Wi‑Fi VLAN
- server VLAN
- management VLAN
- voice VLAN

### 2.3 Connectivity troubleshooting checklist

When a user reports, “I can’t access the internet,” the support professional should check:

- device is connected to Wi‑Fi or wired connection
- valid IP address is assigned
- gateway is reachable
- DNS is resolving properly
- user is not using a blocked VPN route
- firewall is not filtering traffic incorrectly
- ISP connection is healthy

---

## 3. Endpoints and workstation support

Most day-to-day IT support work centers on endpoints.

### 3.1 Common endpoint categories

- desktops
- laptops
- tablets
- mobile phones
- printers
- scanners
- conference room hardware
- thin clients or kiosk devices

### 3.2 Typical endpoint problems

- slow boot or startup
- application crashes or lockups
- driver failures
- patching and update issues
- profile corruption or login errors
- missing permission or policy enforcement
- low disk space
- malware or unauthorized software

### 3.3 Printer support

Printers are often a major source of office tickets.

Common issues:
- queue stuck
- printer offline
- wrong IP address or hostname
- driver mismatch
- print spooler failure
- switch port or Wi‑Fi issue

### 3.4 Mobile device support

Support activities often include:

- email configuration
- MFA enrollment and resets
- VPN setup
- device compliance and MDM enrollment
- lost or stolen device procedures
- remote wipe and access revocation

---

## 4. Identity and access management

### 4.1 User identity basics

A user identity is how a person is recognized in the company’s digital systems.

Examples:
- Active Directory
- Microsoft Entra ID
- Google Workspace accounts
- local desktop accounts
- service accounts

### 4.2 Onboarding

Typical onboarding steps:

- create the account
- assign email and identity credentials
- assign required groups or roles
- grant access to shared resources
- install required software
- configure VPN and remote access
- map printers and shared drives
- verify the user can access essential systems

### 4.3 Offboarding

Offboarding is essential for security and operational continuity:

- disable the account
- revoke access to file shares and cloud apps
- remove SaaS licenses
- archive or transfer data when required
- collect company equipment
- confirm no lingering access remains

### 4.4 Permissions and groups

Permissions should be controlled and reviewed regularly.

Best practices:
- group-based access wherever possible
- least-privilege model
- periodic access review
- documented approval process
- remove stale rights after role changes

### 4.5 MFA and authentication support

Common support issues:
- approval not received
- new phone or device enrollment
- authenticator reset issues
- lockout caused by repeated failed attempts
- inability to access VPN or email after policy changes

---

## 5. Shared data and file management

### 5.1 Where company data usually lives

- file servers
- NAS appliances
- department shared folders
- cloud storage such as OneDrive, SharePoint, Google Drive
- databases and business systems
- email archives and collaboration platforms

### 5.2 Shared folder design

A well-organized shared data model includes:

- HR and payroll folders
- finance and accounting data
- project and operations documents
- templates and standard forms
- archived records and retention storage

### 5.3 File permission model

Recommended approach:

- assign permissions via groups
- avoid broad access rights
- review sensitive folders regularly
- document ownership of each share
- validate access during role changes

### 5.4 Support issues in data access

- user cannot open a folder
- file appears read-only unexpectedly
- share mapping is broken
- permissions are inherited incorrectly
- file server is offline or slow
- user has wrong department access

---

## 6. Backup, storage, and continuity

### 6.1 Backup fundamentals

Backups protect business data against:

- hardware failure
- ransomware and malware
- accidental deletion
- software corruption
- user error
- natural disasters or power disruptions

### 6.2 What to back up

Common business data to protect:

- file shares
- server data
- virtual machines
- databases
- email data
- cloud storage content
- endpoint data when required

### 6.3 Backup design questions

- What is being backed up?
- Where is the data stored?
- How frequently does the job run?
- How long is the data retained?
- What happens if the backup target fails?
- Has the restore process been tested recently?

### 6.4 Recovery objectives

- RPO: Recovery Point Objective — how much data loss is acceptable
- RTO: Recovery Time Objective — how quickly restoration must happen

### 6.5 Storage targets

- local NAS appliance
- offsite or cloud backup service
- external disk rotation
- virtualization backup tools
- SaaS retention tools

### 6.6 Disaster recovery

Disaster recovery planning includes:

- restoring failed servers
- recovering file shares
- re-establishing email and identity access
- restoring remote access and office connectivity
- validating business-critical systems first

---

## 7. Security basics for small and medium companies

SMBs are often targeted because they may have weaker defenses and fewer dedicated specialists.

### 7.1 Basic security controls

- strong password policy
- MFA on critical systems
- patching and software updates
- antivirus and endpoint protection
- user access reviews
- secure Wi‑Fi settings
- least privilege access
- backup verification
- logging and alert review

### 7.2 Common security issues

- phishing attempts
- password reuse
- stale accounts
- unpatched operating systems
- overly broad local admin rights
- insecure remote access
- poor backup testing
- users installing unapproved software

### 7.3 Security operations checklist

- verify user access after role changes
- monitor alerts for suspicious activity
- review firewall logs on a schedule
- check endpoint protection status
- confirm backups succeed and are test-restorable
- validate patch compliance on critical devices

---

## 8. Servers, virtualization, and infrastructure basics

Even small companies may operate basic server infrastructure.

### 8.1 Standard server roles

- domain controller or identity service
- file server
- print server
- database server
- application server
- backup server
- virtualization host

### 8.2 Virtualization concepts

Virtual machines allow a business to run several systems on fewer physical machines.

Support tasks include:

- VM health checks
- storage utilization review
- snapshot management
- host resource monitoring
- VM backup and restore verification

### 8.3 Server health checks

- CPU utilization
- RAM usage
- storage capacity
- service health
- event log review
- uptime and unexpected restarts

---

## 9. Cloud services and SaaS in company IT

Modern business operations depend on cloud tools.

### 9.1 Common cloud services

- Microsoft 365 / Outlook / SharePoint / OneDrive
- Google Workspace
- cloud storage platforms
- collaboration and document systems
- CRM and customer systems
- ticketing and project management tools

### 9.2 Cloud support concerns

- failed sync
- storage quota issues
- stale sharing links
- MFA or sign-in problems
- permission mismatches
- downtime or service outages

### 9.3 Hybrid environments

Many companies rely on hybrid environments:

- local file server and cloud email
- Microsoft Entra ID with local directory services
- on-prem authentication with cloud productivity platforms
- remote access enabled through VPN and identity tools

---

## 10. Monitoring, maintenance, and proactive support

A reliable IT environment is not only reactive. It also includes proactive operations.

### 10.1 Monitoring activities

- uptime checks
- disk usage monitoring
- backup success verification
- firewall event review
- internet connectivity checks
- endpoint health checks
- certificate expiry monitoring
- service availability checks

### 10.2 Maintenance windows

Regular maintenance includes:

- patching and updates
- reboot scheduling for devices or services
- backup validation
- access reviews
- hardware health checks
- software inventory cleanup

### 10.3 Preventive support mindset

The best IT teams reduce incidents by addressing small issues early:

- keep devices updated
- review storage before it fills up
- monitor backups daily
- document changes
- confirm remote access after policy updates
- review network health before users experience outages

---

## 11. Help desk and IT support operations

### 11.1 Ticketing workflow

A strong support workflow should include:

- ticket creation
- issue classification
- owner assignment
- triage and investigation
- corrective action
- user communication
- validation of resolution
- closure and documentation

### 11.2 Triage questions

- Is this affecting one user or many?
- One office or multiple locations?
- One service or many services?
- Was there a recent change?
- Is it a network, device, identity, data, or cloud issue?

### 11.3 Documentation best practices

Good support notes include:

- date and time
- affected user and device
- location and site
- issue summary
- troubleshooting steps taken
- findings and root cause
- final resolution
- validation evidence

---

## 12. Change management and governance

### 12.1 Change control

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
- approver
- scheduled time
- expected impact
- rollback plan
- verification after change

### 12.2 Governance basics

A business should maintain:

- IT asset inventory
- device ownership records
- network documentation
- backup policy and restore test history
- permission review schedule
- supplier and provider contact list

---

## 13. Asset management and lifecycle

### 13.1 Inventory should include

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

### 13.2 Lifecycle planning

Businesses should plan for:

- computer replacement cycles
- printer replacement
- UPS and power protection checks
- network equipment refresh
- storage upgrade planning
- software renewal dates

---

## 14. Remote access and business continuity

### 14.1 VPN and remote support

Remote troubleshooting is essential in modern IT support.

Common remote support tasks:

- VPN diagnosis
- device remote assistance
- cloud sign-in issue resolution
- workstation remote management
- firewall and route validation for remote users

### 14.2 Business continuity ideas

Support teams should consider:

- access to critical services during outages
- emergency communication methods
- remote work readiness
- offline workarounds for essential tasks
- backup restore testing before a real incident

---

## 15. Common IT support scenarios

### User cannot access the internet
Check:

- Wi‑Fi or cable connection
- IP address and subnet
- gateway reachability
- DNS resolution
- ISP or service outage
- firewall or VPN blocking traffic

### User cannot reach a file share
Check:

- user account is active
- file server is online
- DNS resolves the share name correctly
- permissions are correct
- VPN is connected if remote
- drive mapping is valid

### Printer is offline
Check:

- printer IP is valid
- cable or Wi‑Fi connection is healthy
- print queue is not stuck
- print server is available
- driver version matches the install
- switch port status is stable

### New employee cannot work on day one
Check:

- account created and active
- email and identity access are configured
- required groups and roles assigned
- device enrolled or joined to the environment
- required software installed
- printer and shared drive access assigned

### Backup failed overnight
Check:

- storage target has free space
- connection to the target is healthy
- credentials are valid
- backup logs show the failed job
- retention policy and schedule are correct
- restore validation status is current

### VPN fails for a remote user
Check:

- MFA status
- VPN client version
- certificate validity
- route or firewall policy
- service outage or endpoint issue

---

## 16. Troubleshooting workflow

A disciplined troubleshooting approach reduces guesswork and improves professionalism.

### Step 1: Define the symptom
Ask:

- What is actually happening?
- Who is affected?
- When did it start?
- What changed recently?

### Step 2: Check the basics

- power and physical connectivity
- network cable or Wi‑Fi state
- valid IP assignment
- gateway and DNS status
- account status and permissions
- backup or service health

### Step 3: Reduce the scope

- Is it one user or many?
- One site or multiple sites?
- Local, remote, or cloud-based?

### Step 4: Validate likely causes

Useful tools:

- ping
- tracert / traceroute
- nslookup / dig
- ipconfig /all
- arp -a
- firewall logs
- switch port status
- event logs
- backup logs

### Step 5: Apply the smallest correct fix

Avoid broad changes when a focused repair will resolve the issue.

### Step 6: Verify and document

Before closing a ticket, confirm:

- the issue is resolved
- the user can access the required service
- no new problems were introduced
- the change was logged and communicated appropriately

---

## 17. Common IT tools and commands

### Windows

- ipconfig /all
- ping <hostname>
- tracert <hostname>
- nslookup <domain>
- arp -a
- netstat -an
- route print
- systeminfo
- tasklist
- services.msc
- diskpart
- getmac

### Linux / Unix

- ip addr
- ifconfig
- ping
- traceroute
- dig
- ss -tulpn
- df -h
- du -sh
- mount
- journalctl

### Operational checks

- verify backup status and logs
- inspect failed jobs
- check disk utilization and room for growth
- confirm patching status
- review access logs and firewall events
- validate restore tests

---

## 18. Frequently missing but highly important topics

These are the areas that often distinguish a basic technology list from a realistic operational support catalog:

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

These details transform a technology repository into a professional operational playbook.

---

## 19. IT support glossary

### Active Directory
A directory service used to manage users, computers, and permissions in Windows environments.

### DNS
Domain Name System; resolves names into IP addresses.

### DHCP
Dynamic Host Configuration Protocol; automatically assigns network settings.

### VLAN
Virtual local area network; logically separates traffic within a network.

### Firewall
A network control that filters traffic based on policy.

### NAS
Network-attached storage used for shared file access.

### SAN
Storage area network used for block-based storage in server and application environments.

### VPN
Virtual private network for secure remote or inter-site connectivity.

### MFA
Multi-factor authentication; adds an additional layer of verification.

### RPO
Recovery Point Objective; acceptable data loss.

### RTO
Recovery Time Objective; acceptable recovery time.

### CMDB
Configuration management database; asset inventory and configuration tracking.

### Ticket
A tracked support request or incident record.

### Patch
A software update that fixes defects or closes security weaknesses.

---

## 20. Learning roadmap for business IT support

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

## 21. Professional support checklist

Use this as an operational checklist for daily IT work:

- network and internet connectivity verified
- DHCP and DNS healthy
- user account active and permissions correct
- file access and shared storage available
- endpoint patched and protected
- backup status confirmed
- change documented and approved
- issue verified as resolved before closure

---

## 22. Professional mindset for IT support staff

The most effective IT support teams are not only reactive technicians. They are structured problem solvers who understand:

- how the network works
- how users access business systems
- how files and backups are protected
- how identity and permissions affect productivity
- how to verify fixes before closing a ticket
- how to document and improve the environment over time

This is the difference between ad hoc troubleshooting and dependable business technology operations.

---

## 23. Practical portfolio profile

This repository demonstrates a practical skill set aligned with real-world IT support work, including:

- business IT operations and service reliability
- endpoint and desktop support
- network troubleshooting and connectivity analysis
- access management and user lifecycle control
- data protection, backup, and recovery readiness
- cloud and SaaS support awareness
- security hygiene and patching discipline
- documentation, ticketing, and operational consistency

These are the types of capabilities that help IT support professionals move from simply fixing problems to becoming dependable contributors in business operations.

---

## 24. Summary

Company computer networking and data management are foundational capabilities in modern business operations.

For a small-to-medium business, the core goal is to maintain:

- stable connectivity
- reliable endpoint support
- correct user access
- protected and accessible data
- backup and recovery readiness
- secure, well-managed business systems

This catalog is intended to serve as a practical and professional reference for IT support work and as a strong foundation for a technology-focused professional portfolio.

---

## 25. Suggested future repository expansions

To make the project even more complete as a real-world IT support portfolio and operational resource, future sections could include:

- network diagram examples
- troubleshooting decision trees
- common SMB hardware inventory spreadsheet
- onboarding checklist for new employees
- offboarding checklist for leaving staff
- backup validation checklist
- security hygiene checklist
- change log template
- support ticket template
- disaster recovery planning template
- escalation matrix
- remote support playbook

These additions would turn this repository into a true business IT operations handbook.

---

## 26. Final statement

This repository is not only a technical catalog. It represents the work habits, decision-making process, and operational mindset of a capable IT support professional: organized, resilient, service-focused, and business-aware.

That is what makes it valuable both in practice and in professional development.

---

## 27. Recommended repository purpose statement

This project can be positioned in a portfolio or employer context as:

“Practical catalog of company IT support, networking, identity management, and data protection practices for small-to-medium business environments. Focused on reliable endpoint support, secure access control, network troubleshooting, backup readiness, and operational documentation.”

This framing reflects both technical depth and business relevance, which is ideal for an IT support portfolio.

---

## 28. Closing note

The goal is simple: support the business, protect the data, keep users productive, and communicate clearly while resolving issues with discipline and professionalism.

That is the heart of strong IT support work.

