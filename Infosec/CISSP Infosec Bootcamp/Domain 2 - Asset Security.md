# Domain 2: Asset Security

## 2.1 Identify and Classify Information & Assets

### Employing Resource Protection

- maintain CIA
- authenticity controls

### Asset & Media Management

**IT Access Management (ITAM)** - business practices to support life cycle management
**Data Loss Prevention (DLP)** - deploy sensors inside an environment to prevent data exfiltration

Use **syslog** to centrally record log files

Employ a **Configuration Management Database (CMDB)**

#### Maintain Data Integrity and Accuracy

**Quality Assurance (QA)** - assess quality based on external standards
**Quality Control (QC)** - assess quality on internal standards

### Data Security Controls 

**Baseline Protection** - establish a minimum set of safeguards

Step 2 of the RMF process selects *baseline security controls* based on *system categorization*

**FIPS 199** - Standards for Security Categorization of Federal Information and Information Systems
**FIPS 200** - Minimum Security Requirements for Federal Information and Information Systems

**Best Practices**
- App Whitelisting
- Use a baseline configuration
- Apply patches within 48 hours
- Enforce Least Privilege

## 2.2 Establish Information & Asset Handling Requirements

#### Data/Asset Classification & Handling

Handling: CIA protections, protecting DiT
Storage: Protecting data at rest
Destruction: destroy unnecessary media

#### Need to Know and Least Privilege

Need-to-Know is driven by least privilege

#### Separation of Duties (SoD)

- reduces employee fraud and access abuse
- dual-control / two-man rule

## 2.3 Provision Information & Assets Securely

### Information Ownership and Data/Asset Roles

- **Security Administrators** - oversee daily security operations
- **Business/Mission Owners** - Responsible for ensuring data/assets align with org. goals/objectives
- **Data Owner** - responsible for determining classification, protection, and acceptable use
- **Data Custodian** - help ensure data is properly stored and protected 
- **Data Controller/Processor** - a system, service, or individual used to control/process data
- **System Administrators/Owners** - manages assets to ensure compliance with security policies/procedures
- *Data Steward* - responsible for the utility and accuracy of data
- *Users/Subjects*

**Authorizing Official (AO)** - The official formally assuming responsibility for risk. May be delegated (DAO). 

### Asset Inventory

Organizations have both *Tangible Assets* like hardware and *Intangible Assets* like intellectual property.

**ITIL** defines a **Configuration Management Database (CMDB)**

## 2.4 Manage Data Lifecycle

### Data Roles and Location

Refers to the location of data including backups and copies.

**Data Sovereignty** - once data is gathered/stored, it is subject to the local laws, rules, and regulations

### Data Retention

- *Records Retention* - governs the min/max periods of time records are retained and their availability
- **Proper Labeling** - classification & availability

Use *Scoping and Tailoring* to develop a **Records Retention Policy**
![](Pasted%20image%2020241209105331.png)

### Data Remanence & Destruction

**Data Remanence** - residual information remaining on storage media



#### Data Remanence Countermeasures

Clearing - deleting and rewriting to prevent simple attacks

Purging - data sanitization (Data sanitization standards defined in NSA/CSS 9-12)
- **Encryption**
- **Degaussing**
- **Overwriting (zeroize)**
- **Destruction** 

## 2.5 Asset Retention

### Asset EOL/EOS

**End-of-Life**
**End-of-Support**

#### Best Practices
- Inventory Management
- System Lifecycle Policies
- Change Management
- Replacement Criteria
- Vendor Communication/SLA
- Data Access/Remnance
- Continuous monitoring

## 2.6 Security Controls & Compliance Requirements

#### Common Data and Information Protection

- **Digital Rights Management (DRM)** - Usage rights for digital content
- **Data Loss Prevention (DLP)** - prevents data exfiltration
- *Encryption* - turn plaintext into ciphertext
- **Information Rights Management (IRM)** - data usage rights for documents and sensitive data
- **Cloud Access Security Broker (CASB)** - manages, secures, standardized access to cloud apps and data (CSP does the key management)

#### Data State Controls & Requirements

- **Data in Transit** - 
	- *Ex:* TLS/SSL, VPN, IPsec
- **Data At Rest** - Data stored on storage media
	- *Ex:* AES/RSA, Strong Access Controls
- **Data in Use** - data being accessed, processed, or manipulated by users
	- *Ex:* Endpoint security application, physical controls, secure coding practices

#### Scoping & Tailoring Security Policies

**Scoping** - identify scope
**Tailoring** - customization

**Metrics** - measurable goals and performance / auditing
- **Key Goal Indicators (KGI)** - goal an organization aims to achieve
- **Key Risk Indicators (KRI)** - metric measuring likelihood and impact of a risk
- **Key Performance Indicators (KPI)** - quantifiable metric showing progress toward specific objectives