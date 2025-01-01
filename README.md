

# NSG Flow Logs and Virtual Machine Monitoring  
**Project Overview**  
In this project, I configured NSG Flow Logs and integrated virtual machine (VM) log collection into Microsoft Sentinel. The goal was to enable detailed network traffic logging, set up data collection from both Linux and Windows VMs, and ensure comprehensive monitoring using Azure Log Analytics. This project enhanced my ability to monitor VM activity, network traffic, and security events across cloud environments.

---

**Steps Taken and Configurations**  

1. **Azure Storage Account Creation**  
   - **Resource:** `sacyberlab0x` (Storage Account)  
   - **Purpose:** This storage account was created to store NSG Flow Logs and ensure proper integration with VMs within the same region.  

2. **Enable Flow Logs for NSGs**  
   - **Configuration:** Flow logs were enabled for all relevant NSGs and set to send data to the Log Analytics Workspace.  
   - **Challenge:** If no storage account was listed, I created a new one in the appropriate region to match the VMs' location.  

3. **VM Data Collection Rules (DCR) Setup**  
   - **Action:** Configured Data Collection Rules (DCR) within Microsoft Sentinel for both Windows and Linux VMs.  
   - **Status:** Confirmed that VMs were powered on and ready to collect data.  

4. **Content Hub Integration (Microsoft Sentinel)**  
   - **Windows Security Events (DCR-Windows):**  
     - Installed from the Content Hub.  
     - Configured security data sources for the appropriate VMs.  
   - **Syslog (DCR-Linux):**  
     - Installed Syslog and set Linux VMs to collect logs with `Auth: Debug only` configuration.  

5. **Agent Verification and VM Extensions**  
   - **Verification:** Checked under VM > Settings > Extensions Applications to ensure the agent was installed successfully (Provisioning succeeded).  

6. **Log Collection and Analysis**  
   - **Log Queries:** Queried Log Analytics to confirm ingestion from three sources:  
     - **Syslog (Linux)**  
     - **SecurityEvent (Windows)**  
     - **AzureNetworkAnalytics_CL (NSG Flow Logs)**  

7. **Testing and Validation**  
   - Simulated failed login attempts on both Windows and Linux VMs to test log generation.  
   - Verified the visibility of these logs in Microsoft Sentinel’s Log Analytics Workspace.  

---

**Key Learnings**  
- **NSG Flow Logs and Monitoring:** This project reinforced my understanding of NSG Flow Logs and the importance of collecting VM logs for security and monitoring.  
- **Log Analytics Integration:** I gained hands-on experience integrating VM logs with Microsoft Sentinel and ensuring consistent data collection across environments.  
- **Security Best Practices:** By testing user activity through simulated failed logins, I better understood how to track and respond to security events in Azure.  

---

**Technologies Used**  
- **Azure Storage Accounts**  
- **Azure NSG (Network Security Groups)**  
- **Microsoft Sentinel**  
- **Azure Log Analytics**  

---

**Conclusion**  
This project provided valuable hands-on experience in configuring NSG Flow Logs, setting up data collection for VMs, and integrating security monitoring tools in Azure. The ability to log and analyze data from multiple sources ensures a more secure and well-monitored cloud environment. These skills are essential for roles involving cloud security, monitoring, and incident response.
