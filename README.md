# CASE STUDY ON “SCADA/ICS Security Testing”

## 1. INTRODUCTION

## 1.1. WHAT IS SCADA CONTROL SYSTEM

SCADA, or Supervisory Control and Data Acquisition, is a control system architecture
utilized across various industries to remotely manage and monitor critical processes and
infrastructure. It consists of several key components:
- **Supervisory Control:** Software applications enable operators to remotely monitor
processes, view real-time data, and issue commands.
- **Remote Terminal Units (RTUs) or Programmable Logic Controllers (PLCs):**
These hardware devices interface with sensors and actuators in the field, collecting
data and executing control commands.
- **Communication Infrastructure:** SCADA systems rely on various protocols to
transmit data between the control center and remote field devices.
- **Human-Machine Interface (HMI):** Operators interact with the SCADA system
through computer screens or panels displaying real-time data and control options.
- **Data Acquisition:** SCADA systems continuously collect data from sensors measuring
parameters like temperature, pressure, and flow rate.
- **Control Logic:** Predefined algorithms regulate processes based on operator-
configured setpoints, alarms, and control strategies.

Benefits of SCADA systems include remote monitoring and control, real-time data analysis,
increased reliability and safety, and scalability. However, they also pose security challenges,
as they are susceptible to cyber threats such as unauthorized access and malware attacks.

Securing SCADA systems against these threats is crucial to safeguard critical infrastructure
and ensure uninterrupted operations.


## 1.2. SCADA SYSTEM CONCEPT

- SCADA WorkStation : Human operator it's a device to issue a command central
SCADA console, receiving raw data in human form, also monitor and control
- HMI (Human-Machine Interface): It’s Software & Hardware that allows human
operator to monitor state of process under control, modify control settings, manually
override auto-control operations The interface locate between the human operator and
the commands relevant to the SCADA system.
- Data Historian: Collect and store information from your mission critical systems,
extract and perform accurate analyses (SQL).
- SCADA Server MTU: Master terminal unit is a device that issues the commands to
the Remote Terminal Unit (RTUs) which are located at remote places from the
control, gathers the required data, stores the information, and process the information
and display the information.
- RTU: Connecting to sensors on the process, converting sensors signals and sending
digital data to the supervisory systems
- PLC: Programmable Logic Controller automatically performers the main site
control process which controls the operation of industrial equipment's. such as control
of machinery.

## 2. SCOPE AND OBJECTIVE

Securing SCADA (Supervisory Control and Data Acquisition) systems is paramount in
today's interconnected world, where critical infrastructure is increasingly reliant on these
control systems. Let's delve deeper into why security is crucial for SCADA systems:

1. **Vulnerability to Cyber Attacks** : SCADA systems are often connected to corporate
    networks or the internet for remote monitoring and control. This connectivity exposes
    them to a wide array of cyber threats, including ransomware, phishing attacks, and
    sophisticated malware. Attackers may exploit vulnerabilities in SCADA software or
    hardware to gain unauthorized access, manipulate data, or disrupt operations.
2. **Potential for Economic Loss** : The economic impact of a SCADA security breach can
    be significant. Disruptions in power generation, water treatment, or transportation
    systems can lead to financial losses for both public utilities and private companies.
    Moreover, the costs associated with recovering from an attack, including system
    repairs, regulatory fines, and reputational damage, can be substantial.
3. **Supply Chain Risks** : SCADA systems often rely on components and software from
    various vendors. However, vulnerabilities in third-party products can pose significant
    risks to system security. Supply chain attacks, where attackers compromise a trusted
    supplier to infiltrate SCADA networks, are a growing concern. Implementing robust
    supply chain security measures is essential to mitigate these risks.
4. **Complexity of Infrastructure** : Modern SCADA systems are highly complex,
    comprising interconnected components such as sensors, controllers, and
    communication networks. Managing the security of such complex infrastructures
    requires comprehensive risk assessment, regular vulnerability scanning, and proactive
    security measures such as network segmentation and access control.
