# 2019-5-12

## Ivan Torroledo, Luis David Camacho, Alejandro Correa Bahnsen: Hunting Malicious TLS Certificates with Deep Neural Networks. 64-73

https://doi.org/10.1145/3270101.3270105

**deep neural networks**

identifying malicious use of web certificates, uses the content of TLS certificates to successfully identify **legitimate certificates**, avoid investigating encrypted datas.

So far there exists no approach for TLS detection in the wild.

Feature engineering -> Presenting (One-Hot Encoding) -> Network Architecture (LSTM)

SOC - Secure Operation Center

One-Hot Encoding - 一位有效编码，其方法是使用N位状态寄存器来对N个状态进行编码，每个状态都由他独立的寄存器位，并且在任意时候，其中只有一位有效。

Recent work has focused on detecting malicious encrypted traffic by analyzing network connections in real time. This is done by investigating the encrypted malware communication with C2 servers, identifying the destination of such communication and then a DNS sinkhole is created to redirect the malware communication away from the C2 servers [27-1]. This represents a reactive approach because it must allow the malware to infect, propagate and execute its harmful action before it can be stopped. Furthermore, this approach needs to decrypt the communication in order to perform analysis of the malware’s content [34-1].

Another approach is based on certificate and IP address pivoting to keep track of threat actor infrastructure. Classification strategy for this approach is done by the use ofinternet scanning and blacklisting of IP addresses and certificates, so when a new connection is coming from any blacklisted IP or uses a known malicious certificate, the connection is classified as malicious [3-1, 29-1].

Most recent work avoids the pivoting and starts with a focus only on certificates by looking at digital certificates data. For example, researchers from the security company Splunk were able to achieve a 91% accuracy by classifying certificates used in malware activities by using a support vector machines (SVM) algorithm [32-1].

[3-1] Blake Anderson and David McGrew. 2016. Identifying Encrypted Malware Traffic with Contextual Flow Data. In Proceedings ofthe 2016 ACMWorkshop on Artificial Intelligence and Security (AISec ’16). ACM, New York, NY, USA, 35–46. https://doi.org/10.1145/2996758.2996768

[27-1] D. McGrew and B. Anderson. 2016. Enhanced telemetry for encrypted threat analytics. In 2016 IEEE 24th International Conference on Network Protocols (ICNP). 1–6. https://doi.org/10.1109/ICNP.2016.7785325

[29-1] Mark Parson. 2017. Using TLS certificates to track activity groups. Retrieved June 18, 2018 from https://www.slideshare.net/MSbluehat/ bluehat-v17-using-tls-certificates-to-track-activity-groups

[32-1] Dave Herrald Ryan Kovar. 2018. The “Hidden Empires” of Malware. Retrieved June 18, 2018 from https://www.sans.org/summit-archives/file/ summit-archive-1517253771.pdf

[34-1] Sourabh Saxena. 2016. Demystifying Malware Traffic. (August 2016), 1735–80.

## Peter Schneider, Konstantin Böttinger: High-Performance Unsupervised Anomaly Detection for Cyber-Physical System Networks. 1-12

https://doi.org/10.1145/3264888.3264890

**ML-based method.**

