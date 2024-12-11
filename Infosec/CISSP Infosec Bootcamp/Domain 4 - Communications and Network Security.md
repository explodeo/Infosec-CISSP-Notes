# Domain 4: Communications & Network Security

## 4.1 Apply Secure Design Principles in Network Architectures

### The OSI Model

- Know what protocols operate at each layer (ex: TCP)
- Know what services map to each layer (ex: IPsec)

![](Pasted%20image%2020241210140948.png)

##### Common TCP/IP Ports

| Service | Port(s)|
|---------|--------|
| FTP     |  20,21 |
| SSH     |  22    |
| Telnet  |  23    |
| SMTP    |  25    |
| SMTP    |  110   |
| IMAP    |  993   |
| SNMP    |  161   |
| HTTP    |  80    |
| HTTPS   |  443   |
| **DNS** |  53    |
| *OSPF*  |  89    |

![](Pasted%20image%2020241210142611.png)


### IPv4 / IPv6

**IPv4** - 32-bit address
**IPv6** - 128-bit address, 64-bit network, 64-bit host
- *Link-Local address always begins with* `fe80::`
- *Zone ID* follows address to differentiate network segments (ex: `addr%ZID`)

###### Public & Private Address Ranges

**RFC 721**

| - | Public IP Range | Private IP Range | Subnet Mask |
|---|---|---|---|
| Class A | 1.0.0.0 to <br> 127.0.0.0       | 10.0.0.0 to <br> 10.255.255.255     | 255.0.0.0 (/8)      |
| Class B | 128.0.0.0 to <br> 191.255.0.0   | 172.16.0.0 to <br> 172.31.255.255   | 255.255.0.0 (/16)   |
| Class C | 192.0.0.0 to <br> 223.255.255.0 | 192.168.0.0 to <br> 192.168.255.255 | 255.255.255.0 (/24) |

### Secure Protocols

#### Layer 2 Tunneling Protocol (L2TP)

Sets up tunnel for two endpoints for VPN connections 
**Encapsulating Security Payload (ESP)** then encrypts the data.

##### IPsec

Composed of **AH** and **ESP**. 
- **Transport Mode** - Payload is protected
- **Tunnel Mode** - Entire packet is protected

###### IPsec Security Association (SA) Process

1. Device requests IPsec connection
2. **SA** handshakes for hashing and session keys
3. Each endpoint sets up a secure tunnel for each direction
4. each device auth/hash/encrypt/decrypt packets

###### IPsec Sub Protocols

**Authentication Header (AH)** - provides integrity and replay protection via seqnos
**Encapsulating Security Payload (ESP)** - encrypts and decrypts (symmetric) at endpoints
**ISAKMP** - secure key generation and exchange

### Converged Protocols

**Benefits of IP convergence:**
- class of service differentiation (VOIP vs Data Traffic)
- Quality-of-Service (QoS) and traffic prioriztization for real-time functions

#### MultiProtocol Label Switching (MPLS)

Used by ISPs to create private WANs across a network backbone
**MPLS uses a labeling technique** to encapsulate IP traffic

![](Pasted%20image%2020241210173501.png)

#### VoIP

- Susceptible to sniffing (*vishing*)
- requires **QoS** to be set up to prevent lag/jittering

##### Session Initiation Protocol & RTP
**Session Initiation Protocol (SIP)** - sets up and closes VoIP sessions
**Realtime Transfer Protocol (RTP)** - carry media payloads (separate port for *QoS*)

### Logical Segmentation

#### VLANs

VLANs are supported on switches compliant with **802.1q** 

**VLAN Tags** determine routing. Untagged packets are sent to VLAN 1.

### Wireless Networks

- Wi-Fi is defined by the 802.11 specification


#### Wi-Fi Security
#weak_area 

**802.11a/b/g/n/ac** are wireless standards for speed/freq and security
- 802.11a - 54Mb/s , 2.4GHz
- 802.11b - 11Mb/s , 5GHz
- 802.11g - 54Mb/s , 2.4GHz
- 802.11n - 100Mb/s , MIMO
- 802.11ac - 1Gb/s , 5GHz

**802.11i** defines enhanced security standards

- WEP uses *RC4 with a 24-bit IV*

- **WPA1/2 uses *802.1X* and *EAP* for authentication**
	- TKIP uses symmetric keys 
- **WPA3 uses *simultaneous authentication of equals (SAE)*** 

##### Authentication to WLAN

- Captive portal
- Pre-shared keys
- RADIUS/TACACS+

#### Wireless Network Detection

**Footprinting Networks**
- *Warwalking* - walking around to find networks
- *Wardriving* - car, laptop, and a GPS

#### Wireless Attacks

- **Impersonation** - spoofing
- **MitM** - man in the middle, "evil twin"
- **Flooding (DoS)**
- **Web Spoofing** - redirect browser
- **DNS Poisoning**
- **Smurf/Fraggle**

### Content Distribution Networks (CDN)

- avoid a single point of failure
- improve performance of file distribution/streaming
- increases reach, quality, and user exp.
- deployed as a large system of servers in LAN or WAN

#### Distributed Systems
#weak_area 

**Cloud computing**
- IaaS - Hardware as a Service
- PaaS - platform for developing software
- SaaS - distribute software

**Cloud Deployment Models**
- *Public Cloud* - use by public
- *Private Cloud* - used exclusively for organizations (may be on or off-network)
- *Community Cloud* - exclusive use by a common group of consumers/orgs (think Jira)
- *Hybrid Cloud* - combining two or more cloud infrastructures

#### Virtualization

*Hypervisor controls VMs through software*
- **Type 1** - Bare Metal
- **Type 2** - OS hypervisor

### Software Defined Networks (SDN)
#weak_area 

1. **Management Plane** - load balancers, security, etc
2. **Control Plane** - network hypervisor makes decisions and instructions
3. **Data Plane** - hardware 

**Properties of SDNs:**
- Directly Programmable
- Agile
- Centrally Managed
- Programmatically Configured
- Open standards/vendor neutral

## 4.2 Secure Network Components

### Endpoint Security

##### Cyber Hygiene

- good asset and *MDM* (mobile device management)
- educate users
- enforce strong passwords
- implement least privilege
- secure browsing and email practices

##### Attack Surface Management

- disable unnecessary services
- disable wifi/bt
- use application controls
- apply patches
- reduce removable storage
- device encryption

##### Securing Endpoint Communications

- Implement a **DLP** tool
- block attachments/links
- use a VPN or HTTPS
- email filtering
- secure browsing
- email encryption and signatures

##### Threat Detection & Response

- **Endpoint Threat Detection and Response (EDR)** tools
- monitoring
-  supply chain inventory
- attribute based access controls
- penetration testing

## 4.3 Implement Secure Communication Channels

- VPN Tools
- VoIP
- MPLS

