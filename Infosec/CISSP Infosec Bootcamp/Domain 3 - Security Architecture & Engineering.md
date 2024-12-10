# Domain 3: Security Architecture & Engineering

## 3.1 Research, Implement, and Manage Engineering Processes

### Secure Design Principles

1.  **Planning security from the beginning**
2.  **Choose a framework of best practices** (see [Domain 1](Domain%201%20-%20Security%20&%20Risk%20Management.md))
	- NIST
	- COBIT
	- SABSA
	- ITIL
	- ISO 27001/2
3. **Develop Policies and Procedures**

#### Subjects and Objects

**Access Controls** control *Subjects* accessing *Objects*

*Subjects* - User, process, machine instruction. etc. An active entity that requests access to an object.

*Object* - Passive entity that contains information

#### Enterprise Security 

*Enterprise Security Architecture* - practice of applying processes and systems to align with organizational goals and strategic direction

DODAF - DOD Architecture Framework
TOGAF - The Open Group Architecture Framework
Zachman Framework
SABSA - Sherwood Applied Business Security Model

#### Systems Engineering Process

![](Pasted%20image%2020241209113152.png)

Apply threat modeling techniques during system design to scope risk

#### NIST System Development Lifecycle

![](Pasted%20image%2020241209113301.png)

See **NIST SP 800-64**, **NIST 800-100 Section 3.6**

**Phases of Software Development Life Cycle (SDLC)**  (pages 962-965 in the study guide)
- *Initiation* - define high-level requirements
- *Acquisition/Development*
- *Implementation/Assessment*
- *Operations/Maintenance*
- *Sunset (Disposal)*

```
For the exam, understand the steps and what happens at each stage
```

### Threat Modeling
#weak_area 
**Threat Modeling** - the process for attack simulation and threat analysis

**STRIDE** - Spoof, Tamper, Repudiation, Info Disclosure, DoS, Elevating Privilege
**PASTA** - Process for attack simulation and threat analysis

*See notes in* [Domain 1 - Security & Risk Management](Domain%201%20-%20Security%20&%20Risk%20Management.md)

*DREAD* - not used anymore since 2008

#### MITRE ATT&CK

https://attack.mitre.org/matrices/enterprise/

#### Cyber Kill Chain 

7 Steps:
1. XXXX

## 3.2 Understand Fundamental Security Concepts

#### Common Formal Security Models

**State Machine**
- Boot in a secure state
- Operate in a secure state,
- Fail to a secure state

**Lattice based** - MACs control access with *labels*. Users can access data if the subject's level is `>=` the object's

![](Pasted%20image%2020241209120735.png)

**Matrix Model**

*Non-Interference Model* - keeps users in their security contexts (MLS)

![](Pasted%20image%2020241209120713.png)


Information Flow Models

#### Multi-Level Security Model
#weak_area 

MLS systems employ **BIBA** or **Bell-LaPadula** too support different classifications

**Mandatory Access Control** - 

##### Bell-LaPadula

*WURD, Lattice Model*
- **Simple Security Property** - Reading data
- **\*-property** - writing data

![](Pasted%20image%2020241209120959.png)

##### Biba Model

*No WURD, Lattice Model* - deals with integrity levels
- **Simple Security Property** - Reading data
- **\*-property** - writing data

![](Pasted%20image%2020241209122207.png)

##### Clark-Wilson Integrity Model

*Requires Well-Formed Transactions*
Subjects interact with programs that interact with objects (*think APIs*)

![](Pasted%20image%2020241209123119.png)

*Clark-Wilson Model Rules*
1. All subjects must be identified and authenticated
2. Subjects can only execute authorized programs
3. Objects can only be updated by authorized programs
4. Events are Logged

##### Brewer & Nash Model

Prevents users from accessing too much information. Prevents a **conflict of interest**
- **Rule-Based Access Control (RBAC)**
- think of a firewall

*This model is used primarily to prevent insider trading*

![](Pasted%20image%2020241209124034.png)

##### Graham-Denning Model

Defines eight protection rights:
1. Create Object
2. Create Subject
3. Delete Object
4. Delete Subject
5. Read Access Right
6. Grant Access Right
7. Delete Access Right
8. Transfer Access Right

##### Harrison-Ruzzo-Ullman (HRU) Model

Maps a *matrix* of Subjects to Objects where each cell contains set of rights.
Think of linux capabilities

##### Take-Grant Model

How administrators pass on rights.

## 3.3 Select Controls Based on System Security Requirements

- Understand Security Requirements and Objectives
- Review Regulations, Financial Ops, Legal, Restrictions
- Apply RMF
- Leverage Control Frameworks

## 3.4 Trusted Computing Base

**TCB** - the total combination of mechanisms within a computer system

