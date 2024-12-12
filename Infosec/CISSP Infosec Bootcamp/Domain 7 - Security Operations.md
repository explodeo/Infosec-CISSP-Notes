# Domain 7: Security Operations

## 7.1 Understand & Comply with Investigations 

#### Investigative Techniques

- Incident handling
- Interviewing
- **Root-cause Analysis**

#### Digital Forensics Procedures


**Digital Forensics Procedures**
- *Media Analysis* - backup disk first 
- *Network Analysis* (DLP/firewall logs)
- Software Analysis

##### Evidence Types

- Best evidence
- Secondary evidence
- conclusive evidence
- usable evidence
- direct evidence
- circumstantial evidence
- corroborative evidence

#### Chain of Custody

Need to apply a *chain of custody of evidence*

**Evidence life cycle**
- Collect
- analyze
- store/preserve/transport
- present in court
- return to victim

#### Requirements for Investigation Types
#weak_area 

*Requirements:*
- based on law or policy
- identifyu key entities
- define relationships among entities

**Investigations are viewed from these perspectives:**
- *Operational*
- *Criminal*
- *Civil*
- *Regulatory*

#### Types of Statutory Law
#weak_area 

**Criminal Law**
**Civil Law**
**Regulatory Law**


####  Compliance Requirements

**Regulatory Environment** - financial and privacy laws
**Audits** - Accountability and verify controls
**Reporting** - as required or requested

## 7.2 Conduct Logging & Monitoring Activities

#### Security Incident and Event Management (SIEM)

SIEM tools capture event logs from a multitude of devices and sensors into a centralized solution

#### Logging & Monitoring

**Continuous Monitoring and Tuning** via an ongoing process
**Egress Monitoring** - DLP systems
**Log Management** - collecting logs
**Threat Intelligence** on emerging threats

#### IDPS & SOAR

**Intrusion Detection and Prevention System (IDPS)** (read questions and know the difference:)
- *IDS*
- *IPS*

**Security Orchestration, Automation, and Response (SOAR)** - integrates tools and processes for automated incident response.

## 7.3 Perform Configuration Management

**Configuration Management** - Controls changes to hardware, software, and ensuring compliance with policies and standards

**Provisioning** - Installing assets and minimizing vulnerabilities

**Baselining** - capturing a system's configuration at a specific time for a starting point

**Versioning** - track changes in software modifications

#### Benefits of Baseline Provisioning

**Benefits**:
- COnsistency
- Efficiency
- Maintenance Reduction
- Security

*Immutable Architectures* - deploying unmodifiable systems/instances (think containers)

#### Serverless Computing & CM Implications

Serverless Computing does not require developers to maintain or provision asset infrastructure. (Think of cloud/containers)

*Configuration Management Impacts*
- Simplified Configuration
- Dynamic Scaling (scalability)
- Promote Resource Optimization
- Poses Challenges/Risks

## 7.4 Apply Foundational Security Operations Concepts

#### Key Terms

- *Need-to-Know Principle* - Use RBAC or MAC to employ strict AAA
- *Least Privilege Principle*
- **Segregation of Duties** - prevents catastrophes from a singular individual
- **Privileged Account Management (PAM)** - secure and monitor privileged accounts
- **Job Rotation** - shifting employee roles to mitigate insider threats and *promote cross-training*

#### Operational Security & Service Level Agreements

**Service Level Agreements (SLAs)** are contractual agreements between a client and provider

*Key SLA Elements:*
- incident response time
- uptime and availability
- patch management
- security monitoring
- data backup & recovery
- compliance requirements
- escalation procedures (for incidents)
- reporting and documentation

## 7.5 Apply Resource Protection

### Data-At-Rest

Using Encryption mechanisms to protect DAR:
- *Full-Disk Encryption* using TPMs or other **HSMs**
- BitLocker
- **Cloud computing (Control Keys)**

**Hardware Security Modules** perform encryption functions as an external module 9

### Data-in-Transit

##### Link Encryption

- Encrypt/decrypt data *at each node in the network*
- Done at *Layer 2*

##### E2E Encryption

- Source encrypts, Receiver decrypts
- *Examples:* 
	- **IPsec Tunnel Mode VPN**

## 7.6 Conduct Incident Management

### Incident Management Phases

#### Detection

- Use *IDS/IPS*, signature detection, etc. to ovserve system behaviors
- Follow up on threat intel
- system testing and auditing
- **Threat Hunting and Indicators of Compromise**

#### Response

**Response time ∝ Impacts + Costs**

CIRT/CSIRT - Incident Response Teams

#### Mitigation

**Common Mitigations**
- Isolation
- Temporary new controls
- monitoring
- address vulns
- suspend or revoke access

*Considerations*
- Volatile data preservation
- Critical Systems Prioritization
- Legal

#### Reporting

*Effective Reports Concepts:*
- Timely/Accurate Reporting
- Responsive to Requirements
- Adaptive to protect stakeholders and different project lifecycles
- Discretion in external reporting
- attentive to protective data (PII/PHI)

