# Company Computer Networking and Data Management Catalog

A practical field guide for IT support teams, help desk engineers, system administrators, and technical operations staff working in small-to-medium business environments.

This catalog focuses on the real-world technologies that keep a company running: office networking, user connectivity, shared data access, backups, endpoints, security basics, and IT support workflows. It is designed to be clear, operational, and useful when things go wrong.

---

## Why this matters

In a business environment, the most common IT problems are usually not mysterious. They usually come down to a few patterns:

- a user cannot connect to the network
- a printer is offline or unreachable
- file shares are not accessible
- a user has the wrong access rights
- a backup job failed
- a device has a bad IP configuration or DNS issue
- a VPN connection is failing
- a server or service is slow, unavailable, or misconfigured

When a support team understands the structure of company networks and data systems, they can diagnose faster and make better decisions under pressure.

---

## IT support context

Small-to-medium business IT support often includes all of the following:

- user onboarding and offboarding
- laptop and desktop troubleshooting
- Wi‑Fi and office network issues
- printer support
- email and collaboration service issues
- VPN and remote access support
- file share permissions and data access
- backups, restore testing, and retention
- patching and endpoint management
- security awareness and access hygiene
- asset management and change tracking

A strong IT support engineer does not need to know every product or vendor feature by memory. They need to understand the core patterns of how business technology systems connect and fail.

---

## The main layers of a company IT environment

### 1. Network layer

This is the communication path that connects devices together.

Topics include:
- IP addressing
- subnets
- routing
- gateways
- DNS
- DHCP
- switches
- routers
- firewalls
- Wi‑Fi
- VPNs
- VLANs
- ISP and WAN connectivity

### 2. Endpoint layer

This is the layer where users actually work.

Topics include:
- laptops and desktops
- mobile devices
- printers and scanners
- conference room equipment
- user login and profile issues
- software installation and updates
- workstation performance problems

### 3. Identity and access layer

This is the layer that decides who can access what.

Topics include:
- user accounts
- authentication
- MFA
- groups and permissions
- shared folder access
- VPN access
- password resets
- account lockouts
- user lifecycle management

### 4. Data layer

This is where the company’s business information lives.

Topics include:
- file servers
- NAS devices
- cloud storage
- document collaboration systems
- backups
- snapshots
- retention policies
- archival and deletion procedures

### 5. Security layer

This layer protects the network, users, and data.

Topics include:
- endpoint protection
- patching
- access reviews
- firewall configuration
- phishing awareness
- MFA enforcement
- secure remote access
- audit and logging

### 6. Operations and support layer

This is how IT keeps everything reliable over time.

Topics include:
- ticketing
- triage
- incident response
- change management
- documentation
- validation and testing
- escalation and communication

---

## Core networking concepts

### IP address

An IP address identifies a device on a network.

Examples:
- 192.168.1.40
- 10.0.0.12

Support relevance:
- confirms whether a device has a valid network address
- helps detect conflicts and wrong configuration
- allows support teams to check whether a device is on the right subnet

### Subnet mask

A subnet mask separates the network portion of an IP address from the host portion.

Why this matters:
- devices on the same subnet can usually communicate directly
- different subnets require a gateway or router
- wrong subnet settings often create confusing connectivity problems

### Default gateway

The default gateway is the device that forwards traffic from the local network to other networks such as the internet or another office site.

If a device has an IP but cannot reach its gateway, it may have local connectivity but no real outbound access.

### DNS

DNS converts names such as `fileserver` or `mail.company.com` into IP addresses.

Typical symptoms of DNS problems:
- websites or apps fail to resolve
- users cannot reach the file server by name
- email fails or login flows break
- internal services become unreachable

### DHCP

DHCP automatically gives devices an IP address, subnet mask, default gateway, and DNS settings.

Common issues:
- no IP address assigned
- duplicate address conflict
- stale lease after network changes
- wrong DNS or gateway assignment
- rogue DHCP server on the network

### Router

A router forwards traffic between networks.

Support tasks include:
- validating the link status
- confirming the gateway is reachable
- checking whether the upstream path is working
- verifying NAT, firewall, or routing policies

### Switch

A switch connects devices inside a LAN and forwards traffic based on their addresses.

Support concerns:
- port dead or disconnected
- wrong VLAN assignment
- bad cable or patch connection
- switch health and uptime

### Firewall

A firewall controls traffic based on rules and policy.

Important questions:
- Is traffic being blocked intentionally?
- Did a recent rule change break access?
- Is a VPN or remote user being prevented from reaching a service?

### Wi‑Fi

Wi‑Fi is often the most common source of user complaints in office environments.

Typical issues:
- weak signal
- wrong SSID
- poor access point placement
- authentication failure
- channel interference
- roaming or handoff problems
- guest network segmentation issues

### VPN

A VPN creates a secure connection between a remote user or branch location and the company network.

Typical support tasks:
- MFA verification
- VPN client troubleshooting
- certificate check
- route and firewall validation
- verifying access to internal resources

### VLAN

A VLAN separates traffic logically, even when devices are connected to the same physical switch.