Security perimeters separate the trusted base from the rest of a system.

Kind of like a security kernel
![](Pasted%20image%2020241209140414.png)

#### System Self Protection Techniques
#weak_area 

Protection techniques are performed by the TCB

- **![](Pasted%20image%2020241209140641.png)**
	- process isolation
	- security domains
	- VMs
- **Layering and Data Hiding**
	- Levels of access to resources
	- **Protection Rings**

![](Pasted%20image%2020241209140617.png)

#### Reference monitor concept: Access Controls

**Security Kernel** - Components that enforce rules of the *reference monitor*
**Reference Monitor** - controls access between subjects and objects -- actions are audited and logged

## 3.5 Assess & Mitigate Vulnerabilities

### Database Systems

**DBMS** - Database Management system
- Oracle
- SQL Server
- MySQL
- MariaDB
- DB2

*DBA* - Database Admin

#### Database Integrity

**Entity Integrity** - each primary key is unique
**Referential Integrity** - cascading

 **Online Transaction Processing (OLTP)** - load balancing transactions
 **ACID Test**
 - *Atomic* - steps are completed successfully
 - *Consistent* - synchronize records
 - *Isolation* - transactions do not interfere with one another
 - *Durability* - transactions are verified

### Embedded Systems

Lots of devices use embedded systems. Do a risk assessment.

### Security Evaluation Frameworks

3rd party evaluation provides assurance using an objective common metric

#### Common Criteria Process

1. **Develop Protection Profiles (PP)**
2. **Build Product to meet PP - the Target of Evaluation (TOE)**
3. **Prepare a custom Security Target (ST)**
4. **Submit TOE, ST, and documentation to independent auditor**

![](Pasted%20image%2020241209160028.png)

#### Evaluation Ratings
#weak_area 

**Evaluation Assurance Levels**
- EAL 7 - Formally Verified, Designed, and Tested
- EAL 6 - Semi-formal, verified, designed, and tested
- EAL 5 - Semi-formal designed and tested
- EAL 4 - Methodically designed, tested, and reviewed
- EAL 3 - Methodically tested and checked
- EAL 2 - Structurally Tested
- EAL 1 - Functionally tested

## 3.6 Determine Cryptographic Solutions

#### Crypto Life Cycle

*Effective Cryptosystems:*
- maintain key secrecy
- uses strong algorithms
- use a large key space

### Data Hiding Strategies

- One-Time-Pad (OTP)
- Steganography

### Hashing Algorithms

**SHA** - Secure Hashing Algorithm
**HMAC** - Hash Message Authentication Code - encrypt hash with a secret key

### Symmetric & Asymmetric Cryptography

Think AES vs RSA

### Public Key Infrastructure (PKI)

**Certificate Authority** - A trusted third party provider that issues digital certificates to others
**Registration authority** - a licensed cert distributor which handles authentication, cert requests, and revocation

#### PKI Key Management Process

1. Key Generation
2. Certificate Generation
3. ID Verification (by CA/RA)
4. Key Distribution
5. Key Suspension
6. Revocation
7. Expiration
8. Renewal
9. Destruction

##### Key Recovery

*Key Escrow* - maintaining a backup for government use or if a user loses their copy
- *Key Recovery Agent (KRA)* - authorized parties that can recover from an Escrow
- *Separation of Duties* - TPI required for recovering key
- *Split Knowledge* - TPI

#### Digital Signatures

Focus on **Integrity** and **Non-Repudiation**

*Process*
1. Hash a file
2. Encrypt hash using private key
3. verify signature using public key

##### Digital Rights Management (DRM)

Components that control the distribution and control of documents and intellectual property

### Digital Certificates

**X.509** - Proves Identity

![](Pasted%20image%2020241209174213.png)

#### Certificate Revocation

**Certificate Revocation List (CRL)** - list of revoked or suspended certificate serial numbers

**Online Certificate Status Protocol (OCSP)** - a newer mechanism for identifying revoked certificates

#### Public Key Cryptography Standard (PKCS)

PKI Standards for Asymmetric Encryption and Digital Certs
- *PKCS#3* - DHKE
- based on FIPS standards


### Key Exchange

#### IPSEC - Secure Communications: VPN
#weak_area 

**Layer 2 Tunneling Protocol (L2TP)**
- **Authentication Header** - connectionless header protecting against replay attacks
- **Encapsulating Payload (ESP)** - provide confidentiality and anti-reply

IPsec uses **Internet Key Exchange (IKE)** for key exchange


#### SSL/TLS Public Key Infrastructure

*SSL* is older. use **TLS**. 
Process involves exchanging asymmetric session key 

![](Pasted%20image%2020241209180946.png)

#### Point-to-Point Tunneling Protocols

- HTTPS: Port 443
- SSL or VPN
- **TLS**
- RDP: port 3389
- **L2TP/IPsec**

