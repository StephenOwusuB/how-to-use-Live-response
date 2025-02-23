## How to Use Live Response

Live response is a great tool for security operations teams. It allows them to connect to systems remotely in real-time, enabling them to investigate devices and take immediate response actions. Here's how you can use Live Response:

### Features
1. Basic and advanced commands
2. Download files (malware samples or some output of PowerShell)
3. Background downloads (download files in the background)
4. Upload a PowerShell script or executable to the library and run it on the device
5. Take remediation actions or undo any remediation actions

### Steps to Use Live Response
1. Make sure Live Response is turned on and the user has the right permissions.
2. Enable Live Response unsigned script execution if necessary (only digitally signed scripts can be run if this is off).
![Enable Live response](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2072.png)
### Connecting to a Device
1. Go to **Assets and Devices**.
2. Select the device you intend to use Live Response on.
3. On the top right, select the three dots and click on **Live Response**.
4. The session will be established, showing the session ID, creator, start time, and device info.
   ![Connect live response](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2073.png)
   ![Connect live response](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2074.png)
    ![Connect live response](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2075.png)
   
### Basic Commands
- Start a live response session: `Start-DefenderResponseSession`
- Run a command in the background: `bg <command ID>`
- Resume a suspended command: `fg <command ID>`
- List running and suspended commands: `jobs`
- Collect a file: `collect-file <file path>`
- Get a process tree: `findget-process-tree`
- Run an antivirus scan: `run-avscan`
- Query system information: `get-systeminfo`
- Delete a file: `delete-file <file path>`
- Download a file to your local machine: `getfile <file path>`
- View all processes: `process`
- View all scheduled tasks: `scheduledtask`
- View all services: `services`
- View all known files in the startup folder: `startupfolders`
- Enable debug mode: `trace`
 ![Basic commands](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2076.png)
![Basic commands](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2077.png)
![Basic commands](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2078.png)
![Basic commands](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2079.png)
![Basic commands](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2080.png)
![Basic commands](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2081.png)
![Basic commands](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2082.png)
![Basic commands](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2083.png)
![Basic commands](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2084.png)
![Basic commands](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2085.png)
![Basic commands](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2086.png)
![Basic commands](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2087.png)
![Basic commands](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2088.png)
![Basic commands](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2089.png)



### Advanced Commands
- View files uploaded to the live response library: `library`
- Upload a file to the library (use the UI on the top right)
- Disconnect the device from the network: `isolate`
- Release an isolated device: `release`
- Run a script: `run <script name>`
- Run a scan: `scan`
- Analyze whether a file has malware: `analyze file <file path>`
- Analyze whether a process is malicious: `analyze process <process ID>`
- Upload files from the library: `putfile`
- Remediate a file: `remediate file <file path>`
- Undo remediation: `undo file <file path>`
![Advanced comnands](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2091.png)
![Advanced comnands](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2094.png)
![Advanced comnands](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2095.png)
![Advanced comnands](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2096.png)
![Advanced comnands](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2097.png)
![Advanced comnands](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2098.png)

### Managing Directories
- Change directory: `cd <directory>`
- List directory contents: `dir`
- Go up one level: `cd ..`
- View all live connections: `connections`
- Clear the command terminal: `cls` or `clear`

### Session Management
- Disconnect session: Click on **Disconnect Session** in the top bar.
- Review commands during the live session: Select **Command Log**.
![Advanced comnands](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2092.png)
![Advanced comnands](https://github.com/StephenOwusuB/Implementing-Microsoft-Defender-for-Enterprise-Security/blob/main/images/live%20response/MDE%20onboard%2093.png)
### Limitations
- You can only use 25 live response sessions at a time.
- The inactive time limit is 15 minutes.
- One device can only be in one session at a time.

---

By following these steps and commands, you can effectively use Live Response for remote system investigations and immediate response actions.