Industrial computer networks. [Fieldbus](https://www.wikiwand.com/en/Fieldbus), [Modbus](https://www.wikiwand.com/en/Modbus), EtherNet/IP.

a stacked denoising [autoencoder](https://www.wikiwand.com/en/Autoencoder) - Unsupervised learning.

a fully unsupervised learning-based processing pipeline.

avoiding overfitting - multiply the input bytes in $p^*$ with random values of a normal distribution giving a modified input vector $\tilde{p}^*$

pcap, scapy and pyshark

evaluated on Modbus and Secure Water Treatment (SWaT) database Common Industrial Protocol (CIP) over EtherNet/IP (EN/IP)

[3-2] Abdulmohsen Almalawi, Adil Fahad, Zahir Tari, Abdullah Alamri, Rayed Al-Ghamdi, and Albert Y Zomaya. 2016. An efficient data-driven clustering technique to detect attacks in SCADA systems. IEEE Transactions on Information Forensics and Security 11, 5 (2016), 893–906.

[9-2] Marco Caselli, Emmanuele Zambon, and Frank Kargl. 2015. Sequence-aware intrusion detection in industrial control systems. In Proceedings of the 1st ACM Workshop on Cyber-Physical System Security. ACM, 13–24.

[27-2] Stanislav Ponomarev and Travis Atkison. 2016. Industrial Control System Network Intrusion Detection by Telemetry Analysis. IEEE Transactions on Dependable and Secure Computing 13, 2 (2016), 252–260.

[32-2] Jiexin Zhang, Shaoduo Gan, Xiaoxue Liu, and Peidong Zhu. 2016. Intrusion detection in SCADA systems by traffic periodicity and telemetry analysis. In 2016 IEEE Symposium on Computers and Communication (ISCC). IEEE, 318–325.

## LIN

APP LAYER non-ML: DPI, more information with lower cost + details in another paper, tunnel HTTP (many connnection), need payload; take first few bytes

(protocol-based / content-based)

TCP/IP ML: use only header information -> network **flow** data -> models

## LI

DNS database: DNS attacks - (analyse papers are needed to be read)

Web extensions ad injection: DOM; triple -> intergrity model

# 2019-5-15

[Michael Backes, Thorsten Holz, Christian Rossow, Teemu Rytilahti, Milivoj Simeonovski, Ben Stock: On the Feasibility of TTL-Based Filtering for DRDoS Mitigation. 303-322](https://link.springer.com/chapter/10.1007%2F978-3-319-45719-2_14)

TTL-based countermeasures for DRDoS is not workable.

[Practical and Accurate Runtime Application Protection Against DoS Attacks](https://link.springer.com/chapter/10.1007%2F978-3-319-66332-6_20)

APP layer; Finite automated machine / tree

[Quentin Jacquemart, Pierre-Antoine Vervier, Guillaume Urvoy-Keller, Ernst W. Biersack: Demystifying the IP Blackspace. 111-132](https://link.springer.com/chapter/10.1007%2F978-3-319-26362-5_6)

Bogon is an informal term used to describe IP packets on the public Internet that claim to be from an area of the IP address space reserved, but not yet allocated or delegated by the Internet Assigned Numbers Authority (IANA) or any of the Regional Internet Registries (RIR).

[Samuel Jero, Md. Endadul Hoque, David R. Choffnes, Alan Mislove, Cristina Nita-Rotaru: Automated Attack Discovery in TCP Congestion Control Using a Model-guided Approach.](https://dblp.uni-trier.de/db/conf/ndss/ndss2018.html)

a **state machine model** of TCP congestion control to find vulnerable state machine paths that an attacker could exploit

[Synflood Spoofed Source DDoS Attack Defense Based on Packet ID Anomaly Detection with Bloom Filter](https://ieeexplore.ieee.org/abstract/document/8593121)

TCP, bloom filter

[Akshat Gaurav, Awadhesh Kumar Singh, "Entropy-score: A method to detect DDoS attack and flash crowd", 2017 2nd IEEE International Conference on Recent Trends in Electronics Information & Communication Technology, May, 2017.](https://ieeexplore.ieee.org/document/8256833)

Akshat Gaurav et al. (2017) proposed a DDoS attack detection method based on source **IP address entropy**. The basic idea of this method is that when the system is under a DDoS attack, the number of connections with different source IP addresses increases significantly compared to when the system is not. The method calculates the entropy for each group of source IP addresses. Two thresholds, threshold1 and threshold2, are used to determine when a DDoS attack occurs and which packets are malicious. The threshold1 is computed by the calculated entropy of each group and the threshold2 is computed by the Load Shedding algorithm.

[Traceroute-based target link flooding attack detection scheme by analyzing hop count to the destination](https://ieeexplore.ieee.org/abstract/document/8304023)

ICMP, TTL

[UWB with Pulse Reordering: Securing Ranging against Relay and Physical-Layer Attacks](https://www.ndss-symposium.org/ndss-paper/uwb-with-pulse-reordering-securing-ranging-against-relay-and-physical-layer-attacks/)

PHY layer. A enhancement for 802.15.4z Low Rate Pulse standard in security aspect.

---

TCP: Automated Attack Discovery,

IP/ICMP: Entropy-score, Traceroute-based target link flooding attack detection scheme;
