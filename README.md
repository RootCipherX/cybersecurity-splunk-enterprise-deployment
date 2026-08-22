# Cybersecurity: Splunk Enterprise SIEM Deployment & Configuration

## Table of Contents
- [Introduction to Splunk](#-introduction-to-splunk-enterprise-siem)
- [Project Overview](#-project-overview)
- [Objective](#-objective)
- [System Specifications](#️-system-specifications)
- [Deployment Methodology Workflow](#-deployment-methodology-workflow)
  - [Phase 1: Account Provisioning & Package Acquisition](#phase-1-account-provisioning--package-acquisition)
  - [Phase 2: Local Installation & Configuration](#phase-2-local-installation--configuration)
  - [Phase 3: Service Initialization & Dashboard Access](#phase-3-service-initialization--dashboard-access)
- [Security Relevance & Impact](#-security-relevance--impact)
- [Ethical Guidelines & Disclaimer](#️-ethical-guidelines--disclaimer)

---

## Introduction to Splunk Enterprise (SIEM)
**Splunk Enterprise** is an industry-leading platform utilized by Security Operations Centers (SOCs) for searching, analyzing, and visualizing machine-generated data in real-time. In the cybersecurity domain, it functions as a powerful Security Information and Event Management (SIEM) tool. Splunk ingests massive volumes of logs from networks, servers, and applications, allowing security analysts to detect anomalies, investigate breaches, and monitor the overall health and security posture of an IT infrastructure.

## Project Overview
This project documents the end-to-end deployment of a local Splunk Enterprise instance. It details the workflow of provisioning an authorized Splunk account, acquiring the correct enterprise binaries, executing a secure local installation on a Windows environment, creating local administrative credentials, and successfully initializing the Splunk Web interface.

## Objective
To establish a functional, locally-hosted SIEM environment capable of indexing log data. This baseline installation will serve as the foundation for future advanced cybersecurity labs, including log ingestion, custom dashboard creation, and threat hunting.

## System Specifications
*   **Operating System Environment:** Windows / Windows Server Architecture[cite: 9]
*   **Software Version:** Splunk Enterprise 10.4.2 (64-bit)[cite: 9]
*   **Installer Type:** Windows Installer Package (`.msi`)[cite: 9]
*   **Web Interface Access:** `localhost:8000`

---

## Deployment Methodology Workflow

### Phase 1: Account Provisioning & Package Acquisition
**Objective:** To register for the Splunk developer/trial program and obtain the official enterprise binaries.

1.  **Portal Access & Registration:** Navigated to the official Splunk Free Trials & Downloads portal and initiated the account creation process[cite: 1, 2, 3].
2.  **Verification:** Provided organizational details and verified the account creation via a One-Time Password (OTP) delivered securely to the registered business email[cite: 4, 5, 6, 7].
3.  **Binary Acquisition:** Accessed the Splunk Enterprise product catalog and selected the 64-bit `.msi` Windows installer for version 10.4.2[cite: 8, 9]. 
4.  **License Agreement:** Reviewed and accepted the Splunk General Terms to authorize the software download[cite: 10].

**Result / Evidence:**
The 1.04 GB binary (`splunk-10.4.2-33c3bf42cd73-windows-x64.msi`) was successfully downloaded to the local environment.
<br>

*(Insert images: 6-fill-the-form-2.jpg, 7-otp-will-receive-via-email.png, 9-select-click-download.png, 12-splunk-setup-msi.png)*

---

### Phase 2: Local Installation & Configuration
**Objective:** To execute the MSI installer and configure the core Splunk services and administrative access controls.

1.  **EULA & Directory Setup:** Executed the installer, accepted the end-user license agreement, and verified the default installation path (`C:\Program Files\Splunk`).
2.  **Service Configuration:** Configured Splunk Enterprise to run securely as a Local non-administrator Virtual Service account, enforcing the Principle of Least Privilege.
3.  **Access Control:** Created a highly secure `admin` account with a robust password to govern access to the Splunk Web interface.
4.  **Execution:** Initiated the installation wizard, allowing the system to generate script operations, unpack binaries, and update the Windows component registry.

**Result / Evidence:**
Splunk Enterprise was successfully installed without errors, and the core services were bound to the local machine.
<br>

*(Insert images: 13-accept-license.png, 14-give-username-password.png, 18-updating-regristry.png, 19-installation-completed.png)*

---

### Phase 3: Service Initialization & Dashboard Access
**Objective:** To verify that the Splunk Web interface is active, listening on the correct port, and successfully accepting administrative logins.

1.  **Web Interface Access:** Launched a local web browser and navigated to the default Splunk management port via `localhost:8000`.
2.  **Authentication:** Successfully authenticated against the local service using the administrative credentials created during Phase 2.
3.  **Dashboard Verification:** Accessed the primary Splunk Administrator Dashboard. Verified that default modules such as "Search & Reporting," "Audit Trail," and "Splunk Secure Gateway" were actively loaded and ready for log ingestion.

**Result / Evidence:**
<br>

*(Insert images: 20-splunk-login-page.jpg, 22-splunk-dashboard.png)*

---

## Security Relevance & Impact
Setting up a SIEM like Splunk is a foundational skill for Blue Team operations and SOC analysts. A properly configured Splunk environment allows security teams to:
*   **Centralize Log Management:** Aggregate Windows Event Logs, Sysmon data, and firewall traffic into a single pane of glass.
*   **Threat Hunting:** Query massive datasets to identify Indicators of Compromise (IoCs), lateral movement, or unauthorized access attempts.
*   **Incident Response:** Create automated alerts and real-time dashboards to reduce the Mean Time to Detect (MTTD) and Mean Time to Respond (MTTR) to active cyber threats.

---

## ⚖️ Ethical Guidelines & Disclaimer
This installation and configuration process was performed within a private, authorized laboratory environment strictly for educational and defensive cybersecurity training purposes.