Why this matters:
- guest Wi‑Fi stays separate from production traffic
- voice traffic and data traffic can be separated
- user, management, and server networks can be isolated

### WAN and ISP connectivity

A WAN or ISP link connects office locations or provides internet access to the company.

Problems may include:
- outages from the service provider
- degraded bandwidth
- router failures
- internet link instability
- branch office connectivity loss

---

## Data management fundamentals

### File server

A file server stores shared company data that many users need to access.

Common support tasks:
- checking file share availability
- validating user permissions
- monitoring storage capacity
- handling slow access or offline shares
- restoring files from backup or snapshot

### Shared drives and permissions

A large part of IT support is making sure people can access the right folders and not too much.

Support issues include:
- user cannot open a shared folder
- a user has access to the wrong department data
- a file share is missing after a server change
- permissions are too broad or outdated
- a user retains access after role changes

Best practice:
- favor group-based permissions over user-by-user assignments
- apply least privilege
- regularly review access rights
- remove stale access during employee changes

### NAS and SAN

- NAS = network-attached storage, usually file-based
- SAN = storage area network, usually block-based and used by servers

Support relevance:
- storage health
- volume capacity
- performance issues
- failed drives
- restoration and redundancy checks

### Backups and restore

Backups are essential for business continuity.

Key areas:
- what is being backed up
- where the backups are stored
- how often they run
- how long data is retained
- whether the restore process has been tested

Typical backup targets:
- local backup appliance
- NAS or storage array
- cloud backup service
- external disk rotation
- virtual machine backup systems

### RPO and RTO

- RPO = Recovery Point Objective: how much data can be lost
- RTO = Recovery Time Objective: how quickly services must be restored

These are key business continuity metrics used when planning data protection.

### Snapshots and versioning

Snapshots preserve a point-in-time state of data and are often used to restore earlier versions.

Useful for:
- restoring deleted files
- recovering a virtual machine
- reverting a database to a known-good state
- reducing recovery time after accidental changes

### Retention and archival

Retention policies determine how long company data must be kept before it is archived or deleted.

This matters for:
- compliance
- audit readiness
- storage optimization
- legal and operational retention requirements

### Cloud storage

Business teams increasingly use:
- OneDrive
- SharePoint
- Google Drive
- Dropbox
- other SaaS storage platforms

Support attention areas:
- sync issues
- file conflicts
- storage quota limits
- stale access rights
- security and sharing restrictions

---

## Identity and access fundamentals

### User accounts

A user account is the primary identity used for login, file access, email, apps, and policy enforcement.

Problems often include:
- account is disabled
- password expired or needs reset
- account lockout due to failed sign-ins
- MFA prompt rejected or expired
- no permission to access the right data

### Groups and permissions

Groups are a standard way to assign access more efficiently and consistently.

Good access model:
- team-based group assignment
- least privileges
- regular audits
- controlled changes

### MFA

Multi-factor authentication adds a second layer of verification.

Common support issues:
- approval not received
- device lost or not enrolled
- wrong authenticator app setup
- users blocked after security policy changes

### Onboarding and offboarding

IT support is critical during employee lifecycle events.

Onboarding includes:
- account setup
- email access
- device assignment
- VPN profile
- shared drive access
- printer access
- software installation

Offboarding includes:
- account disablement
- data access review
- device return or wipe
- mail and SaaS removal
- audit of permissions and licenses

---

## Endpoint support essentials

### Workstations and laptops

Most day-to-day support issues involve desktop systems.

Common issues:
- slow boot times
- software conflicts
- driver problems
- printer issues
- file access problems
- login and profile issues
- patching not applied

### Printers and scanners

Printers are a frequent source of tickets in office environments.

Typical causes:
- wrong IP address
- queue stuck
- driver mismatch
- spooler errors
- patch cable or switch port issue
- Wi‑Fi connectivity problem

### Mobile devices

Support often includes smartphones and tablets:
- email setup
- MFA enrollment
- VPN access
- device management
- lost or stolen device process
- remote wipe and security procedures

---

## Backup and business continuity concepts

### Backup jobs

A backup job is the automated process of copying business data to a secure destination.

Support tasks include:
- checking job success or failure
- reviewing logs
- verifying retention periods
- testing restore operations
- confirming destination health

### Recovery objectives

- RPO = how much data can be lost
- RTO = how long the business can survive without the service

These objectives drive design decisions for backup and disaster recovery.

### Disaster recovery

A disaster recovery plan prepares an organization to restore operations after an outage, cyber incident, or major failure.

This can include:
- server recovery procedures
- offsite backup data
- failover systems
- remote office continuity
- communication plans

---

## Common IT support scenarios

### User cannot access the internet

Check:
- device is connected to Wi‑Fi or LAN
- valid IP address assigned
- gateway reachable
- DNS resolving properly
- firewall or VPN policy blocking traffic
- ISP or upstream communication issue

### User cannot reach the file server

Check:
- DNS name resolves
- network path reachable
- correct permissions
- file server online
- VPN connected if remote
- share mapping exists and is still valid

### Office wifi is unstable

Check:
- AP placement and coverage
- channel interference
- client roaming behavior
- switch port or AP health
- DHCP and connectivity errors
- recent configuration changes

