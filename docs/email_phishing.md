# Email Phishing
Phishing emails are often the first step in a cyber attack. 
Hackers trick people into opening harmful files or links in emails that look real. 
Once opened, the hackers can put malware on the victim's computer, steal passwords and personal information, 
and even commit fraud or launch ransomware attacks.

As it is a common attack, analyzing the phishing emails are common work for the Security Operation Center Analyst role.
Here are some quick reference notes of procedures.



## Source Review
You can review the basic information of the potential Phishing emails in the sorce without special email analyzing tools.  
The source contains the information listed below;
- The sender's email address / IP address
- The time of the email delivery
- SPF, DKIM, and DMARC information
- DNS and delivery path
- The links which are contained within the email messages, etc.

### How-To (in Gmail)
1. Open the email in your Gmail inbox (DO NOT OPEN any attachments)
2. Click 3 vertical dots on the right corner > "<> Show original"

<br>

## <a href="https://talosintelligence.com/">Cisco Talos</a> (Research the collected information) 
This intelligence website helps to analyze the potential phishing email with the information you collected from the email. The Cisco Talos can pull the information listed below;
- Owner Details (IP address, Host name, Domain, Network owner)
- Email volume data
- Block lists
- Top IP Addresses used to send emails in the IP address which you searched by.
- WHOIS information, etc.

### How-To-Use
1. Access to the link <a href="https://talosintelligence.com/">Cisco Talos</a>
2. Search by IP, URL, domain, network owner, or file SHA256.  
    1. SHA256 can see in Terminal with the command: "sha256sum [File Name]"

The below is the screenshot of Cisco Talos IP address search result:  
![alt text](https://github.com/CheeZee22/cybersecurity-portfolio/blob/dde58c24e30c0f048187c2e9b79e220e704a6e03/pics/CiscoTalos.png "Cisco Talos")

<br>

## <a href="https://www.phishtool.com/">PhishTool</a> (Community versions)
PhishTool can do the following features;
- Perform email analysis - Retrieves metadata from the phishing emails.
- Analysis with OSINT - The tool has built-in OSINT (open-source intelligence).
- Classification and Reporting - Reports can be generated to provide a forensic record.

Unfortunately, the following features are available only on the Enterprise version;
- Manage user-reported phishing events.
- Report phishing email findings back to users and keep them engaged in the process.
- Email stack integration with Microsoft 365 and Google Workspace.

### How-To-Use
Firstly, you need to create an account and login. (The community version is free to use.)
1. Go to "Analysis" > Upload the potential phishing email (file format; .eml, .msg, and txt.)
2. Review the email details;  
    - Headers: the routing information of the email  
      (i.e., source and destination email addresses, Originating IP and DNS addresses and Timestamp.)
    - Received Lines: Details on the email traversal process across various SMTP servers for tracing purposes.
    - X-headers: Extension headers added by the recipient mailbox to provide additional information about the email.
    - Security: Details on email security frameworks and policies.  
      (i.e., Sender Policy Framework (SPF), DomainKeys Identified Mail (DKIM) and Domain-based Message Authentication, Reporting and Conformance (DMARC).)
    - Attachments: Lists any file attachments found in the email.
    - Message URLs: Associated external URLs found in the email will be found here.

