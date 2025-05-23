# FortiClient VPN

FortiClient is a comprehensive endpoint security solution designed to integrate seamlessly with the Fortinet Security Fabric. It provides advanced threat protection, ensures adherence to security policies, and facilitates secure remote access through its built-in VPN features. FortiClient can operate independently or in conjunction with FortiClient EMS (Enterprise Management Server) for centralized administration.

- [Installation](#installation)  
- [Getting Started](#installation-and-deployment)  
- [Installation and Deployment](#installation-and-deployment)  
- [Zero Trust Telemetry](#zero-trust-telemetry)  
- [Remote Access & VPN Configuration](#remote-access--vpn-configuration)  
- [Malware Protection & Antivirus](#malware-protection--antivirus)  

## Installation  
To begin with FortiClient VPN, download the installer by clicking the link below:

**[Download FortiClient VPN](https://github.com/fortinet-cl/FortiClient-VPN/releases/tag/7.4)**  

Installing FortiClient VPN is straightforward and quick. Simply download the appropriate installation file, follow the step-by-step instructions, and establish a secure connection within minutes. The process is optimized for Windows, macOS, and Linux platforms.

**System Requirements:**  
- **Windows:** Windows 10/11 (64-bit), Windows Server 2019 and later  
- **macOS:** Sonoma (14), Ventura (13), Monterey (12)  
- **Linux:** Ubuntu 18.04+, Red Hat 7.4+, CentOS 7.4+, Fedora 36+  

**Steps to Install:**  
1. Download the correct installer from Fortinet’s official website.  
2. Follow the specific instructions for your platform to complete the installation.  
3. Optionally connect the client to FortiClient EMS for centralized control.  
4. Configure the VPN settings and apply the desired security configurations.

>[!info] **Note:** Some advanced features require a licensed version activated through EMS.


## Installation and Deployment

### Installing on Windows  
1. Run the FortiClient installer (`.exe` or `.msi`).  
2. Agree to the End-User License Agreement.  
3. Select the components you wish to install.  
4. Continue through the installation wizard until it completes.  

**Silent CLI Installation:**  
```sh
FortiClientSetup_7.2.4_x64.exe /quiet /norestart /log c:\install.log
```

### Installing on macOS  
1. Open the `.dmg` file and run the installer package.  
2. Grant necessary system permissions when prompted.  
3. Reboot the device if required after installation.  

### Installing on Linux  
- **Ubuntu/Debian:**  
  ```sh
  sudo apt install ./forticlient_7.2.4_x86_64.deb
  ```  
- **Red Hat/CentOS:**  
  ```sh
  sudo yum install ./forticlient_7.2.4_x86_64.rpm
  ```  

>[!warning] **Caution:** Uninstall any conflicting security applications before installing FortiClient.


## Zero Trust Telemetry

Zero Trust Telemetry allows FortiClient to send endpoint health data to EMS and FortiGate devices, enhancing visibility and automating policy enforcement.

### Key Features:  
- Secure device identity validation  
- Real-time updates on endpoint security posture  
- Dynamic policy enforcement based on device trust level  

To activate telemetry:  
1. Open FortiClient and navigate to **Zero Trust Telemetry**.  
2. Enter the EMS server address to establish the connection.  
3. Confirm the connection and applied security policies.


## Remote Access & VPN Configuration

FortiClient supports both SSL and IPsec VPN protocols, providing secure remote access for users.

### Setting Up an SSL VPN  
1. Open FortiClient and go to **Remote Access**.  
2. Click **Add a new connection**, and select **SSL VPN**.  
3. Enter the server details and your user credentials.  
4. Save the profile and press **Connect** to start the session.

### Configuring IPsec VPN  
1. Go to **Remote Access > VPN**.  
2. Choose **IPsec VPN** and input the connection details.  
3. Add your authentication credentials and save the configuration.  
4. Connect to the VPN server.


## Malware Protection & Antivirus

FortiClient includes a robust malware engine capable of detecting and neutralizing threats in real time.

### Key Features:  
- Signature-based and behavior-based threat detection  
- Integration with Fortinet’s cloud-based threat database  
- Options for manual and scheduled scans

### To Perform a Manual Scan:  
1. Open FortiClient and go to **Malware Protection**.  
2. Choose between **Full Scan** or **Quick Scan**.  
3. Review the results and handle any detected threats appropriately.

>[!note] **Tip:** Enable real-time scanning to maintain ongoing protection against malicious files.


## Web Filtering & Application Firewall

### Web Filtering  
FortiClient uses a browser extension to filter HTTPS traffic and block access to potentially harmful or inappropriate websites.

- Define filter rules in **EMS > Web Filter**.  
- Activate the browser plugin for enhanced web protection.

### Application Firewall  
The application firewall inspects and manages network traffic generated by installed applications.

- Review blocked applications in **Application Firewall**.  
- Set custom firewall rules to control access at the application level.


## Vulnerability Scan & Security Compliance

FortiClient includes a scanner designed to detect system vulnerabilities and enforce compliance standards.

### Running a Scan:  
1. Open FortiClient and navigate to **Vulnerability Scan**.  
2. Click **Scan Now** to start the analysis.  
3. Review any issues found and implement necessary updates.


## Troubleshooting & Diagnostics

### Common Issues & Solutions  
- **VPN Connection Failure:** Double-check credentials and firewall settings.  
- **Telemetry Connection Error:** Verify EMS settings and ensure SSL certificates are correct.  
- **Antivirus Not Updating:** Confirm connection to FortiClient Cloud services.

### Diagnostic Tools  
FortiClient comes with built-in troubleshooting commands.  
```sh
forticlient_diag --check-connectivity
```


## Command-Line Interface (CLI) & API

### Helpful CLI Commands  
- **Check Software Version:**  
  ```sh
  forticlient --version
  ```  
- **Start VPN Connection:**  
  ```sh
  forticlient --vpn connect myvpn
  ```

### API Integration  
FortiClient supports integration via REST APIs for automation and management tasks.

- Consult the **FortiClient EMS API Guide** for in-depth documentation.  
- Use REST API endpoints to interact with and manage clients programmatically.