5. **Emerging Threat Landscape** : The threat landscape facing SCADA systems is
    constantly evolving. New attack vectors, vulnerabilities, and exploitation techniques
    emerge regularly, challenging security professionals to stay ahead of the curve. Threat
    intelligence sharing, collaboration with cybersecurity experts, and participation in industry-specific information sharing and analysis centers (ISACs) are essential for staying informed and adapting defensive strategies accordingly.
6. **Human Factors** : People remain one of the weakest links in SCADA security. Insider
    threats, whether intentional or unintentional, can pose significant risks to system
    integrity and confidentiality. Employees with access to SCADA systems must receive
    regular security training to recognize and respond to potential threats effectively.
7. **Continual Improvement** : Achieving and maintaining SCADA security is not a one-
    time endeavor but rather an ongoing process. Regular security assessments, audits,
    and updates are necessary to address emerging threats, comply with evolving
    regulations, and adapt to changes in the operational environment.

In conclusion, the security of SCADA systems is critical for safeguarding critical
infrastructure, protecting public safety, ensuring data integrity and confidentiality, and
complying with regulatory requirements. Addressing the multifaceted challenges of SCADA
security requires a holistic approach that integrates technological solutions, robust policies
and procedures, ongoing vigilance against emerging threats, and collaboration among
stakeholders across various sectors. Proactive measures such as threat intelligence sharing,
employee training, and supply chain risk management are essential components of a
comprehensive SCADA security strategy. By prioritizing security and investing in proactive
measures, organizations can mitigate risks, enhance resilience, and ensure the reliable and
secure operation of SCADA systems in an increasingly interconnected world.


## 2.1. REAL ATTACKS

Security risks have been reported in control systems for the last few years.


## 2.2. ATTACK VECTORS

SCADA (Supervisory Control and Data Acquisition) and ICS (Industrial Control Systems)
are critical components of modern infrastructure, managing industrial processes ranging from
manufacturing to energy distribution. Given their importance, they're prime targets for
cyberattacks. Here are some common attack vectors:

1. **Network Intrusion** : Hackers exploit vulnerabilities in network infrastructure to gain
    unauthorized access to SCADA/ICS systems. This can include exploiting weak
    passwords, unpatched software, or using malware to infect connected devices.
2. **Phishing Attacks** : Social engineering techniques are used to trick employees into
    revealing sensitive information or installing malware. Phishing emails targeting
    personnel with access to SCADA/ICS systems can lead to unauthorized access or
    system compromise.
3. **Malware** : Specifically crafted malware, such as ransomware or trojans, can infect
    SCADA/ICS systems, disrupting operations or allowing attackers to gain control.
    Stuxnet is a famous example of malware designed to target SCADA systems.
4. **Supply Chain Attacks** : Attackers compromise third-party suppliers or contractors
    involved in SCADA/ICS infrastructure, using them as entry points to infiltrate the
    main systems.
5. **Insider Threats** : Malicious insiders with authorized access can exploit their
    privileges to cause damage or leak sensitive information. This can be intentional or
    unintentional, such as through negligence.
6. **Physical Attacks** : Physical access to SCADA/ICS infrastructure can enable attackers
    to directly manipulate or sabotage systems. This includes tampering with hardware
    components or connecting unauthorized devices to the network.
7. **Denial of Service (DoS) Attacks** : Overwhelming SCADA/ICS systems with
    excessive traffic can disrupt operations or cause them to fail, leading to potentially
    severe consequences.
8. **Zero-Day Exploits** : Attackers may leverage previously unknown vulnerabilities
    (zero-days) in SCADA/ICS software or protocols to gain unauthorized access or
    disrupt operations before patches or defenses are available.

