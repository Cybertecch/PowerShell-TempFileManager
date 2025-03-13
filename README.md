# README.md Content
# TempFileCleaner

TempFileCleaner is a PowerShell script that automates the deletion of temporary files from your system's temp directories every 24 hours. It helps free up disk space, improve system performance, and keep your system clean.

---
## Features

- **Automated Cleanup**: Deletes temporary files every 24 hours.
- **Customizable Directories**: Cleans multiple temp directories, including:
  - User Temp (`%TEMP%`)
  - System Temp (`%SystemRoot%\Temp`)
  - Prefetch (`%SystemRoot%\Prefetch`)
- **Error Handling**: Silently skips files or directories that cannot be deleted.
- **Easy to Use**: Run the script manually or schedule it as a task.

---
## Getting Started
### Prerequisites

- Windows OS
- PowerShell 5.1 or later

### Installation

1. Clone the repository:
   \`\`\`bash
   git clone https://github.com/yourusername/TempFileCleaner.git
   \`\`\`
2. Navigate to the repository:
   \`\`\`bash
   cd TempFileCleaner
   \`\`\`

### Usage

Run the script manually:
\`\`\`powershell
.\Delete-TempFiles.ps1
\`\`\`

---

## Automating the Script

To run the script automatically every 24 hours, set it up as a scheduled task in Windows Task Scheduler:

1. Open **Task Scheduler**.
2. Create a new task.
3. Set the trigger to **Daily** and configure it to repeat every 1 day.
4. Set the action to **Start a program** and point it to \`powershell.exe\`.
5. In the **Add arguments** field, enter:
   \`\`\`powershell
   -File "C:\path\to\Delete-TempFiles.ps1"
   \`\`\`
6. Save the task and ensure it runs with administrative privileges.