## 3.7 Methods of Cryptanalytic Attacks

**Frequency Analysis
*Algorithm Errors*
**Dictionary Attacks**
**Social Engineering**
**Rubber Hose Attacks** - Extortion, bribery, threats of violence
**Birthday Attack** - reverse-hash matching

### Methods of Cryptanalytic Attacks  

**Chosen Plaintext** - IND-CPA
**Chosen Ciphertext** - IND-CCA
*Ciphertext Only* -IND-C2A
*Known-Plaintext* - guess the ciphertext
Implementation Attacks

**Birthday Attacks** - generating collisions 

## 3.8 Apply Security Principles to Site Design

### Site and Facility Design

#### Intruder Protection Concepts

*Deter, detect, delay, and respond* to intruders

***protect the people first***

**Layered Physical Access Control and Monitoring**
- **Match Access Design to Business Needs**
	- first, assess existing security
	- balance cost risk and convenience
- **Design controls to enforce *specific needs***

#### Deciding a Location

**Location considerations**
- natural disasters
- adjacent facilities / regulations

**hazards**
- burgulars

**Outside Assistance**
- public services, EMTs, etc

**Visibility**
- line of sight
- markings
- easy to find

#### Site Security and Risk Assessment

- Identify assets
- identify threats
- *Perform a site survey and develop a plan*

#### Appropriate Facility Attributes

**Fire Ratings** 
- **Class A** – Class A fires involve solid materials like wood, trash, and textiles. Ordinary combustibles. These fires are most familiar to us and are the most easily extinguished.
- **Class B** – Class B fires involve flammable liquids like gasoline, alcohol, diesel, or oil (not cooking oils). The volatility of the fuel source makes them more difficult.
- **Class C** – Class C fires involve electrical components and equipment as fuel sources. This includes fires started by faulty wiring in walls, circuit breakers, and appliances.

1. A **dry pipe system** contains compressed air that is released when the system is triggered, and opens a water valve that causes the pipes to fill and discharge water.
2. A *deluge system* is another dry pipe system that uses larger pipes and therefore a significantly larger volume of water. Deluge systems are not appropriate for environments that include electronic equipment.
3. A **preaction system** is a combination of dry pipe and wet pipe systems. The system exists as a dry pipe until the initial stages of a fire are detected and then the pipes are filled with water. The water is released only after the sprinkler head activation triggers are melted by sufficient heat. If the fire is quenched before the sprinklers are triggered, the pipes can be manually emptied and reset. Preaction systems are the most appropriate water-based system for environments that include both electronic equipment and personnel in the same locations.

## 3.9 Site/Facility Design Security Controls

### Doors & Locks

1. Something you have
2. Something you are
3. Something you know

### Fire & Safety Prevention

#### Early Fire & Smoke Detection

- **Smoke detection**
- **Heat detection**
- **Flame Sensor**
- Human Detection

#### Fire Suppression

##### Fire Extinguisher Types
#weak_area 

**Class A** - Ordinary combustible materials
**Class B** - Flammable or combustable liquids
**Class C** - electrical fires (*USE CO2*)
**Class D** - Combustible metals

##### Sprinkler Systems
#weak_area 

**Wet Pipe** - pressurized water pipe
**Dry Pipe** - Only air in pipes until valve is turned to feed sprinklers
**Preaction** - two-step dry pipe (ex: smoke detector then valves open)
**Deluge** - floods water/foam (best for manufacturing areas)

### Internal Facilities Security

##### Access Control Systems

- Prox Cards
- Smart Cards
- Access Control DB - logs
- Photo ID

### Physical Intrusion Detection

**Defense-in-Depth** - layered security
- *Guards*
- *Motion detectors*
- *Cameras*
- Intrusion detection systems (ex: magnetic doors, glass break sensors)

### Utilities and HVAC

#### Available & Reliable Utilities

**Service-Level Agreement (SLA)** - service contract

- supply redundancy
- communication systems
- heating/cooling/hvac
- fuel for heat

**Supervisory Control and Data Acquisition (SCADA)** are ICS systems consolidate monitoring of multiple control sources/sensors.

## 3.10 Manage the Information System Lifecycle

**Information Lifecycle Phases**
1. *Initiation Phase* - Define system objectives and scope
2. *Planning Phase* - Develop project plan and governance
3. *Analysis Phase* - Gather and Prioritize requirements
4. *Design Phase* - Create System Architecture
5. *Implementation Phase* - build, integrate, and test components
6. *Deployment Phase* - roll out and train users
7. *Operations and Maintenance Phase* - Provide monitoring and support
8. *Evaluation Phase* - Assess performance and gather feedback
9. *Retirement Phase* - Decommission system and ensure compliance