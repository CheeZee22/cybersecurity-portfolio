# Wazuh
Wazuh is an open-source EDR (Endpoint detection and response) software that provides:

* Security monitoring
* Intrusion detection
* Log analysis
* Compliance auditing
* File integrity monitoring
* Vulnerability detection
* Incident response

It is often used in Security Operations Centers (SOCs) and by IT teams to monitor infrastructure and detect threats across endpoints, servers, and cloud environments.  
<br>
The Use Cases are below;

* Intrusion Detection System (HIDS)
* SIEM alternative or enhancement
* Endpoint Threat Detection
* Security Monitoring for Cloud and On-Prem Systems
* Automated Compliance Checks

### How Wazuh Works
Wazuh is made up of 3 core components:

* **Agent**:
Installed on monitored endpoints (Windows, Linux, macOS). Collects logs, system data, file changes, etc.

* **Manager**:
Central brain of Wazuh. Receives data from agents, analyzes logs, triggers alerts, and applies rules.

* **Dashboard (Web UI)**:
A visual interface (typically running on Kibana or OpenSearch Dashboards) where security analysts view alerts, configure rules, and investigate incidents.

## Set-Up Wazuh
1. Install [Wazuh](https://wazuh.com/install/) (Review the requirements in Quickstart guide from the link attached.)
2. 