Protecting SCADA/ICS systems requires a multi-layered approach involving robust
cybersecurity policies, regular security audits, employee training, and the implementation of
technical safeguards such as firewalls, intrusion detection systems, and encryption.


## 3. PENTESTING TOOLS

### 3.1. T-Pot

T-Poy is an ICS honeypot with the goal to collect intelligence about the motives and methods
of adversaries targeting industrial control systems.

T-Pot is based on Ubuntu Server 14.04.4 LTS. The honeypot daemons as well as other
support components being used have been paravirtualized using docker. This allowed us to
run multiple honeypot daemons on the same network interface without problems make the
entire system very low maintenance. The encapsulation of the honeypot daemons in docker
provides a good isolation of the runtime environments and easy update mechanisms.

**Installation:**

1. Clone the repository.
    git clone https://github.com/dtag-dev-sec/tpotce.git
    cd tpotce
2. Invoke the script that builds the ISO image.
    sudo ./makeiso.sh


### 3.2. firmwalker

A simple bash script for searching the extracted or mounted firmware file system.
It will search through the extracted or mounted firmware file system for things of interest
such as:

- etc/shadow and etc/passwd
- list out the etc/ssl directory
- search for SSL related files such as .pem, .crt, etc.
- search for configuration files
- look for script files
- search for other .bin files

**Installation:**

- If you wish to use the static code analysis portion of the script, please install eslint:
    npm i -g eslint && ./firmwalker {path to root file system}
    {path for firmwalker.txt}
- Example: ./firmwalker linksys/fmk/rootfs ../firmwalker.txt
- A file firmwalker.txt will be created in the same directory as the script file unless you
    specify a different filename as the second argument
- Do not put the firmwalker.sh file inside the directory to be searched, this will
    cause the script to search itself and the file it is creating
- chmod 0700 firmwalker.sh


### 3.3. MODBUS Penetration Testing Framework

MODBUS Penetration Testing Framework is a modular framework with every kind of
diagnostic and offensive feature you could need in order to pentest modbus protocol. It is a
full Modbus protocol implementation using Python and Scapy.

The Modbus/TCP protocol was used as the reference protocol to display the effectiveness of
the test bed in carrying out cyber attacks on a power system protocol. Modbus/TCP was
chosen specifically for these reasons:

- modbus is still widely used in power systems.
- modbus/TCP is simple and easy to implement.
- modbus protocol libraries are freely available for utilities to implement smart grid
    applications.

**Installation:**

1. Clone the repository
    git clone https://github.com/0x0mar/smod.git
2. Run the script
    python3 smod.py


### 3.4. Binwalk

Binwalk is a fast, easy to use tool for analyzing, reverse engineering, and extracting firmware
images.

**Installation:**

1. Installation follows the typical Python installation procedure:
    sudo python3 setup.py install
2. Dependencies
    sudo pip install nose coverage pycryptodome capstone


## 4. STEPS OF ETHICAL HACKING

Penetration testing, often abbreviated as pentesting, is a crucial process for assessing the
security posture of SCADA (Supervisory Control and Data Acquisition) and ICS (Industrial
Control Systems) environments. However, conducting penetration testing on SCADA/ICS
systems requires specialized methodologies due to their critical nature and potential impact
on infrastructure and safety. Here are some methodologies commonly employed for
SCADA/ICS penetration testing:

1. **Pre-Engagement Phase** :
     Define Scope: Clearly outline the objectives, scope, and limitations of the
       penetration test, including which systems, networks, and assets will be tested.
     Obtain Permissions: Obtain necessary permissions from relevant stakeholders
       and ensure that all legal and regulatory requirements are met.
2. **Information Gathering** :
     Reconnaissance: Gather information about the target SCADA/ICS
       environment, including network architecture, protocols used, software
       versions, and potential vulnerabilities.
     Asset Identification: Identify critical assets, such as controllers, HMIs
       (Human-Machine Interfaces), RTUs (Remote Terminal Units), and
       communication networks.
