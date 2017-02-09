# WIP_network-handbook

## CompTIA+ Certification  

Entry level certification

## Comptia Network + Objectives N10-006
  
- See PDF
- Navigate to Pearson VUE in For test takers tab (https://home.pearsonvue.com/)
- CompTIA blueprint will list the metadata of the exam
- Not all multiple choice questions
- Passing is 720 and above from scale 100-900

## 1. Network Architecture for CompTIA Network+

- Introducing network devices
- Understanding network services and applications
- Configuring network services and applications
- Understanding WAN technologies
- Installing and terminating network cables and connectors
- Differentiating between common network topologies
- Differentiating between common network infrastructures
- Implementing a network addressing scheme
- Understanding routing concepts and protocols
- Introducing unified communication technologies
- Comparing cloud and virtualization technologies
- Implementing a basic network

## 1.1 - Explain the Functions and Applications of Various Network Devices 

- Core connectivity devices
- Security devices
- Special purpose devices

### Hub
- Works at OSI Layer 1 (Physical)
- Hubs are multiport repeaters
  * Regenerate the signal  
- One big collision domain
- Good for network diagnostics and nothing else

### Switch
- Successor to the bridge
- Works at OSI Layer 2 (Data Link)
  * Can also function at OSI Layer 3 (Network)
- Switches store an in-memory MAC (aka media access control) table and provide dedicated bandwidth to each port (collision domain)

### Router
- Operates at OSI Layer 3 (Network)
- Seperate entire networks
- Modular design (especially Cisco)

### Wireless Acess Point
- Provides IEEE 802.11 connectivity
- Many support Power over Ethernet (PoE)
  * IEEE 802.af specifies 15.4W power
- Wireless LAN controllers
  * Centralized management of many WAPs
  
### Ethernet Domains
- Hub
  * One collision domain
- Switch
  * Four collision domains
- Router
  * Four broadcast and collision domains

### Configuring a Router
- VMWare or Virtualbox will allow for creation of computer and aoppliance instances in software
  * Vyos
  
    `$ show int`   
    `$ config`   
    `# set interfaces ethernet eth0 address 10.0.0.254/24`   
    `# save`   
    `# ping 10.0.0.254`   
    `# clear`
    
  * Ability to use tab completion with various CLI's
  * NOTE - Always ensure that you save configuration changes. A common beginner's mistake is making configurations and not saving the changes
  
### Security Devices
- Firewall
  * Exist as software or hardware varieties
  * Selectively allow or block network traffic
    - IP addresses, port numbers - packet-filtering firewall
  * Stateful packet inspection - Identifies sessions and can enforce rules on high level applications and services
  * Serves as a gatekeeper
- Intrusion Detection
  * Intrusion Detection System (IDS) - Passive detection of network traffics
    - Also called NIDS
  * Host-Based IDS (HIDS) - Protects local computer (Tripwire)
  * Intrusion Prevention System (IPS) - Active prevention of network attacks
  * Threat detection often involves signatures and anomolies
- Proxy/Cotent Filter
  * Forward proxy: Hides internal computers IP addresses from the internet
  * Reverse proxy: Publishes internal applications to the internet
  * Proxy provides security and sometimes content caching
  * Content filters use a subscription service (WebSense) to classify web content
  * Generally network devices often combine different but related functions as a all in one operation
- Remote Access and Performance Devices
  * Analog Modem
    - Modulate digital signals to anaolg for transmission over phone lines
    - Receiving modem demodulates analog to digital
    - Modems can have a purpose today
      * Special-purpose equipment that already uses a modem to send small amounts of data
      * "If it ain't broke, don't fix it"    
  * VPN Concentrator
    - Provides dedicated hardware circuitry to host virtual private network (VPN) connections
    - VPN protocols (tunneling and encryption) can be resource intensive
    - Server software can provide VPN services, with decreased cost but also decreased performance and scale
  * Load Balancer
    - Distributes incoming network traffic across multiple nodes
    - Load balancing gives users a faster experience
    - Load balancing is a way of providing high availability (HA)
  * Packet Shaper
    - Prioritize network traffic based upon your business rules
    - Ensures that certain types of traffic always have adequate bandwidth
    - Also ensures that low-priority traffic gets squashed to avoid DoS
    
### Load Balancing in Action Demonstration
  `C:\> ping -4 www.google.com`   
  `C:\> nslookup www.google.com`   
- We use nslookup to query Domain Name System (DNS) servers for informational or troubleshooting purposes
  
### Network Applicances with GUI Demonstration
- Web graphical interfaces (GUIs) are populare because you can get to them from almost anywhere, provided you have a web browser

### The Rack Unit
- Most enterprise servers come as rack mounted appliances
- Mount to rack by rails and "ears"
  * 1U standard is 1.75 inches or 44mm
  * Average rack is 42U or 19 inches wide (483mm)
  
## 1.1.Z - Appendix

### Useful Links
- Understanding Network Hubs -> (http://www.techiwarehouse.com/engine/5ea76190/Understading-Networking-Hubs)
- Network Bridges -> (http://compnetworking.about.com/cs/internetworking/g/bldef_bridge.htm)
- Network Switch -> (https://en.wikipedia.org/wiki/Network_switch)
- Difference Between Hubs, Switches, and Routers -> (http://www.webopedia.com/DidYouKnow/Hardware_Software/router_switch_hub.asp)
- How Does a Network Switch Work? -> (http://www.cisco.com/cisco/web/solutions/small_business/resource_center/articles/connect_employees_and_offices/how_does_a_network_switch_work/index.html)
- Networking Basics - What You Need to Know -> (http://www.cisco.com/cisco/web/solutions/small_business/resource_center/articles/connect_employees_and_offices/networking_basics/index.html)
- Router (Computing) -> (https://en.wikipedia.org/wiki/Router_%28computing%29)
- Router Hardware 101 -> (http://lifehacker.com/5830886/know-your-network-lesson-1-router-hardware-101)
- Understanding Routing -> (http://www.enterprisenetworkingplanet.com/netsp/article.php/3607381/Networking-101-Understanding-Routing.htm)
- Wireless Access Point (https://en.wikipedia.org/wiki/Wireless_access_point)
- Access Point, Wireless (http://compnetworking.about.com/cs/wireless/g/bldef_ap.htm)
- Configuring a Wireless Access Point (http://www.dummies.com/how-to/content/configuring-a-wireless-access-point.html)
- Power over Ethernet (PoE) -> (https://en.wikipedia.org/wiki/Power_over_Ethernet)
- PoE Explained -> (http://www.veracityglobal.com/resources/articles-and-white-papers/poe-explained-part-1.aspx)
- Piet Mondrian -> (http://www.theartstory.org/artist-mondrian-piet.htm)
- Collision Domain -> (https://en.wikipedia.org/wiki/Collision_domain)
- Broadcast Domain -> (https://en.wikipedia.org/wiki/Broadcast_domain)
- Collision Domains vs. Broadcast Domains -> (http://ciscoskills.net/2011/03/30/collision-domains-vs-broadcast-domains/)
- Collision & Broadcast Domains -> (http://study-ccna.com/collision-broadcast-domain)
- VMware Workstation -> (http://www.vmware.com/products/workstation)
- VMware Solution Exchange (Virtual Appliances) -> (https://solutionexchange.vmware.com/store)
- Oracle VM VirtualBox -> (https://www.virtualbox.org/)
- VyOS Virtual Router -> (http://vyos.net/wiki/Main_Page)
- Firewall (Computing) -> (https://en.wikipedia.org/wiki/Firewall_(computing))
- Stateful Firewall -> (https://en.wikipedia.org/wiki/Stateful_firewall)
- What is Stateful Inspection? -> (http://www.webopedia.com/TERM/S/stateful_inspection.html)
- HIDS/NIDS -> (http://searchsecurity.techtarget.com/definition/HIDS-NIDS)
- HIDS -> (https://en.wikipedia.org/wiki/Host-based_intrusion_detection_system)
- NIDS -> (https://en.wikipedia.org/wiki/Intrusion_detection_system)
- IPS -> (https://en.wikipedia.org/wiki/Intrusion_prevention_system)
- Tripwire HIDS -> (http://www.tripwire.com/)
- Proxy Server -> (https://en.wikipedia.org/wiki/Proxy_server)
- Content Control Software -> (https://en.wikipedia.org/wiki/Content-control_software)
- Websense Content Filter Appliance -> (https://www.websense.com/content/v-series-appliances.aspx)
- Using the PING Command -> (https://technet.microsoft.com/en-us/library/cc737478(v=ws.10).aspx)
- Using NSLOOKUP -> (https://support.microsoft.com/en-us/kb/200525)
- Traffic Shaping -> (https://en.wikipedia.org/wiki/Traffic_shaping)
- Blue Coat Traffic Shapers -> (https://www.bluecoat.com/products/packetshaper)
- Load Balancer -> (https://en.wikipedia.org/wiki/Load_balancing_(computing))
- F5 Networks Load Balancers -> (https://f5.com/glossary/load-balancer)
- Meaning of 'RTFM' -> (http://www.internetslang.com/RTFM-meaning-definition.asp)
- Rack Unit -> (https://en.wikipedia.org/wiki/Rack_unit)

## 1.2 - Compare and Contrast the Use of Networking Services and Applications

### Study Alerts for Exam
- Know your basic vocabulary (especially VPN protocols)
- Apply when web services or UC is appropriate

### Understanding VPN Services
- Purpose of VPN
  * Provides remote access to external employees
  * Cheaper to setup and maintain than a leased line
  * Advantages: 
    - Cost, scalability
  * Disadvantages:
    - User must initiate a VPN connection
    - Performance can be poor
- VPN Deployment Types
  * Site to site
    - Site to site VPNs are used to connect on premise network to a cloud service such as Microsoft Azure
  * Host to site
  * Host to host
- VPN Encapsulation
- VPN Protocols
  * PPP: Layer 2 protocol with a long history
  * PPTP: Older, Microsoft centric tunneling protocol (TCP 1723)
    - Uses generic routing encapsulation (GRE IP Protocol value 47) for tunnel and MPPE (microsoft point to point encryption) for encryption
  * L2TP: Combination of PPTP and L2TP (TCP 1701)
    - Uses Internet protocol security (IPSec) and IKE encryption
  * IPSec: Can be used with IKE to create VPN tunnels (UDP 500)
    - Can break NAT (network address translation) because in tunnel mode sue to IP header encryption
  * SSL VPN: VPN by using SSL/TLS (TCP 443)
- Radius Components
  * aka Remote and User Dial In User Service
  * AAA protocol (Authentication, Authorization, Accounting)
- AAA Differences
  * RADIUS
    - Vendor neutral
    - Uses UDP (best effort)
    - Encrypts only payload
    - Combines authentication and authroization 
    - Pros: Interoperability and performance
  * TACASS+
    - Cisco proprietary
    - TCP (ensured delivery)
    - Encrypts entire session
    - Isolates the "three A's"
    - Pros: Security and flexibility
    - Cisco's Identity Services (ISE) supports RADIUS but not TACACS+

### Web Serveices Basics
- Development methods to allow Web Applications to communicate with each other
- Uses standard protocols (Web ptorocols: HTTP, HTTPS, XML, SOAP)
- As a network administrator, you may need to manage firewall exceptions for Web Services (but you shouldn't have to)
- Example: LAMP Web application exchanging data with a Windows Server IIS/ASP.NET Web application

### Unified Communications Basics
- Suite of real time communications technologies
- IP telephony (IPT) and voice over IP (VOIP)
- Presence
- Instant Messaging
- Web conferencing/collaboration
- Voice mail, etc. from desktop or mobile device

## 1.2.Z - Appendix

### Useful Links
- Virtual Private Network -> (https://en.wikipedia.org/wiki/Virtual_private_network)
- VPNs and VPN Technologies -> (http://www.ciscopress.com/articles/article.asp?p=24833)
- Types of VPN Access -> (http://www.orbit-computer-solutions.com/Types-of-VPN-Access.php)
- Site-to-Site VPN -> (http://computer.howstuffworks.com/vpn4.htm)
- Remote Access VPN -> (http://computer.howstuffworks.com/vpn3.htm)
- Host Your Own Private VPN -> (http://www.instructables.com/id/Host-Your-Own-Virtual-Private-Network-VPN-with-O/)
- LogMeIn Hamachi VPN -> (https://secure.logmein.com/products/hamachi/)
- Configure Site-to-Site VPN with Microsoft Azure -> (https://msdn.microsoft.com/en-us/library/azure/dn133795.aspx)
- Encryption and Security Protocols in a VPN -> (http://computer.howstuffworks.com/vpn7.htm)
- Understanding VPN Tunneling -> (http://www.enterprisenetworkingplanet.com/netsp/article.php/3624566/Networking-101-Understanding-Tunneling.htm)
- VPN Tunneling Protocols -> (https://technet.microsoft.com/en-us/library/cc771298(v=ws.10).aspx)
- VPN Tunneling -> (http://compnetworking.about.com/od/vpn/a/vpn_tunneling.htm)
- Configure a Firewall for VPN Traffic -> (https://technet.microsoft.com/en-us/library/dd458955(v=ws.10).aspx)
- What Ports are Used in a VPN? -> (http://kb.juniper.net/InfoCenter/index?page=content&id=KB5671)
- NAT Compatibility Requirements -> (https://www.ietf.org/rfc/rfc3715.txt)
- How Does NAT-T Work with IPSec? -> (https://supportforums.cisco.com/document/64281/how-does-nat-t-work-ipsec)
- Why SSL VPN? -> (https://openvpn.net/index.php/open-source/339-why-ssl-vpn.html)
- Microsoft SSTP Protocol -> (https://technet.microsoft.com/en-us/magazine/2007.06.cableguy.aspx)
- RADIUS Protocol and Components (https://technet.microsoft.com/en-us/library/cc726017(v=ws.10).aspx)
- RADIUS vs. TACACS+ -> (http://www.networkworld.com/article/2838882/radius-versus-tacacs.html)
- TACACS+ and RADIUS Comparison -> (http://www.cisco.com/c/en/us/support/docs/security-vpn/remote-authentication-dial-user-service-radius/13838-10.html)
- IPv4 Address Blocks Reserved for Documentation -> (https://tools.ietf.org/html/rfc5737)
- Using the IPCONFIG Command -> (https://support.microsoft.com/en-us/kb/314850)
- Introduction to Web Services -> (http://www.w3schools.com/webservices/ws_intro.asp)
- Web Service -> (https://en.wikipedia.org/wiki/Web_service)
- What is DevOps? -> (http://blog.pluralsight.com/what-is-devops)
- What is Unified Communications? -> (http://voip.about.com/od/unifiedcommunications/a/UnifiedComm.htm)
- UC Architecture Basics -> (http://www.cisco.com/c/en/us/td/docs/voice_ip_comm/uc_system/UC6-0-1/system_description/SDIPC.html)
- Session Initiation Protocol (SIP) -> (https://en.wikipedia.org/wiki/Session_Initiation_Protocol)
- Microsoft Lync/Skype for Business -> (http://products.office.com/en-us/lync/lync-2013-video-conferencing-meeting-software)
- Cisco UC Products and Services -> (http://www.cisco.com/c/en/us/products/unified-communications/index.html)
- DirectAccess Always-on VPN -> (https://technet.microsoft.com/en-us/windows/directaccess.aspx)

## 1.3 Configuring Network Services and Applications

### Study Alerts for Exam
- Understand the Basic concepts of DNS, DHCP, NAT
- Recognize when to use relevant command line tools (ipconfig, ifconfig)

### DHCP
- aka Dynamic Host Configuration Protocol
  * RFC 1531
  * UDP port 67 (server); port 68 (client)
- Many devices need statically assigned IPv4 addresses
  * Servers, access points, printers, switches and routers
- Request for Commants (RFC) documents are published by the Internet Engineering Task Force (IETF)
- Method for automating client IPv4 Address assignment

### DNS
- aka Domain Name System
- Distributed database of hostname to IP address mappings
- Defined in RFC 1035
- UDP, TCP port 53
- Records (A, AAAA, MX, CNAME, PTR)
- Dynamic DNS
- DHCP Integration

### DNS Troubleshooting Skills
- Windows
  * ipconfig
  * nslookup
  * dig
- Linux
  * ifconfig
  * nslookup
  * dig

### Proxy, Address Translation, and Port Forwarding
- Forward and Reverse Proxies
  * Proxies provide security and possibly caching and/or content filtering
  
### IPV4 Address Exhaustion
- IPv4 address space is 32 bits = 4.2billion addresses
- IPv6  address gives us 128 bits, almost unlimited amount
- RFC 1883 codified IPv6 in 1996, will be a long time before tranisitioning permanently

### Network Address Translation (NAT)
- Nat: one to one, one to many
- Dynamic NAT: Sharing multiple public IPs
- PAT - Port mapping or port forwarding
- DNAT: Also called port forwarding; used to publish private IPs to public internet
- SNAT: Source, static, stateful, secure

## 1.3.Z - Appendix

### Useful Links
- Microsoft Visio 2013 Trial -> (http://www.microsoft.com/en-us/evalcenter/evaluate-visio-professional-2013)
- What is a SOHO Network? -> (http://www.dsl.com/faqs/what-is-a-soho-network/)
- RFC 1918 (Private IPv4 Addresses) -> (https://tools.ietf.org/html/rfc1918)
- RFC 3046 (DHCP Relay Agent) -> (https://tools.ietf.org/html/rfc3046)
- APIPA - Automatic Private IP Addressing -> (http://compnetworking.about.com/cs/protocolsdhcp/g/bldef_apipa.htm)
- Dynamic Host Configuration Protocol -> (https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol)
- DHCP Overview -> (https://technet.microsoft.com/en-us/library/cc731166.aspx)
- IPCONFIG -> (http://ss64.com/nt/ipconfig.html)
- IFCONFIG -> (http://linux.die.net/man/8/ifconfig)
- NSLOOKUP -> (https://support.microsoft.com/en-us/kb/200525)
- DIG -> (https://www.madboa.com/geek/dig/)
- Domain Name System -> (https://en.wikipedia.org/wiki/Domain_Name_System)
- Root Name Server -> (https://en.wikipedia.org/wiki/Root_name_server)
- RFC 2663: NAT -> (https://tools.ietf.org/html/rfc2663)
- Forward Proxy vs. Reverse Proxy -> (http://www.jscape.com/blog/bid/87783/Forward-Proxy-vs-Reverse-Proxy)
- Port Forwarding -> (https://en.wikipedia.org/wiki/Port_forwarding)
- IPv4 Address Exhaustion -> (https://en.wikipedia.org/wiki/IPv4_address_exhaustion)
- Did Bill Gates Really Say the 640K Quote? -> (http://www.computerworld.com/article/2534312/operating-systems/the--640k--quote-won-t-go-away----but-did-gates-really-say-it-.html)
- RFC 2460: IPv6 -> (https://tools.ietf.org/html/rfc2460)
- Network Address Translation -> (https://en.wikipedia.org/wiki/Network_address_translation)
- NAT and PAT: What's the Difference? -> (http://blog.boson.com/bid/53313/NAT-and-PAT-What-s-the-Difference)

## 1.4 Explain the Characteristics and Benefits of Various WAN Technologies

### WAN Basics
- What is LAN?
  * WANs connect networks that are wider range
    - Distance is relative
  * Own LANs and Lease WANs

### WAN Connection Types
  * Dedicated leased line
    - Reserved point to point link
  * Circuit switched connection
    - As needed link (phone call)
  * Packet switched connection
    - Pseudo dedicated virtual links
    
### Dedicated Leased Line Technologies
- Circuits use multiplexing technology to aggregate 64 Kbps channels
- Layer 2 protocols are PPP or Cisco HDLC (PPP is multiprotocol and multilink)
- T1: 24 DS0 channels = 1.544 Mbps (~$200/mo)
- E1: 32 DS0 channels = 2.048 Mbps
- T3: 28 T1s = 44.7 Mbps (~$5-10K/mo)
- E3: 34 Mbps

### SONET and OC Levels
- Synchronous Optical Network (SONET): Layer 1 technology that uses fiber optic cabling
  * Can transmit some Layer 2 encapsulations like Asynchronous Transfer Mode (ATM)
  * ATM required special hardware which costs significantly more
- Uses TDM to support multiple data flows over single fiber
- OC3: Equivalent to 100 TAz @ 155 Mbps (~$20-45K/mo)
- OC12: Equivalent to 4 OC3s @ 622 Mbps
- DWDM (Dense Wavelength Division Multiplexing): Each light Wavelength carries a data stream independantly; more expensive than CWDN
- CWDM (Course Wavelength Divsion Multiplexing); Spectrum broken less granularly than DWDN

### Circuit Switched WAN Technologies
- Circuit Switched Connections
  * Analog Modem
  * ISDN
  * Digital Subscriber Line
  * Broadband Cable
- Analog Modem and ISDN
  * Analog to digital modulation
  * Voice or Data @ 53 Kbps
- Integrated Services Digital Network
  * Voice or data over PTSN
  * B: 64 Kbps x 2 (128 Kbps total)
  * D: 16 Kbps control panel
  * Requires modem and ISDN telephones
- Digital Subscriber Line
  * Digital voice and data over PSTN
  * ASDL is more common
  * Uses PPPoE and IP
- Broadband Cable
  * Data over cable tv coax cabling
  * Generally asymmetric transfers
  * Uses DOCSIS (data over cable service interface specification)
  
### Packet Switched WAN Technologies
- Frame Relay
  * Was the standard for business WANs
  * Operates at OSI Layer 2
  * Permanent or switched virtual circuits (PVCs, SVCs)
  * DTE (Data Terminal Equip): Modem or CSU/DSU on customer's side - terminates the connection
  * DCE (Data COmmunications Equip): On Providers side
- MPLS
  * Microprotocol Label Switching
  * The current WAN standard
  * Single backbone can route Frame, ATM, Metro Ethernet, etc
  * Header functions as OSI Layer 2.5
  * MPLS uses special headers called "labels" to make routing decisions
- Metro Ethernet
  * Used in metropolitan area network (MAN ) environments
  * Can do pure Ethernet, Ethernet over SONET, Ethernet over MPLS

### Wireless WAN Technologies
- Satellite
  * Appropriate for locations that are far way
  * Need satellite dish and line of sight
  * Latency because satellites travel 22K miles high
  * Sensitivity to weather
  * Pay for the data transfer (like smartphones)
- WiMAX
  * Worldwide Interoperability for Microwave Access
  * Up to 45 Mbps downstream / 50km
  * Certain companies are moving away from WiMAX
- Cellular Networks
  * Targeted at smartphones and tablet devices
  * GSM (Global System for Mobile Communications)
  * CDMA (Code Division Multiple Access)
  * 2G: Edge: 135 Kbps downstream
  * 3G: High Speed Packet Access (HSPA+) ~4 Mbps downstream
  * 4G Long Term Evolution (LTE) 50Mbps
  
## 1.4.Z Appendix

### Useful Links
- Difference Between LAN, MAN, and WAN (https://kb.iu.edu/d/agki)
- Verizon Managed WAN Service Level Agreement (SLA) (http://www.verizonenterprise.com/external/service_guide/reg/cp_mwan_sla.pdf)
- Leased Line (https://en.wikipedia.org/wiki/Leased_line)
- Understanding Dedicated Leased Lines vs. Shared Access (http://www.chaffeecountyedc.com/EndUserFiles/33266.pdf)
- Packet vs Circuit Switching (http://bpastudio.csudh.edu/fac/lpress/471/hout/netech/circuitvpacket.htm)
- T-Carrier (https://en.wikipedia.org/wiki/T-carrier)
- E-Carrier (https://en.wikipedia.org/wiki/E-carrier)
- Time-Division Multiplexing (TDM) (https://en.wikipedia.org/wiki/Time-division_multiplexing)
- Point-to-Point Protocol (PPP) (https://en.wikipedia.org/wiki/Point-to-Point_Protocol)
- Use Multilink PPP (http://www.techrepublic.com/blog/data-center/use-multilink-ppp-to-combine-multiple-circuits-into-a-single-circuit-with-a-single-router-interface/)
- Cisco HDLC (https://en.wikipedia.org/wiki/Cisco_HDLC)
- CSU/DSU (https://en.wikipedia.org/wiki/CSU/DSU)
- T1/E1 CSU/DSUs (http://www.adtran.com/web/page/portal/Adtran/group/127)
- Demarcation Point (https://en.wikipedia.org/wiki/Demarcation_point)
- Asynchronous Transfer Mode (ATM) (https://en.wikipedia.org/wiki/Asynchronous_Transfer_Mode)
- A Brief Overview of ATM (http://ccr.sigcomm.org/archive/1995/apr95/ccr-9504-siu.pdf)
- Synchronous Optical Networking (SONET) (https://en.wikipedia.org/wiki/Synchronous_optical_networking)
- Optical Carrier Transmission Rates (https://en.wikipedia.org/wiki/Optical_Carrier_transmission_rates)
- SONET/OC Topology and Cost (https://www.10gea.org/network/sonet-ocx/)
- Wavelength-Division Multiplexing (https://en.wikipedia.org/wiki/Wavelength-division_multiplexing)
- What is Difference Between DWDM and CWDM? (http://www.wisegeek.com/what-is-the-difference-between-dwdm-and-cwdm-optical-technolgies.htm)
- Integrated Services Digital Network (ISDN) (https://en.wikipedia.org/wiki/Integrated_Services_Digital_Network)
- What is ISDN? (http://public.swbell.net/ISDN/overview.html)
- Modem (https://en.wikipedia.org/wiki/Modem)
- Hayes (AT) Command Set (https://en.wikipedia.org/wiki/Hayes_command_set)
- ADSL (https://en.wikipedia.org/wiki/Asymmetric_digital_subscriber_line)
- ADSL Packages (http://www.mweb.co.za/internet-connection/adsl/adsl-packages.aspx)
- Cable Internet Access (https://en.wikipedia.org/wiki/Cable_Internet_access)
- List of Broadband Cable Providers (http://broadbandnow.com/Cable-Providers)
- PPPoE (https://en.wikipedia.org/wiki/Point-to-point_protocol_over_Ethernet)
- DOCSIS Specification (http://docsis.org/)
- Frame Relay (https://en.wikipedia.org/wiki/Frame_Relay)
- Frame Relay Details (http://www.protocols.com/pbook/frame.htm)
- MPLS (https://en.wikipedia.org/wiki/Multiprotocol_Label_Switching)
- MPLS for Dummies (https://www.nanog.org/meetings/nanog49/presentations/Sunday/mpls-nanog49.pdf)
- Metro Ethernet (https://en.wikipedia.org/wiki/Metro_Ethernet)
- Metro Ethernet Forum (MEF) (http://www.metroethernetforum.org/)
- DTE vs. DCE (http://ftp1.digi.com/support/cabling/dte_vs_dce.pdf)
- Satellite Internet Access (https://en.wikipedia.org/wiki/Satellite_Internet_access)
- Hughes Satellite Service (http://www.hughesnet.com/)
- WiMAX (https://en.wikipedia.org/wiki/WiMAX)
- WiMAX Forum (http://www.wimaxforum.org/)
- GSM vs. CDMA: What is the Difference? (http://www.makeuseof.com/tag/gsm-vs-cdma-difference-better/)
- Giz Explains: How Cell Towers Work (http://gizmodo.com/5177322/giz-explains-how-cell-towers-work)
- Ookla Speedtest Mini API (https://www.speedtest.net/mini.php)

## 1.5 Installing and Properly Terminating Various Cable Types and Conenctors using Apropriate Tools

### Study Alerts for Exam
- Recognize Cable and connector form factors
- Associate different cables/connectors with different goals

### Overview
  * Copper cables and connectors
  * Fiber cables and connectors
  * Media converters
  * termination
  * Network Technician Tools
  
### Twisted-Pair Copper Cables
  * Copper conductor
  * Twisting reduces electronic inteference (Cross talk and EMI)
  * Foil shielding: further reduce crosstalk
  * Pinout: Defines meaning of each wire
  
### Twisted Pair Cable Standards
  * Max cable length = 100 M (328 ft); 10 Gbps Ethernet is less
  * Unshielded Twisted Pair (UTP) - Susceptible to EMI
  * Shielded Twisted Pair - Protects against EMI 
  * Twisted Pair Categories
    - CAT 3 = 10 Mbps - Legacy Category
    - CAT 5 = 100 Mbps
    - CAT 5e = 1 Gbps
    - CAT 6/6a = 10 Gbps
    
### Twisted-Pair Wiring Standards
  * 568A and 568B is part of the Electronic Industries Alliance (EIA)/Telecommunications Industry Association (TIA)
  * Network Infrastructure would be compatible with any type provided they follow the standards
  * Cable Types
    - Straight Through Cable - 568B on each side or 568A on each side
    - Crossover Cable - 568A and 568B on each side and not necessaryily used today as switches and routers incorporate the crossover
    - Rollover Cable - 568A and reversal of 568A ion other side

### Coaxial Copper Cables
  * Made up of 4 Layers
    - Outer insulator
    - Shielding wire mesh
    - Inner Insulator
    - Copper core
  * Types of Copper Cables
    - Radio Guide RG-58 (Thinnet)
      * 10 Mbps
      * 185 meters
      * Uses a BNC connector
      * Has been replaced by twisted pair
    - RG-59 and RG-6
      * Typically Used for cable television and cable internet service

### Plenum-grade Cable
  * Traditional cables coated with polyvinyl chloride (PVC) give off toxic fumes when burning
  * PVC vs. Plenum
    - The plenum is an enclosed space used for airflow
    - Usually thought of as the space above a drop ceiling or below a raised floor
    - Plenum grade cable should always be used in a plenum space
    - Plenum-grade cable has a fire-retardent plastic jacket consisting of low-smoke PVC

### Ethernet Standards
  * 100BaseTX
    - 100: Line speed
    - Base: Baseband transmission
    - TX: Cable standard (twisted-pair or fiber)

### Common Connectors
  * Registered Jack RJ-11 (3 pairs)
  * RJ-45/RJ-48 (4 pairs)
  * UTP Coupler (extended patch cables)
  * BNC (British Naval Connector; Bayonet Neill-Concelman)
  * BNC Coupler (Extends cable length)
  * F-Connector
 
### Serial Connector
  * DB-9/RS-232
  * DB-25
  
### Fiber Cables
  * Transmits light instead of electricity
  * Pros: Security, speed, distance
  * Cons: Expensive, termination, flexibility
  * Single mode: One light path; longer distance
  * Multimode: Many light propagation paths; shorter
  * UPC (Ultra Physical Contact): 1G Green + Blue; flat endface
  * APC (Angled Physical Contact): 2G Green, endface polished at 8 degree angle to eliminate airgap at termination point
  
### Fiber Connectors
  * SC - aka subscriber connector, standard connector, squared connector
  * ST aka straight tip
  * LC aka lucid connector
  * MTRJ Media termination recommended jack
  * FC Fiber connector
  * Fiber coupler
  
      
      
      
  
  
  
  
  
