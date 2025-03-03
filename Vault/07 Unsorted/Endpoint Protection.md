# Endpoint Protection

From Embedded Lab Vienna for IoT & Security

## Summary

This article describes the importance of endpoint protection and the types of threats an endpoint can be a victim of. It also gives insights into data leakage, the concept of sandboxing and offers possible solutions for protecting an endpoint.

## Types of Threats

The CNNIC “Statistical Report on Internet Development in China” defined 20 types of internet usages, then classified internet users into 7 groups based on their habits, time and activities done while surfing on the web or using some applications connected to the internet. Some of these categories are Gamer, Network Businessman or Socializer. People in all of these groups may encounter various threats attempting to harm their systems or steal valuable information from them. Such threats can be fraud, attacks by virus, system overhead, false positive or prevalent malware. In general, threats can be divided into two main types:

- Internal threats
- External threats

Endpoint Protection Suites primarily focus on external threats. The most common attacks by external threats include:

- Phishing
- Unpatched vulnerabilities
- Malvertising
- Drive-by-downloads
- Data loss and theft
- Session Hijacking

Internal threats, on the other hand, often require other approaches such as "awareness training" of the Employees - internal threats include:

- Sabotage
- Espionage
- Unauthorized disclosure of information
- Corruption
- Intended or unintended loss of data and information
- Abuse of the assigned right

In order to shed some light on some of the most important external threats and words (key-terms) that are important in connection with Endpoint Protection, the next section will now go into a little more detail here:

### Data Leakage

Trusting third-party companies (agents) with handling confidential data has several advantages: partner companies may gain access to customer data, which can be done by using the same service as the distributor (data owner). This way, not only reading but also updating and altering data in any way can be more efficient, but it can also lead to worse data quality due to perturbation. One of the main goals of the agents is to keep the data quality as high as possible while also preventing data leakage via endpoints. This means the protection of computer networks that are remotely bridged to client devices, such as mobile phones, laptops, or tablets. Many companies are trying to ensure endpoint security by using a single, multi-purpose software solution that enables administrators to set up a centrally managed security system. However, there are also several specialized products on the market. 53% of the companies that participated in the 2018 Insider Threat report have been victims of insider attacks more than once a year, which highly emphasizes the importance of using proper cyber security systems.

### Malware

Malware (malicious software) is by far the most dangerous type of threat and even though EPPs using the most updated signature databases used to detect such programs, they have widely spread across systems in the globe. The best way to eliminate malware in time is to use behavior-based detection, which is why EDR systems are most suited for this task.

### Virus

A virus has the capability to spread from host to host and is designed to replicate itself. It is a type of malicious code or program written to alter the way a computer operates. A virus attaches itself to a legitimate program in order to execute its code and in the process, it has the potential to cause unexpected or damaging effects. This can be anything from harming the system software by corrupting data to fully destroying it.

### Phishing

Phishing is a security attack used to get control of a user’s passwords, credit card information, or other account credentials through websites or emails. Phishing websites mimic authentic ones in appearance, making it challenging for the average person to tell them apart

### Drive-by-downloads

Drive-by-download attacks are a common method of spreading malware, exploit insecure websites in order to inject malware code into the user’s endpoint device by initialize an automatically download the user do not want or notes. Malware may manifest as spyware, keyloggers, or trojan viruses.

### Session Hijacking

In a session hijacking attack, the hacker switches out the client or server’s session token for their own, gaining access to the user’s web browsing session. As a result, the hacker is able to steal any data they can access, such as cookie information, login credentials, or any other data accessed while the session is compromised, while the server continues to believe it is still in communication with a client during the attack.

### False Positive

This happens, when an antivirus program or any other security system identifies a legitimate code as illegitimate by mistake.

## Endpoint Protection Systems

Endpoint protection systems have been developed to provide sufficient protection against such external threats. These systems are divided into the following groups:

- Endpoint Protection Platform (EPP)
- Endpoint Detection and Response (EDR)
- Extended Detection and Response (XDR)
- Next-Generation Endpoint Security (NGES)

These systems are used in combination and delivered by various software vendors as ready-to-use software products (e.g., FireEye, Symantec, ...).

