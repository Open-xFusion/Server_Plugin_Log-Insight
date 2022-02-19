#1. Content Pack Introduction

Log Insight is the VMware log management system. After the xFusion Log Insight content pack is installed,you can monitor and manage the sysLog logs reported by xFusion rack and blade servers, collect log statistics, analyze logs,view event change trends, and pre-customize alarm sending.You can quickly locate server problems and analyze potential server problems.

**Content Pack Name:**
- xFusion - HMM  v1.9.vlcp 
- xFusion - iBMC  v1.11.vlcp

**Supported Version:** 
- Log Insight 4.0.0 
- Log Insight 4.6.0
- Log Insight 4.8.0
- Log Insight 8.1.1
- Log Insight 8.4.1

**Mapping Software:** 
- MM910: (U54) 6.86D or later
- iBMC: 2.94 (U25) or later

**Supported Device:**
-   xFusion blade server:        E9000
-   xFusion rack server:         RH2288H V2, RH1288 V3, RH2288 V3, RH2288H V3, RH5885 V3, RH8100 V3, 1288H V5, 2288H V5, 2488 V5, 1288H V6 and 2288H V6
-   xFusion high-density server: XH321 V3, XH620 V3, XH622 V3, and XH628 V3

#2. Content Pack Functions
##iBMC content pack:
- **Dashboards:** 
The Overview, Security, System, and Operation pages are included. The view functions are as follows:
	- Change trends of different events
	- Statistics on and analysis of events of each server
	- Statistics on login failures, system error events, and operation error events
	- Statistics on proportion views of some events
	- Statistics on and analysis of operation events of each client

- **sysLog log parsing:** parsing of fields and meanings of sysLog events
- **Alarms:** Multiple Login Failure Alert and alarms triggered by major faults on boards

##HMM content pack:
- **Dashboards:**
The Overview, System, and Operation pages are included. The view functions are as follows:
	- Change trends of different events
	- Statistics on and analysis of events of each server
	- Statistics on login failures, system error events, and operation error events
	- Statistics on proportion views of some events
	- Statistics on and analysis of operation events of each client	

- **sysLog log parsing:** parsing of fields and meanings of sysLog events
- **Alarms:** Multiple Login Failure Alert and alarms triggered by major faults on boards

# 3. Verify the software package
You need obtained the Log Insight plug-in software package and verified its integrity.
1.	Obtain the Log Insight plug-in software package (for example,**Log Insight_V1.11.zip**) and its SHA256 verification file (for example,**Log Insight_V1.11.sha256.sum**) from GitHub.

2.	Verify the integrity of the Log Insight plug-in software package(on Linux).
	-	Go to the directory where the plug-in installation package and SHA256 verification file are stored.
	-	Run the **sha256sum -c < (grep** software package name sha256 verification file name) command to verify the software package.Example: **sha256sum -c <(grep Log Insight_V1.11.zip Log Insight_V1.11.sha256.sum)**
	-	Check whether the verification result is **OK**.
		-	If yes, the software package has not been tampered with and can be used.
		-	If no, the software package has been tampered with. Obtain a new software package.

# 4. Server Configuration
## iBMC Configuration
1.	Log in to the BMC WebUI as an administrator and choose **Alarm&SEL > Alarm Settings**.

2.	Set the following parameters in the **Syslog Notification Settings** area:
	-	**Syslog Notifications:** Set this parameter to ON.
	-	**Transmission Protocol:** Set this parameter to TCP or UDP.
	-	**Current Status:** Set this parameter to Enable.
	-	**Server Address:** Set this parameter to the IP address of the Log Insight server.
	-	**Syslog Port:** Set this parameter to 514.
	-	Set other parameters as required.

## HMM Configuration
1.	Log in to the HMM WebUI as an administrator and choose **System Management > Remote Syslog**.</b>

2.	Set the following parameters in the **Operation Logs** area:
	- **Syslog Status:** Set this parameter to ON.
	-	**Server Address:** Set this parameter to the IP address of the Log Insight server.
	-	**Transmission Protocol:** Set this parameter to TCP or UDP.
	-	Set other parameters as required.

3.	Set the following parameters in the **System Logs** area:
	-	**Syslog Status**: Set this parameter to ON.
	-	**Server Address**: Set this parameter to the IP address of the Log Insight server.
	-	**Transmission Protocol**: Set this parameter to TCP or UDP.
	-	Set other parameters as required.