### Printer is offline

Check:
- correct printer IP or hostname
- port status on switch or wall jack
- print server availability
- driver version
- queue stuck or drained
- IP conflict or network disconnect

### New employee cannot work on day one

Check:
- account created and active
- correct group memberships
- device joined to domain or enrolled
- email and VPN access configured
- required software installed
- printer and network shares mapped

### Backup failed overnight

Check:
- storage target free space
- backup credentials valid
- connectivity to backup server
- retention policy settings
- failed job log details
- restore tests or snapshot health

---

## Troubleshooting workflow

When a problem appears, the most effective support method is to isolate the source gradually.

### Step 1: determine scope

Ask:
- one user or many?
- one office or multiple?
- one app or whole network?
- local or remote access?

### Step 2: validate the basics

- the device has power
- network cable or Wi‑Fi is connected
- DHCP issued an IP
- the gateway responds
- DNS resolves names
- the user account is active
- the service is online

### Step 3: classify the issue

Possible categories:
- network connectivity issue
- device configuration issue
- identity/access issue
- file server or storage issue
- application or service issue
- security or policy issue

### Step 4: test likely causes

Useful checks:
- ping
- traceroute or tracert
- nslookup or dig
- verifying DHCP lease details
- checking switch port status
- confirming VPN state
- verifying file share permissions

### Step 5: document evidence

A solid support note should include:
- the time the issue started
- location and device name
- error description
- steps attempted
- results of tests
- whether any change was made

### Step 6: verify resolution

Before closing the ticket, confirm that:
- the original issue is resolved
- the user can access the needed service
- no additional side effects were introduced
- the change was documented

---

## Security and governance reminders

Even in day-to-day IT support, security is operationally important.

Key concepts:
- least privilege
- patched endpoints
- MFA enforcement
- login audits
- secure remote access
- device inventory
- software inventory
- permission review
- incident reporting

Bad support habits include:
- broad user access granted “just to fix it”
- shared local admin accounts without tracking
- no documentation for device changes
- ignored security alerts
- unvalidated backups

---

## Common IT tools and commands

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

### Linux / Unix

- `ip addr`
- `ifconfig`
- `ping`
- `traceroute`
- `nslookup` or `dig`
- `ss -tulpn`
- `df -h`
- `du -sh`
- `mount`

### Storage and backup checks

- verify backup completion logs
- check retention windows
- check restore validation
- inspect expired or failed jobs
- monitor disk capacity and usage growth

---

## Support terminology glossary

### Active Directory
A directory service used to manage users, computers, and permissions in Windows-based environments.

### DHCP
Automatic IP configuration used by clients to obtain network settings.

### DNS
Name resolution service that maps names to IP addresses.

### Endpoint
Any user device or system attached to the network.

### Firewall
A security control used to filter inbound and outbound traffic.

### NAS
Network-attached storage, usually used for shared files.

### VPN
A secure tunnel used to connect remote users or sites to the company network.

### Ticket
A tracked support request used to organize work and resolution history.

### Patch
A software update that fixes bugs or security vulnerabilities.

### Snapshot
A restore point saved at a specific time.

### Permissions
Rules that determine who can access a file, folder, or system resource.

### Authentication
The process of verifying a user or device identity.

### RTO / RPO
Recovery time objective and recovery point objective; used in continuity planning.

---

## Recommended learning path for company IT support

### Step 1: networking basics

Learn:
- IPs and subnets
- DNS and DHCP
- gateways and routers
- Wi‑Fi basics
- switch and firewall fundamentals

### Step 2: user and device support

Learn:
- Windows and Mac troubleshooting
- account setups
- printer support
- shared drive access
- VPN setup and troubleshooting

### Step 3: file and data management

Learn:
- file share permissions
- backup routines
- restore processes
- retention policies
- cloud storage access

### Step 4: security and operations

Learn:
- MFA
- password resets
- account lockouts
- patching
- access review
- ticket workflow and documentation

---

## A practical mindset for IT support

The best support engineers are not just “tech people.” They are problem solvers who understand business impact.

They know how to ask:
- what changed?
- who is affected?
- what service is failing?
- what layer is responsible?
- what is the most likely cause?
- what is the safest quick fix?
- how do we verify it worked?

This is what separates reactive troubleshooting from reliable support.

---

## Quick summary

Company computer networking and data management are the backbone of business IT support. The main responsibility of an IT support team is to keep users connected, permissions correct, data available, and services running without unnecessary disruption.

The most important skills are:
- understanding network basics
- diagnosing common user issues
- managing access and permissions
- handling file storage and backups
- validating service recovery
- communicating clearly to users and teams

These skills make IT support practical, resilient, and valuable to any business.

---

## Final note

This catalog is designed to be used as a real-world reference and operational guide. It is not just theory. It reflects the day-to-day work of a company IT support function: keeping devices online, users productive, data safe, and business operations stable.

The most useful support mindset is simple:

- know the network
- know the data path
- know who is allowed to access what
- know how to restore service safely
- document what happened and how it was fixed

That combination is the foundation of reliable business IT.
