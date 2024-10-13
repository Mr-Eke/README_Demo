# Heart Rate Monitoring System

## Project Overview  
This project aims to develop a system for **recording heart rate data**, **archiving logs**, and **backing them up to a remote server**. The project includes three main tasks, each implemented as a shell script:
1. **Heart Rate Monitoring Script**
2. **Log Archival Script**
3. **Archival and Backup Script**

These scripts are part of a hospital’s system upgrade to improve patient monitoring and data management.

---

## Setup Instructions

### Prerequisites:
- A Unix/Linux environment with Bash installed
- SSH access to a remote server (one of the group members' sandbox)
- Proper permissions to run scripts and create directories

### Instructions:

### Task 1: Heart Rate Monitoring Script
#### Script Name: `heart_rate_monitor.sh`

This script records heart rate data every second from a specified monitoring device.

1. **Download the Script**:  
   Place the `heart_rate_monitor.sh` script in your desired working directory.

2. **Make the Script Executable**:
   ```bash
   chmod +x heart_rate_monitor.sh
   ```

3. **Run the Script**:
   ```bash
   ./heart_rate_monitor.sh
   ```

4. **Enter Device Name**:
   When prompted, enter the name of the monitoring device (e.g., "Monitor_A").

5. **Background Process**:
   The script will run in the background, and the Process ID (PID) will be displayed. To check the log output, use:
   ```bash
   tail -f heart_rate_log.txt
   ```

---

### Task 2: Log Archival Script
#### Script Name: `archive_log.sh`

This script archives the heart rate log file by renaming it with a timestamp.

1. **Download the Script**:  
   Place the `archive_log.sh` script in your working directory.

2. **Make the Script Executable**:
   ```bash
   chmod +x archive_log.sh
   ```

3. **Run the Script**:
   ```bash
   ./archive_log.sh
   ```

4. **Check Archive**:  
   The original `heart_rate_log.txt` will be renamed to `heart_rate_log.txt_YYYYMMDD_HHMMSS` with the timestamp of when the script was executed.

---

### Task 3: Archival and Backup Script
#### Script Name: `backup_archives.sh`

This script moves the archived log files to a designated directory and backs them up to a remote server using SSH.

1. **Download the Script**:  
   Place the `backup_archives.sh` script in your working directory.

2. **Make the Script Executable**:
   ```bash
   chmod +x backup_archives.sh
   ```

3. **Set Up SSH Access**:
   Ensure you have SSH access to the remote server with the appropriate credentials. Use the sandbox host details provided by your group.

4. **Run the Script**:
   ```bash
   ./backup_archives.sh
   ```

5. **Check Backup**:  
   Archived files will be moved to the `archived_logs_group$` directory (replace `$` with your group number) and then securely copied to the remote server using `scp`.

---

## Group Session Attendance Report

The team met several times during the development of this project. Below is a summary of attendance during group sessions:

### Session 1: Initial Planning (Date: 2024-10-01)
- **Present**: Alice, Bob, Charlie, David
- **Absent**: None

### Session 2: Task 1 Implementation (Date: 2024-10-03)
- **Present**: Alice, Charlie, David
- **Absent**: Bob (excused)

### Session 3: Task 2 Implementation (Date: 2024-10-05)
- **Present**: Bob, Charlie, David
- **Absent**: Alice (excused)

### Session 4: Task 3 Implementation & Final Testing (Date: 2024-10-07)
- **Present**: Alice, Bob, Charlie, David
- **Absent**: None

---

## Contact Information

For any questions or issues with setup, please contact:
- Alice (Project Manager): alice@example.com
- Bob (Lead Developer): bob@example.com
- Charlie (Systems Engineer): charlie@example.com
- David (Backup Specialist): david@example.com

---

Thank you for using the **Heart Rate Monitoring System**!
