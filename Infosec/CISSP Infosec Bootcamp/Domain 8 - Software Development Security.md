# Domain 8: Software Development Security

## 8.1 Integrate Security in SDLC

**Security By Design** embeds security from the start
1. Analysis
2. Design
3. Implement
4. QA Testing
5. Deployment
6. Maintenance

**Key Components**
- *Proactive*
- *Implement secure defaults/failure states*
- *security from the start*
- *Aligns requirements*
- *promotes visibility & Transparency*

## 8.2 Identify & Apply Security Controls in Software Development Ecosystems

**Protect Development Pipelines**

- Access Control
- Secure SDLC
- Change Control & Cyber Governance
- Code Reviews & Static Analysis
- Secure Coding Practices
- Dependency Management
- Security Testing
- Backup & Version Control

#### Capability Maturity Model (CMM/CMMI)

**Capability Maturity Model (CMM)** is a development improvement process (leverages *Agile Methodology*)

The goal is to implement mature, vetted engineering techniques

##### CMM's Five Levels of Maturity
#weak_area 

1.  **Initial** - Processes are unpredictable and reactive (increases risk)
2. **Repeatable** - Repeatable processes are used and repeatable results are expected from similar projects
3. **Defined** - developers operate according to SW development processes
4. **Managed** - Quantitative measures are used to understand the development process
5. **Optimizing** - CI/CD is integrated

#### Software Assurance Maturity Model (SAMM)

**Software Assurance Maturity Model (SAMM)** is an open source framework to enhance security practices across five key business functions

##### SAMM Key Business Functions
#weak_area 

**Governance** - activities org. takes to manage SW development
**Design** - process used to define SW requirements
**Implementation** - actually building code
**Verification** - testing
**Operations** - maintain CIA through the SDLC

![](Pasted%20image%2020241212152255.png)

#### IDEAL Model

*IDEAL* - Initiating, Diagnosing, Establishing, Acting. Learning

## 8.3 Assess the Effectiveness of Software Security


#### General Software Testing Types

Know **White/Gray/Black Box** testing

**Static Application Security Testing (SAST)** - static code analysis

**Dynamic Application Security Testing (DAST)** - runtime testing

**Interactive Application Security Testing (IAST)** - provides feedback during application testing

#### Common Tests for Software Effectiveness

- Penetration Testing
- Vulnerability Scanning
- Code Review/SAST
- DAST
- *Composition Analysis* - examine underlying libraries
- Security Architecture Review - ensure best practices are in use
- Threat Modeling
- Compliance Based Assessment

## 8.4 Assess Security Impact of Acquired Software

Understand vetting software is important.

**Common Tools for Review**
- MITRE
- OWASP
- CMMC

## 8.5 Secure Coding Guidelines & Standards

**Common Secure Coding Frameworks**
- OWASP
- NIST 800-64
- ISO/IEC 27034
- CIS Benchmarks
- IEEE 2178
- CERT Secure Coding Standards

**Common Attacks to Know**
- BOF
- CSRF/XSRF/XSS
- SQLi
- TOC/TOU

Also know secure APIs

### Software Development Methods

#### Agile

Uses things like scrum, timebox, and "iterative process"

#### Waterfall

Discrete phases with ability complete each phase before flowing down

#### Spiral Model

Cyclical model combining prototyping 