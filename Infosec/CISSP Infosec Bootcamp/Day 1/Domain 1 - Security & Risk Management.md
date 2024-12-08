## 1.1 Professional Ethics

**ISC 2 Code of Ethics Canons**
1. Protect Society, the commonwealth, and the infrastructure
2. Act honorably, honestly, justly, responsibly, and legally
3. Provide diligent and competent service to principals
4. Advance and protect the Profession

## 1.2 Understand and Apply Security Concepts

### CIA Triad

**Confidentiality** - no unauthorized disclosure of information
- have good access controls
- ***Identification, Authentication, Authorization***

**Integrity** - no unintentional modifications
- Least privilege driven by need-to-know
- Separation of duties
- Rotation of duties

**Availability and Reliability** - data/systems are available when needed
- implement redundancy

### 5 Pillars of Information Security

1. Confidentiality
2. Integrity
3. Availability
4. **Authenticity** - ensure *chain of custody* can be verified
	- code signing
	- *digital signatures*
1. **Non-Repudiation** - users cannot repudiate having performed an action
	- *digital signatures*

### Key Terms and Concepts

**IAM** - Identity and Access Management
**AAA** - Authentication, Authorization, and Accounting

## 1.3 Security Governance 

### Aligning Security & Organizational Objectives

#### Security Management Planning

*Developing Security Policies* - how do we maintain accountability
*Defining Security Roles*

#### Scoping and Tailoring

**Scoping** - Identify and document project objectives, requirements, and restrictions/limitations of a project
- Consider factors that affect achieving an objective

**Tailoring** - a customized solution to meet objectives 

These concepts are used to create a ***retention policy***

### Control Frameworks

A tool for *communication* and *Securiity Management*

### Standards for Security Governance

**ISO/IEC 27001** (Governance)
**ISO/IEC 27002** (Controls)
**CMMI** - Capability Maturity Model Integration

*These can be on the test, but may be* **distractors**:
***ITIL*** - IT Infrastructure Library best practices
***COBIT*** - Controls for IT regulatory compliance

### Security Governance Requirements

GOAL is to protect the privacy of data (**PII**):
- **GDPR** - EU General Data Protection Requirements

### Common Control Frameworks and Methodologies

#### ISO 27001

Information Security Management requirements for *governance*
- Guidance for deploying an **ISMS**
- Supplemented by **ISO 27002** which describes controls to administer 
- **Plan - Do - Check - Act** model

#### COBIT 
![](Pasted%20image%2020241208123235.png)

Elements of a security program:
- People
- Process
- Technology

##### Plan-Do-Check Model - COBIT

![](Pasted%20image%2020241208123358.png)

#### PCI-DSS Model

**Payment Card Industry (PCI) - Data Security Standard (DSS)** - a common set of industry tools/measurements to handle PII wrt. credit card purchases

![](Pasted%20image%2020241208123608.png)

#### Other Models and Frameworks

- Sherwood Applied Business Security Architecture (SABSA)
- **Capability Maturity Model (CMMI)**
- ITIL
- Six Sigma

### Assessment & Authorization

**Assess** a system is in compliance with security controls

**Authorization** is done by the *Authorizing Official* accepting or rejecting residual risk


For the exam know how these interact and the responsibilities of each. The exam does not use the proper names. 
- **Data Custodian** (Administrator)
- **Data Owner** (C-Level) also known as AO. 

## 1.4 Understand Legal, Regulatory, and Compliance Issues

**Due Care** - the degree of care a person would exercise under similar circumstances
- act responsibly to prevent breaches

**Due Diligence** - the duty to act professionally and legally
- evaluating risks and best mitigation practices (perform risk analysis)

### Liabilities

*Negligence* - Not performing *due diligence and due care*

**Downstream Liabilities** - negligence (when a company offers assets external and a third party abuses it)

#### Legal Liability

**Legally-Recognized Obligation** - a standard exists that protects others from unreasonable risks

##### Types of Common law

**Proximate Causation** - Negligence that can be proven (plaintiff/defendant cases)

**Violation of any law**

Violation of due care (unreasonable actions)

Violation of privacy (PII leaks)

#### US Legal & Regulatory Compliance

*Sarbanes-Oxley (SOX)* - financial recordkeeping accuracy
*Basel III* - international banking
*Gramm-Leach-Bliley Act (GLBA)* - banking consumer privacy

