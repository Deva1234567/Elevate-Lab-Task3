Cybersecurity Internship Task 3: Vulnerability Scan Report
Objective
Perform a basic vulnerability scan on my local PC to identify common vulnerabilities, document critical issues, and propose mitigations using OpenVAS Community Edition.
Scan Setup

Policy: Basic Network Scan
Status: completed
Severity Base: CVSS v3.0
Scanner: Local Scanner
Start: Today at 9:13 AM
End: Today at 9:36 AM
Elapsed: 23 minutes


Methodology

On macOS/Linux: Open Terminal and type ifconfig or ip addr to find your IP address.
Alternatively, use localhost or 127.0.0.1 to scan your own machine.

Nessus Essentials:
Log in to the Nessus web interface.
Go to Scans > New Scan > Basic Network Scan.
Enter your local IP (e.g., 127.0.0.1) or localhost in the “Targets” field.


Nessus Essentials:
Visit the Tenable website (https://www.tenable.com/products/nessus/nessus-essentials).
Register for a free Nessus Essentials activation code.
Download and install Nessus Essentials for your operating system (Windows, macOS, or Linux).
Follow the on-screen instructions to complete the setup and activate using the code.


Critical Vulnerabilities Identified

1.CVE Record Found
View the CVE Record below. If you are searching for this CVE ID in other CVE Records, view the Other Results section below.

CVE-2023-46809
CNA: HackerOne

Node.js versions which bundle an unpatched version of OpenSSL or run against a dynamically linked version of OpenSSL which are unpatched are vulnerable to the Marvin Attack - https://people.redhat.com/~hkario/marvin/, if PCKS #1 v1.5 padding is allowed when performing RSA descryption using a private key.

2.CVE Record Found
View the CVE Record below. If you are searching for this CVE ID in other CVE Records, view the Other Results section below.

CVE-2024-22019
CNA: HackerOne

A vulnerability in Node.js HTTP servers allows an attacker to send a specially crafted HTTP request with chunked encoding, leading to resource exhaustion and denial of service (DoS). The server reads an unbounded number of bytes from a single connection, exploiting the lack of limitations on chunk extension bytes. The issue can cause CPU and network bandwidth exhaustion, bypassing standard safeguards like timeouts and body size limits.

3.CVE Record Found
View the CVE Record below. If you are searching for this CVE ID in other CVE Records, view the Other Results section below.

CVE-2024-27983
CNA: HackerOne

An attacker can make the Node.js HTTP/2 server completely unavailable by sending a small amount of HTTP/2 frames packets with a few HTTP/2 frames inside. It is possible to leave some data in nghttp2 memory after reset when headers with HTTP/2 CONTINUATION frame are sent to the server and then a TCP connection is abruptly closed by the client triggering the Http2Session destructor while header frames are still being processed (and stored in memory) causing a race condition.

Summary of Findings
The scan identified 68 vulnerabilities: 1 Critical, 4 High, 86 Medium, and 29 Low. The critical vulnerabilities involve outdated software (Apache and Java), which pose significant risks like remote code execution and data exposure. Immediate mitigation involves updating the affected software and applying firewall rules to limit exposure.
Screenshots

scan_summary.png: Overview of the scan results showing total vulnerabilities and severity distribution.
apache_vuln_details.png: Detailed view of apahe vulnerabilities in the nessus report.
java_vuln_details.png: Details of java vulnerabilities the nessus report.

Conclusion
This task provided hands-on experience with vulnerability scanning using NESSUS, highlighting the importance of keeping software updated and securing network configurations. The identified vulnerabilities underscore common PC risks, such as outdated software and exposed services, which can be mitigated through timely patches and system hardening.
