The following clean, refactored Markdown represents the corrected and streamlined version of the file, ready to be applied directly to the repository update:

```markdown
# System Information & Utilities Repository

A collection of PowerShell and Bash scripts for system diagnostics, information gathering, and utilities designed for automated deployment and environment profiling.

## 📅 Repository Info

* Last Updated: July 7, 2026
* Primary Focus: System information gathering and diagnostics
* Tested On: Windows 11, Ubuntu

## 📁 Repository Structure


```text

/workspace/
├── Qwen_powershell_20260614.PS1    # PowerShell system info script
├── PS_System_Information           # Sample output from PowerShell script
├── README.md                       # This file
├── .gitignore                      # Git ignore rules
└── Bash/
├── README                      # Bash scripts documentation
└── Notes                       # GitHub directory creation guide

```

## ⚙️ Automation and Script Capabilities

The primary operational objective of this codebase is to automate repetitive system tasks, gather precise environment diagnostics, and optimize local machine deployment. Within the Linux ecosystem, the scripts focus on environment customization, routine maintenance, and terminal optimization, allowing for rapid machine setup with minimal manual intervention. On the system information front, the repository leverages specialized administrative scripts—such as the included PowerShell modules—to query underlying hardware architectures, audit operating system configurations, and log vital system metrics. This multi-shell approach provides a comprehensive administrative framework, enabling rapid execution of diagnostic checks and system configurations from a single, lightweight repository.

## 🔧 PowerShell Scripts

### Qwen_powershell_20260614.PS1

A comprehensive system information gathering script that collects hardware and OS details using WMI/CIM queries.

#### Features
* Computer name and manufacturer
* Hardware model
* Operating system version
* CPU model and core count
* Total and free RAM (in GB)
* Free disk space on C: drive (in GB)
* System uptime

#### Requirements
* PowerShell with CIM/WMI access
* Windows OS (tested on Windows 11)

#### Usage

```powershell
# Run the script
.\Qwen_powershell_20260614.PS1

# Optional: Export to CSV (uncomment line 64 in script)
# $report | Export-Csv -Path "SystemInfo.csv" -NoTypeInformation

```

#### Sample Output

```text
ComputerName : HP-LAPTOP-2021
Manufacturer : HP
Model        : HP Laptop 17
OS           : Microsoft Windows 11 Home Insider Preview
CPU          : AMD Ryzen 5 5500U with Radeon Graphics
Cores        : 6
RAM_Total_GB : 31.33
RAM_Free_GB  : 18.41
Disk_C_Free  : 487.13
Uptime       : 08:12:53.0575772

```

## ⚠️ Common Error: Execution Policy

If you encounter an execution policy error preventing the script from running on your current system, run PowerShell as an Administrator and execute one of the following commands to update your execution boundaries.

For the current user only (recommended):

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser

```

For all users (requires Administrator privileges):

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope LocalMachine

```

## 🐚 Bash Scripts

The Bash subdirectory contains dedicated environment configuration assets and automation routines tailored specifically for Linux environments. This includes explicit system execution notes and localized deployment logic designed to streamline terminal-based workflows. For detailed setup instructions and shell script execution parameters, please refer directly to the documentation contained within the internal Bash folder files.

## 📝 Notes

* This repository is utilized for testing, validating, and archiving automated, AI-assisted scripts focused on system diagnostics.
* Because Git does not track empty directories natively, ensure all newly created structural folders contain at least one anchor file, such as a localized README or a configuration asset.
* Refer to the internal documentation path for step-by-step guidance on establishing clean directory creation hierarchies directly within a remote interface.

```

```
