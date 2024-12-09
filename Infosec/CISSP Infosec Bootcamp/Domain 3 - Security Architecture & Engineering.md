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

MLS systems employ **BIBA** or **Bell-LaPadula** too support different classifications

**Mandatory Access Control** - 

##### Bell-LaPadula

*WURD, Lattice Model*

![](Pasted%20image%2020241209120959.png)

##### Biba Model

*No WURD, Lattice Model* - deals with integrity levels

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

**Evaluation Assurance Levels**
- EAL 7 - Formally Verified, Designed, and Tested
- EAL 6 - Semi-formal, verified, designed, and tested
- EAL 5 semi-formal designed and tested
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

## 3.7 Methods of Cryptanalytic Attacks



## 3.8 Apply Security Principles to Site Design



## 3.9 Site/Facility Design Security Controls



## 3.10 Manage the Information System Lifecycle