###### `AUDITING TESTS COMPLIANCE`

### Protecting Privacy

**Fair Information Practice Principles (FIPPs)**
Many laws exist to protect (PII). Organizations have an **Acceptable Use Policy**

#### General Data Protection Regulation (GDPR)

- Lawful Processing
- Right to be Informed
- Right to Access
- Right to Recertification
- Right to Erasure
- Right to Data Portability
- Right to Object
- Rights related to automated decision making (right to talk to a human)
- Breach Notification within 72 hours
- Transfer of Data Permission

#### HIPAA

**Security Rule** - requires safeguards to protect *confidentiality* and *integrity* of PHI 

**Privacy Rule** - requires written consent to share data

*Transaction Rule* - standardized formats for electronic record transmissions between parties

### Licensing and Intellectual Property Requirements

#### Statutory (Written) Law

**Administrative Law** - regulations/contract violations
**Civil or Tort Law** - legal suits over damages
**Criminal Law** - violations of federal or state law 
**Intellectual Property Law** - protects against piracy and license violation

### Import/Export Controls

International Traffic in Arms Regulations (ITAR)
Export Arms Regulation (EAR)

## 1.5 Understand Requirements for Investigation Types

Understand why these privacy laws exist in [Section 1.4](#1.4-understand-legal,-regulatory-and-compliance-issues)
## 1.6 Develop, Document, and Implement Security Policy

### Security Policies

**Security Policy Categories**
- Regulatory
- Advisory (most policies)
- Informative

**Security Policy Types**
- *Organizational* - organization-wide aspects *(Program Policies)*
- *Issue-Specific* - addresses a particular security issue (ex: acceptable use policy)
- *System Specific* - secure handling of specific systems or system types

![](Pasted%20image%2020241208152745.png)

See **NIST SP 800-12: 1995 NIST IT Security Standard**

#### Functions for Supporting Policies

- **Standards** - (binding/mandatory) Stanardization of practice or baseline (ex: comply with ICD 503)
- **Procedures** - (binding/mandatory) steps to comply with specific tasks
- **Baselines** - (binding/mandatory) actions to achieve a specific task
- **Guidelines** - recommendations / non-binding

##### For the Exam

Focus on policies to prevent risks from being realized again and to hold someone accountable

## 1.7 Identify, Analyze, Assess, Prioritize, and Implement Business Continuity Requirements

See [Domain 7 - Security Operations](Domain%207%20-%20Security%20Operations.md)

**Business Continuity Planning**
1. Identify
2. Analyze
3. Assess
4. Prioritize
5. Implement
6. Continuous Improvement

## 1.8 Personnel and Security Policies and Procedures

### Employee Policies: Human Resources

**Pre-Employment**
- onboarding process

**Termination Procedures**
- NDA review
- surrender equipment/credentials
- conduct exit interview

### Personnel Security
- Employee Agreements & Policies
- Security Education, Training, and Awareness
- Clear Acceptable Use Policies (AUP)
- Privacy issues and employee monitoring

## 1.9 Understand and Apply *Risk Management* Concepts

### Security Risk Concepts

**Risk** - a threat or potential of a threat being realized. Measured in:
- **Likelihood** 
- **Impact**

**Vulnerability** - weakness of an asset
- Asset - a resource of value

**Threat** - Potential danger

**Control** - safeguards or countermeasures

#### Risk Management

The process of identifying, analyzing, and reducing risks to acceptable levels

1. **Risk Assessment**
2. **Risk Mitigation - Reduction Analysis**
3. **Control Evaluation - Continual**

#### Risk Management Framework

RMF *aligns risk appetite (tolerance) and business strategy*.

##### Generic RMF Process
![](Pasted%20image%2020241208161111.png)

#### Risk Assessment & Management Models

**NIST SP 800-30** - USG Guide to conducting risk assessments
**NIST SP 800-37** - RMF for Information Systems and Organizations
**NIST SP 800-39** - Managing Information Security Risk

Other Models:
- *OCTAVE*
- *CRAMM*
- *SOMAP*
- *VAR*

### Assessing Risk

#### NIST SP 800-30

**Step 1: Prepare for Risk Assessment:**
- Identify a risk assessment *purpose*
- Identify a risk assessment *scope*

**Step 2: Conduct the Risk Assessment**
- *Identify* threats, events, vulns
- *Risk Assessment and Analysis*
- *Risk Assignment / Transfer*
- *Control Selection*

**Step 3: Communicate and Share Risk Assessment Results**
**Step 4: Maintain Risk Assessment**

#### Risk Analysis

**Quantitative** - evaluate risk based on amount of damage in a dollar value
**Qualitative** - subjective rating based on the *Delphi method*, a group decision method

##### Steps for Qualitative Risk Analysis

1. Develop risk scenarios
2. Gather experience from SMEs
3. Walk through scenarios to determine results
4. Build consensus for best countermeasures
5. Use the *delphi* method to communicate anonymously

##### Risk & Mitigation Calculation

**Asset Value (AV)** - estimate of the asset's value
**Exposure Factor (EF)** - percentage of value lost in an incident

**Single Loss Expectancy (SLE)** - `SLE = AV x EF` - estimate of loss in a single incident

**Annualized Rate of Occurrence (ARO)** - Probability an incident occurs in a year

**Annualized Loss Expectancy** - `ALE = SLE x ARO` - estimate of loss in a year

```
Goal is to compare annualized control costs versus potential loss.
```

###### Cost Benefit Analysis Formula

`Control Value = ALE (before implementing control) - ALE (after implementing control) - Control Cost`

#### Identifying Types of Risks

- *Total Risk* - risk before controls
- **Residual risk** - risk after implementing controls
- *Accepted risk*

![](Pasted%20image%2020241208164407.png)

### Managing Risk

###### RMF STEPS (KNOW FOR EXAM)

Mnemonic - CSI AAM - CSI Anti Aircraft Machine 

1. **Prepare** - create context and priorities for managing risk
2. **Categorize** - understand threats that can affect system CIA
3. **Select** - appropriate set of controls
4. **Implement** - security controls
5. **Assess** - security controls
6. **Authorize** - DAO approves
7. **Monitor** - Continuous

#### Risk Responses

**Risk Mitigation** - reduce risk by implementing controls
**Risk Acceptance** - do not implement countermeasures
**Risk Avoidance** - changing activity to avoid the risk (ex: hot glue)
**Risk Transference** - transfer risk to another entity (ex: purchasing insurance)

#### 7 Common Control Categories

*Need to know the category a control belongs to for the exam.*

1. **Directive Controls** - SOPs
2. **Deterrent Controls** - deters malicious use
3. **Preventative Controls** - prevents unwanted activity
4. **Compensating Controls** - make up for deficiencies in other controls
5. **Detective Controls** - detects and sends warning when discovering 
6. **Corrective Controls** - modify conditions that *allowed* an incident
7. **Recovery Controls** - restore system back to normal after an incident

#### 4 Common Control Types

1. **Administrative Controls** - policies & procedures
2. **Physical Controls** - physical security
3. **Logical/Technical Controls** - digital protections
4. **Regulatory/Compliance Controls** - mandated by law

## 1.10 Understand and Apply Threat Modeling Concepts

### Threats / Threat Agents

**Threat** - potential danger to an asset

**Threat Agent** - anyone or anything that can realize a threat

#### Types of Threats
- Natural
- Human
- Environmental

#### Some Threats to Security

*Confidentiality*
*Integrity*
*Available*

### Threat Modeling

Performed during the early stages of the SDLC.

**Common Threat Modeling Frameworks**:
- **STRIDE**
- **PASTA**
- *Kill Chain Analysis*
- DREAD
- Attack Trees
- etc.

## 1.11 Apply Supply Chain Risk Management (SCRM) Concepts

Third-Party Governance may result in shared **downstream liability** or other risks from third-party relationships.

#### Service Level Agreement (SLA)

**Service Level Agreement (SLA)** - a contract defining the responsibilities, penalties, remedies, situations, for a provided service

SLA metrics are monitored and audited:
- service availability
- defect rates
- technical quality
- security
- Carrot & Stick: rewards/penalties for good/bad service

*FOR EXAM: Understand the purpose of SLAs limit the risk exposure to an organization*

#### MOU & ISA

**Memorandum of Understanding (MOU)** - agreement to accomplish a goal or mission

**Interconnection Security Agreement (ISA)** - agreement documenting technical requirements to exchange sensitive data

## 1.12 Establish and Maintain Security Awareness, Education, & Training