### Endpoint Protection Platform

One of the best solutions to achieve endpoint protection is to use an Endpoint Protection Platform (EPP), which consists of several tools, that can protect our systems from unwanted intrusion, such as firewalls, antivirus systems and data encryption. Such an Endpoint Protection Platform has several main characteristics:

- It is deployed on endpoint devices
- It focuses on preventing file-based attacks
- It can detect malicious activity
- It can provide investigation & Remediation capabilities

Endpoint protection platforms are software using signatures to ensure negative endpoint protection. They also have access to an own database, which stores signatures of collected threats and use it to match them with other signatures, which helps them detecting possible threats. A signature of a virus can be compared to a human fingerprint, is it a set of unique data or bits of code that makes it possible to identify it. An EPP also uses different services to monitor processes running in networks for the sake of malfunction, virus detection. Even though most attacks can be stopped by monitoring and signature matching, some viruses are still able to get in the system and that’s where the so-called Host-based Intrusion Prevention System (HIPS) takes action. It does not only wipe out malicious activities, but is also capable of deep behavioral inspection. The annihilation of threats, that already got into the system needs to be done as fast as possible, since the virus can spread really fast and take over the whole system.

According to a 2019 study the average protection rate of an Endpoint Protection Platform is 99.3% with an average false positive rate of 17 in 3000, which equals to 0.0057%.

#### Advantages of Endpoint Protection Platforms

- It provides a single, central endpoint security management solution
- It simplifies security management
- It protects and endpoint against most well-known threats

#### Disadvantages of Endpoint Protection Platforms

- It cannot deal with the complete network
- It reduces efficiency & productivity because it needs a lot of resources
- It cannot protect against insider threats

