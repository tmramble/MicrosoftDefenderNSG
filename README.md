# NSG Flow Logs and Monitoring Project

This project focuses on enabling and configuring NSG Flow Logs, collecting data from virtual machines, and integrating with Microsoft Sentinel for enhanced monitoring and analytics.

## ⚙️ Project Checklist - NSG Flow Logs and Monitoring Setup
1. **Create an Azure Storage Account** (e.g., `sacyberlab0x`) in the same region as the VMs.
2. **Enable Flow Logs** for both Network Security Groups (NSGs) and send logs to Log Analytics Workspace.
3. If no storage account is listed, create a new one in the same region as the VMs.
4. **Configure Data Collection Rules (DCR)** for VMs within Microsoft Sentinel.
5. **Ensure VMs are powered on.**
6. **Install "Windows Security Events"** from Sentinel Content Hub and configure Security Data Sources for appropriate VMs.
7. **Install "Syslog"** from Sentinel Content Hub for Linux VMs (Auth: Debug only).
8. **Verify agent installation** under VM > Settings > Extensions Applications (Provisioning succeeded).
9. **Query Log Analytics** for the following:
   - **Syslog** (Linux)
   - **SecurityEvent** (Windows)
   - **AzureNetworkAnalytics_CL** (NSGs)
10. **Generate test logs** (e.g., failed logons) and observe in Log Analytics.
11. **Shut down VMs** after confirming log ingestion to save costs.

---

## 📊 Visual Recap
**Logging and Monitoring:** Enable MDC and Configure Log Collection for Virtual Machines.  
Ensure logs from **Linux**, **Windows**, and **NSGs** are visible in Log Analytics before concluding the lab.