#### Recovery/Remediation

**Recovery Phase** - restore affected systems to normal functionality
**Remediation Phase** - address root causes and implement corrective measures

### Incident Response Frameworks

**Common IR frameworks & standards:**
- ***NIST 800-61*** - Computer security incident handling guide
- **ISO/IEC 27035**
- SANS Guidance
- CERT Publications
- ENISA Incident Handling Guide
- OASIS CIRT
- ISACA IRMF
- ITIL Incident response framework
- DHS CIRP

## 7.7 Operate and Maintain Detection & Preventative Measures


### Secure Network Architecture

**Demilitarized Zone (DMZ)** - a small network between internal and external network offering security and privacy

**Screened Subnet** - a network segment between the internal and external networks (Network DMZ)
- Use *Bastion Hosts* as hosts will be attacked

#### Firewalls

![](Pasted%20image%2020241212114219.png)

*Application Layer Firewall*
- does NAT/PAT and replaces IP/PORT with chosen ones
- Laggy, so it caches data

*Application Level Proxy Firewall*
- layer 7 firewall
- does stateful packet inspection
- anonymizes sender information
- HTTPS interceptor

**Web Application Firewall**
- proxy for web server
- reverse proxy does load balancing

#### IDS/IPS

Know that an IDS *monitors*, and IPS *prevents*
- NIDS - detection across network
- HIDS - installed on individual workstation

*Common IDS Techniques*
- Behavior / Anomaly
- Signature

#### Honeypots

Systems placed in a *DMZ* with many open ports/services with known vulnerabilities.

**HoneyNet** - 2+ honeyports simulating a network

**HoneyToken** - a file or component that generates an intrusion alert when accessed

**Padded Cell** - an isolate environment emulating a part of an internal network to isolate an attacker

##### Issues

- *Enticement* vs. *Entrapment*
- If a honeypot is too close to production, then it can leak realistic information

## 7.8 Patch & Vulnerability Management

#### Patch Management

**Patch Management Process (might be on the exam)**
1. Evaluation
2. Testing
3. Approval
4. Deployment
5. Verification

## 7.9 Change Management Process

###### Change Control Steps
1. *Request / Initiate*
2. *Review / Evaluate*
3. *Approve / Reject*
4. *Test & Validate*
5. *Implement*
6. *Review & Document*


## 7.10 Implement Recovery Strategies

**Business Continuity** - Maintaining *continuous* business critical operations

**Disaster Recovery** - restoration of IT ressources

**KNOW:**
- High Availability (HA)
- System Relilience
- QoS
- Fault tolerance

### Capacities Planning & Continuity of Operations 

**Continuity of Operations (COOP)** - techniques to keep organizations running in the event of a system failure

**Capacity Planning** - analyzing organizational requirements to meet business objectives
- *People* - Ensure Personnel are skilled
- *Technology* - tech supports business needs
- *Infrastructure* - resilient to demand

#### Backups

Use *Full site backups* stored off-site. *Failovers* allow temporary switching to a redundant system.

**Backup Types**
- *Full*
- *Differential* - backs up data since last full backup
- *Incremental* - backs up data since last backup of any kind

**Snapshots** - a saved state of operation

### Recovery Sites

![](Pasted%20image%2020241212135615.png)

**Hot Site** - fully operational site equipped with standard hardware/software

**Warm Site** - somewhere between hot/cold sites (may not have the software needed for restoration)

**Cold Site** - facility without the computer equipment in place to restore operation

## 7.11 Implement Disaster Recovery Processes

### Set Recovery Objectives
#weak_area 

#### Business Impact Analysis (BIA)

**BIA** is a method of gathering data to predict how system loss will affect a business.

###### Key Steps
1. *Identify Mission Essential Functions*
2. *Risk Assessment to determine risk exposure to critical systems*

###### Key Metrics

**Recovery Point Objective (RPO)** - Time to which data must be recovered after an outage (i.e last 12 hours must be available from backups)

**Recovery Time Objective (RTO)** - Length if time a system can be in the recovery phase before negatively affecting the business

**Maximum Tolerable Downtime** - maximum outage time 

*Mean Time Between Failures (MTBF)* - time it takes for a system to fail

*Mean Time to Repair (MTBR)* - time it takes to repair a system after failure

![](Pasted%20image%2020241212141937.png)


## 7.12 Test Disaster Recovery Plans

###### Incident Response Testing - Types & Formats

**Read-Through/Tabletop Exercise** - discussion to exercise/review incident response procedures & roles

**Walkthrough** - step-by-step review with key personnel to validate feasibility of responses

**Simulation** - Realistic scenario to validate operational readiness

**Parallel** - implement duplicate systems to run assessment in parallel with existing processes (test if parallel site is able to meet objectives)

**Full interruption**

## 7.13 Participate in Business Continuity Planning/Exercises

see above section

## 7.14 Implement & Manage Physical Security


## 7.15  Address Personnel & Safety Concerns