3. **Threat Modeling** :
     Analyze Potential Threats: Evaluate potential threats and attack vectors that
       could be used against the SCADA/ICS environment, considering both internal
       and external threats.
     Assess Impact: Determine the potential impact of successful attacks on the
       availability, integrity, and confidentiality of SCADA/ICS systems.
4. **Vulnerability Assessment** :
     Vulnerability Scanning: Utilize automated tools to scan SCADA/ICS systems
       for known vulnerabilities in software, protocols, and configurations.


```
 Manual Analysis: Perform manual analysis to identify vulnerabilities that may
not be detected by automated scanners, such as logic flaws or
misconfigurations.
```
5. **Exploitation** :
     Exploit Development: Develop or utilize exploits targeting identified
       vulnerabilities to gain unauthorized access to SCADA/ICS systems.
     Post-Exploitation: Once access is gained, escalate privileges and explore the
       environment to determine the extent of compromise and potential impact.
6. **Reporting and Remediation** :
     Documentation: Document findings, including identified vulnerabilities,
       exploited weaknesses, and recommendations for remediation.
     Prioritize Risks: Prioritize vulnerabilities based on their severity,
       exploitability, and potential impact on SCADA/ICS operations.
     Remediation Guidance: Provide guidance and recommendations for mitigating
       identified vulnerabilities and improving overall security posture.
7. **Post-Testing Activities** :
     Debriefing: Conduct a debriefing session with relevant stakeholders to discuss
       findings, lessons learned, and recommendations for improving security.
     Continuous Monitoring: Implement continuous monitoring mechanisms to
       detect and respond to future security threats in the SCADA/ICS environment.

It's essential to conduct SCADA/ICS penetration testing by experienced professionals with
specialized knowledge in industrial control systems, as these environments have unique
characteristics and requirements compared to traditional IT systems. Additionally, testing
should be performed with caution to avoid disruptions to critical operations and ensure the
safety and reliability of industrial processes.


## 5. CONCLUSION

Implementing a comprehensive network security strategy involves several essential
components. Creating Demilitarized Zones (DMZs) tailored for specific functionalities and
access levels within the network infrastructure, such as peer connections, data historian
storage, and hosting the Inter Control Center Communications Protocol (ICCP) server in
SCADA systems, is crucial. Alongside DMZs, properly configured firewalls act as barriers,
safeguarding sensitive information like passwords, IP addresses, and files from unauthorized
access and cyber threats. Proxy servers further enhance security by filtering and monitoring
traffic between internal networks and the internet. However, deploying these technologies
alone is insufficient without a robust security policy framework. Effective security policies
outline guidelines and procedures for maintaining data integrity and confidentiality,
establishing access controls, and responding to security incidents promptly. Moreover,
regular security training for staff is essential in fortifying the human element of cybersecurity,
educating employees on identifying and mitigating security risks, including physical and
social engineering attacks. In summary, a multi-layered approach incorporating DMZs,
firewalls, proxy servers, stringent security policies, and ongoing staff training is imperative in
safeguarding critical infrastructure against evolving cyber threats.


## 6. REFERENCES

```
 Weiss, J. A. (2006). "Protecting Industrial Control Systems from Electronic Threats."
ISA - The Instrumentation, Systems, and Automation Society.
 Sauter, T., & Stuxnet, R. (2014). "The true story of the Stuxnet virus." IEEE
Spectrum, 51(3), 48-53.
 Langner, R. (2013). "To Kill a Centrifuge: A Technical Analysis of What Stuxnet's
Creators Tried to Achieve." IEEE Security & Privacy, 11(3), 14-21.
 Bejtlich, R. (2015). "The Practice of Network Security Monitoring: Understanding
Incident Detection and Response." No Starch Press.
 kh4sh3i/ICS Pentesting Tools - https://github.com/kh4sh3i/ICS-Pentesting-Tools
```

