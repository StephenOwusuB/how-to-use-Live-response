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

### Connecting to a Device
1. Go to **Assets and Devices**.
2. Select the device you intend to use Live Response on.
3. On the top right, select the three dots and click on **Live Response**.
4. The session will be established, showing the session ID, creator, start time, and device info.

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

### Managing Directories
- Change directory: `cd <directory>`
- List directory contents: `dir`
- Go up one level: `cd ..`
- View all live connections: `connections`
- Clear the command terminal: `cls` or `clear`

### Session Management
- Disconnect session: Click on **Disconnect Session** in the top bar.
- Review commands during the live session: Select **Command Log**.

### Limitations
- You can only use 25 live response sessions at a time.
- The inactive time limit is 15 minutes.
- One device can only be in one session at a time.

---

By following these steps and commands, you can effectively use Live Response for remote system investigations and immediate response actions.
