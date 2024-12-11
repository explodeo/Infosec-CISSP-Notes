# Domain 5: Identity & Access Management (IAM)

## 5.1 Control Physical & Logical Access to Assets

### Access Control Mechanisms

**Administrative Controls** - Management controls (policies, standards, etc)

**Technical Controls** - Protect data and resources

**Physical Controls** - Protect from physical damage

### Access Control Definitions

**Subject** - Active entity requesting access
**Object** - Passive entity containing information
**Access** - ability of the subject to do something (rwx)

**Access Control** - security features controlling *Access*

### Access Control Steps

1. **Identify all subjects**
2. **Authenticate Subject**
3. **Authorization of Interaction** (determine resource access and allowed operations)
4. **Accounting**  (Logs)

## 5.2 Design Identification and Authentication Strategy

### Identification

*Identification* - the process which a subject professes an identity and 
*accountability* is initiated
- **1-N Matching for biometrics**

### Authentication

**Factors:**
- something you know
- something you have 
- something you are

Know **2FA**, **mutual authentication**, and *authentication methods* 

- **1-1 Matching for biometrics**

*One Time Passwords*
- OTP
- HOTP

#### Crossover Error Rate (CER)

**False Negative Rate - Type 1 Errors**
**False Positive Rate - Type 2 Errors**

**CER** identifies the failure rate 

### Authorization

#### Access Criteria

- need to know
- clearance
- least privilege
- default no access


#### Remote User Authentication

**802.1x** - Enterprise Authentication
- Central AAA server (**RADIUS or TACACS+**)
- Digital certs for *mutual authentication* (**PEAP**)

RADIUS and Kerberos both do AAA

### Accounting

Logging and Audit trails

**Know what a SIEM, IDS, IPS, and a SOAR system are and what they do**

### SAML

An XML-based language for *exchanging authentication and authorization data*.
- SAML uses HTTP POST
- Allows for SSO in a federated system
- Think of X.509 certificates (JSON)

### Single Sign On (SSO)

**When thinking of SSO, think SAML**

#### Kerberos

**Kerberos Components**
- Key Distribution Server (KDC)
- *Authentication Server (AS)* - authorizes user to request tickets
- *Ticket Granting Service (TGS)* - seucres and issues tickets to authenticated users

## 5.3 Federated Identity with Third-Party Services

**Examples:** OKTA, OAuth,, Azure AD, Ping Identity
- These use *SAML* for authentication. 
- These implement SSO using browsers

## 5.4 Implement & Manage Authorization Mechanisms
#weak_area 

##### Role Based Access Control (RBAC)

RBAC allows objects access using *roles* in a company (i.e. jobs)
- *Example:* Assigning users to an **Administrators Group**

##### Rule Based Access Control (RBAC)

A *dynamic model* where access is based on *rules* based on conditions applied to every action
- *Example:* Switch ACLs or firewall rules

##### Mandatory Based Access Control (MAC)

A *Lattice Model* based on *security levels* (i.e security clearance and classification). Access is decided and controlled by administrators
- *Example:* SELinux MLS labels

##### Discretionary Based Access Control (DAC)

DAC is where an *owner/creator* assigns access to resources
- *Example:* OneDrive file access 

##### Attribute Based Access Control (ABAC)

Access rights based on policies that define attributes (if-then rules)
- **Key Criteria:**
	- Enables fine-grained Access Control
	- Policies may be simple or complex
	- Access rights are granted via policies combining attributes

- *Example:* think scattered castles and compartments

ABAC prevents users from interfering with each other.

## 5.5 Manage the Identity & Access Provisioning Cycle

**Provisioning** - setting up access to meet a need/requirement
*User provisioning is unique to each business*

### Access Provisioning Models

**Role-Based Provisioning** - job title defines basic needs

**Request-Based Provisioning** - generally supports DAC/MAC where approved requests are auditable

**Hybrid Provisioning Model** - combines request/role based approaches

##### Identity & Access Provisioning Lifecycle
1. *Account Maintenance*
2. *Review & Audit*
3. *Revocation or Termination* (De-provisioning)

![](Pasted%20image%2020241211155609.png)

## 5.6 Implement Authentication Systems

### Access Control Techniques

- **Restrict user interfaces** - no shell access
- **Content-dependent Access** - access determined by sensitivity
- **Context-dependent access** - access determined by sequence of events

### Access Control Matrix 
#weak_area 

- **Capabilities** - Identifies subject's access rights
- **Profiles** - list of objects associated with each subject

![](Pasted%20image%2020241211160511.png)


### Access Control on the Internet

- XML
- **SAML**
- **OAuth**
- OpenID
- OIDC

### Access Control In-Network

- Kerberos
- RADIUS
- TACACS+