[[file:///index.php?title=File:Gartner2021.png|[file:///images/f/f2/Gartner2021.png|![Gartner2021.png]]

### Endpoint Detection and Response

EDR is a new generation of EPP, which combines endpoint management solutions and endpoint antivirus systems to wipe out malicious activities. EDR are complex systems also designed to monitor the state of multiple devices at the same time in bigger security infrastructures. Since this technology uses a moderner approach to endpoint detection, machine learning also plays some part in the functionality of EDR systems using calculations and well-tested algorithms to catch several kinds of suspicious activities from ruining the infrastructure without the need for manually created signatures. When relying on this method, attacks can be detected not by analyzing the file system, but by interpreting and monitoring the system, focusing on its malicious activities providing stable, real-time capture and alerting solutions.

#### Advantages of EDR

- It provides greater visibility of the network and the state of each individual endpoint
- It is able to scan entire networks
- It can detect unusual activity and respoind by isolating a possibly compromised endpoint

#### Disadvantages of EDR

- It produces a high volume of false alarms
- It creates mountains of backlogs and each alarm has to be assessed individually to identify the threat level
- Log retention is a burden to the system and its operators so often logs get deleted before they are assessed

Some examples of EDR technology are FireEye Endpoint Security and Symantec Endpoint Protection.

### Extended Detection and Response

XDR is a cloud-provided technology that includes multipoint solutions and advanced analytics to correlate alerts from multiple sources with incidents that originate from weaker individual signals to create more accurate detections. It aims to, reduce product sprawl, alert fatigue, integration challenges, and operational expenses, and will and will particularly appeal to security operations teams that have difficulty managing a portfolio of cutting-edge solutions. While EDR detects at the endpoint level, XDR goes beyond that. It can, detect anomalous and potentially malicious activity on devices such as servers, clouds, networks, etc. collect and detect

### Next-Generation Endpoint Security

This is one of the latest cybersecurity technologies that combines advanced artificial intelligence (AI), machine learning, and tighter integration of network and device security. These are used in next-generation endpoint security to provide more comprehensive and more adaptive protection than traditional endpoint security systems. To examine executable files, next-generation endpoint security combines the Real-time analysis of user and system activity. This enables users to quickly Identify key advanced technologies before and during execution and detect zero-day threats. Next-generation solutions not only address Threats, but also learn proactively! They continuously adapt their strategies to faster and more effective.

## Services and Tools

### FireEye

FireEye is a US cyber security company based in California, which offer solutions for cloud, network, email, or endpoint systems. Their Endpoint Protection Platform uses a signature-based engine and also has the capability to use EDR through a behavior-based analytics engine. It is able to find threats, for which signatures do not exist yet using MalwareGuard, which is based on machine learning algorithms, that help fulfilling this task. FireEye has various different features, that can be downloaded as modules on the FireEye Market. Some features include:

- Investigating known and unknown threats on tens of thousands of endpoints in minutes
- Identifying vectors an attack used to infiltrate an endpoint
- Determining whether an attack occurred (and persists) on a specific endpoint and where it spread
- Establishing timeline and duration of endpoint compromises and follow the incident
- Clearly identifying which endpoints and systems need containment to prevent

further compromise

It also comes with a malware guard, a machine learning engine to protect against more complex threats, as well as an exploit guard, a behavior analysis engine, which protects against software exploits.

### Symantec Endpoint Security

Symantec Endpoint Security provides security at the endpoint for both traditional and mobile devices across the three attack phases—Pre-Attack, Attack, and Post Attack. Some of its features include Attack Surface Reduction, Attack and Breach Prevention, and Post Breach Response and Remediation. Attack Surface Reduction is based on advanced policy controls and technologies, that continuously scan for vulnerabilities and misconfigurations on the endpoint. Its Attack Prevention System uses Machine Learning and Artificial Intelligence on devices and in the cloud to detect schemes to identify evolving threats across device types. Breach prevention is used to detect suspicious activity as early as possible at the endpoint—before they have any opportunity to persist on the network.

### ESET

ESET Endpoint Security is a network monitoring solution that detect advanced persistent threats, block targeted attacks, prevent data breaches, and provide protection against ransomware. Key features of ESET Endpoint Security include web threat management, signature matching, activity logging, whitelisting/blacklisting capabilities, application security, vulnerability scanning, email attachment protection and event tracking. Using predefined rules, the host-based intrusion prevention solution tracks system activity and detects suspicious behavior in the system. In addition, the exploit blocker module helps scan multiple vulnerable applications, including email clients, document readers, Java and more to block threats when triggered. ESET Endpoint Security can be deployed on-premises or hosted in the cloud.

### OSSEC

OSSEC (Host-based Intrusion Detection System) is a versatile, open-source software that operates on individual hosts. It employs sophisticated techniques for event monitoring, including:

- Tracking changes in Windows registry
- Enforcing central security policies
- Analyzing logs for suspicious activity
- Identifying rootkits
- Verifying file integrity
- Issuing real-time alerts
- Activating automatic responses

OSSEC is compatible with numerous operating systems, including FreeBSD, Open BSD Linux, Mac OS, Windows, and Solaris. It is made up of multiple components: a central manager that monitors data from databases, agents, system logs, and non-agent devices, the manager collects events from logs and devices connected remotely. In case of suspicious activity, it executes pre-defined responses and notifies administrators.

### Sandboxing

Sandboxing is an approach Endpoint Protection Platforms use to prevent intrusions rather than detecting them. It is defined as a method of isolating untrusted data or software that is executed in the same address sapce as the trusted software. By executing suspicious software in an isolated envronemnt its behavior and output can be closely monitored and tested without having to worry that it will impact the entire system or network. Unlike traditional antivirus software, sandboxing actively monitors the behavior of unknown threats, making it especially useful against new vulnerabilities. It works by studying suspicious files in a controlled setting to decide if they are harmless or harmful. While sandboxing improves security and teaches us about how malware acts, we need to know that it can't always find very smart threats. Sandboxing should be part of a larger defense system to make endpoints safer.

#### Sandboxing Weaknesses

- Sandbox environments look slightly different to real environments and can therefore be detected by the malware
- A Sandbox can only handle and process files up to a certain size
- The attackers' software can also act as a trojan horse, act innocent during the sandboxing process and then infect the system when triggered afterwards.

### Antivirus and Antimalware

Antivirus and anti-malware software are indispensable for protecting digital devices from viruses and other threats. They use different techniques to identify and stop these threats, including:

- Scanning for known threats (signature-based scanning)
- Analyzing unknown threats based on patterns (heuristic analysis)
- Monitoring device behavior to detect suspicious activity (behavioral assessment)

These tools provide real-time protection, constantly scanning devices for threats and blocking them as they appear. They also perform scheduled scans to ensure all threats are caught. When threats are detected, the software often isolates or quarantines them for further investigation and action. Regular updates are essential for these tools to stay effective against new and evolving threats. Antivirus software refreshes its threat database automatically to recognize and combat the latest malware. In the intricate cybersecurity realm, antivirus and antimalware software team up with other security measures to ensure that endpoint devices function properly and their data remains secure.

### Firewalls

Firewalls are essential for protecting devices from cyber threats. They can be physical devices or software that monitor and filter data traffic based on defined security rules. Firewalls have evolved over time, leading to different types:

- Traditional Packet-Filtering Firewalls: They examine data packets individually.
- Stateful Inspection Firewalls: They track connections and inspect data within established connections.
- Proxy Firewalls: They act as intermediaries, controlling all communication between the network and external sources.
- Next-Generation Firewalls (NGFWs): They combine traditional features with advanced capabilities like application inspection and intrusion prevention. Firewalls regulate access, ensuring only authorized devices can communicate within the network. They also specify which applications can operate. Some modern firewalls support Virtual Private Networks (VPNs), enabling secure remote connections.

### Data Loss Prevention

Data Loss Prevention (DLP) is an essential part of protecting devices, especially in keeping sensitive data safe from people who shouldn't have it and trying to move it. DLP tools are designed to make sure data stays private and complete, whether it's moving, stored, or being used. Using smart detection and rules that have already been set up, DLP can find possible leaks or unauthorized movement of data. When it finds something that breaks the rules, it can tell admins or stop data from being transferred. This system helps prevent data from being accidentally leaked because of human error and stops insiders or malware from trying to steal data. DLP works well with other ways to protect devices, making endpoint protection more complete.

### Patch Management

Patch management is crucial for endpoint protection. It involves regularly updating software and systems to fix security flaws. As cyber threats change, software companies release patches to seal these vulnerabilities. Patch management ensures that these updates are obtained, tested, and installed on all devices in an organization. Without effective patch management, endpoints are vulnerable to attacks that exploit known flaws, giving hackers a chance to access systems. To enhance their cybersecurity, organizations should regularly update devices with the most recent security patches. This reduces the time that vulnerabilities are exposed, minimizing the impact of potential cyberattacks. As part of endpoint protection strategies, patch management plays a crucial role in proactively addressing known weak points, keeping organizations one step ahead of attackers.

### Machine Learning and AI

Endpoint protection software now commonly employs machine learning and artificial intelligence. These advanced technologies are particularly valuable in Endpoint Detection and Response systems, where they aid in promptly detecting and defending against threats, including previously undiscovered ones. In a rapidly changing cybersecurity environment, conventional defenses that rely on known signatures often falter against advanced cyberattacks. ML and AI bridge this gap by introducing predictive and proactive security measures. EDR systems leverage these technologies to learn continuously, identify novel threats, and provide comprehensive insights into potential breaches. This fusion not only improves detection capabilities but also optimizes security operations, ushering in a new era where intelligent technologies empower endpoint protection to stay ahead of cybercriminals.

## The Importance Of User Awareness and Training

Although cutting-edge technology and strong security protocols are vital for protecting endpoints, the human factor plays a key role in enhancing cybersecurity resilience. Training and educating users allows them to identify and address security risks effectively, reducing the potential impact of threats on the organization's overall security posture. By informing users about cybersecurity threats like phishing, social engineering schemes, and the need for secure passwords, we can significantly prevent successful attacks on devices. Training should also focus on: * Best practices for safely accessing and using sensitive data * Identifying suspicious activities or signs of compromise * Reporting security incidents in a timely manner. When businesses encourage employees to be aware of cybersecurity and adopt proactive security practices, they create an extra barrier of protection against threats aimed at specific devices or systems (endpoints). Educating and training users strengthens technical security measures, improving the overall ability of the organization to withstand cybersecurity attacks.

## References

- [https://ieeexplore.ieee.org/document/8945852](https://ieeexplore.ieee.org/document/8945852)
- [https://ieeexplore.ieee.org/document/1652120](https://ieeexplore.ieee.org/document/1652120)
- [https://ieeexplore.ieee.org/document/8939836](https://ieeexplore.ieee.org/document/8939836)
- [https://ieeexplore.ieee.org/document/6703683](https://ieeexplore.ieee.org/document/6703683)
- [https://ieeexplore.ieee.org/document/6016683](https://ieeexplore.ieee.org/document/6016683)
- [https://ieeexplore.ieee.org/document/9971847](https://ieeexplore.ieee.org/document/9971847)
- [https://ieeexplore.ieee.org/document/10314198](https://ieeexplore.ieee.org/document/10314198)
- [https://ieeexplore.ieee.org/document/646182](https://ieeexplore.ieee.org/document/646182)
- [https://ieeexplore.ieee.org/document/8082684](https://ieeexplore.ieee.org/document/8082684)
- [https://us.norton.com/internetsecurity-malware-what-is-a-computer-virus.html](https://us.norton.com/internetsecurity-malware-what-is-a-computer-virus.html)
- [https://techdocs.broadcom.com/us/en/symantec-security-software/endpoint-security-and-management/endpoint-security/sescloud.html](https://techdocs.broadcom.com/us/en/symantec-security-software/endpoint-security-and-management/endpoint-security/sescloud.html)
- [https://docs.broadcom.com/doc/endpoint-security-en](https://docs.broadcom.com/doc/endpoint-security-en)
- [http://acta.uni-obuda.hu//Vokorokos_Balaz_Mados_57.pdf](http://acta.uni-obuda.hu//Vokorokos_Balaz_Mados_57.pdf)
- [https://www.trellix.com/en-us/security-awareness/endpoint/what-is-endpoint-security.html](https://www.trellix.com/en-us/security-awareness/endpoint/what-is-endpoint-security.html)
- [https://www.trellix.com/en-us/security-awareness/endpoint/what-is-xdr.html](https://www.trellix.com/en-us/security-awareness/endpoint/what-is-xdr.html)
- [https://www.trellix.com/en-us/security-awareness/endpoint/what-is-endpoint-detection-and-response.html7](https://www.trellix.com/en-us/security-awareness/endpoint/what-is-endpoint-detection-and-response.html7)
- [https://www.trellix.com/en-us/security-awareness/endpoint/what-is-endpoint-encryption.html](https://www.trellix.com/en-us/security-awareness/endpoint/what-is-endpoint-encryption.html)
- [https://www.trellix.com/en-us/security-awareness/endpoint/what-is-endpoint-protection-software.html](https://www.trellix.com/en-us/security-awareness/endpoint/what-is-endpoint-protection-software.html)
- [https://www.trellix.com/en-us/security-awareness/endpoint/what-is-advanced-endpoint-protection.html](https://www.trellix.com/en-us/security-awareness/endpoint/what-is-advanced-endpoint-protection.html)
- [https://www.deepinstinct.com/glossary/next-generation-endpoint-security-nges](https://www.deepinstinct.com/glossary/next-generation-endpoint-security-nges)
- [https://www.eset.com/](https://www.eset.com/)
- [https://www.fireeye.de/](https://www.fireeye.de/)
- [https://securitycloud.symantec.com/cc/landing](https://securitycloud.symantec.com/cc/landing)
- [https://www.researchgate.net/publication/344170480_Sandbox_A_Secured_Testing_Framework_for_Applications](https://www.researchgate.net/publication/344170480_Sandbox_A_Secured_Testing_Framework_for_Applications)

Retrieved from "[https://wiki.elvis.science/index.php?title=Endpoint_Protection&oldid=14519](https://wiki.elvis.science/index.php?title=Endpoint_Protection&oldid=14519)"

[[file:///index.php?title=Special:Categories "Special:Categories"|Category]]:

- [[file:///index.php?title=Category:Basic "Category:Basic"|Basic]]