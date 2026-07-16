# Copilot Instructions for Terminal_Bash_apps

## Repository Overview

This is a collection of **PowerShell and Bash scripts** for system diagnostics, information gathering, and automation routines. The repository is organized by shell type, with scripts designed for Windows (PowerShell) and Linux (Bash) environments.

## Architecture

The repository follows a simple, shell-centric structure:

- **PowerShell Scripts (root directory)**: Windows-focused system diagnostics scripts using WMI/CIM queries
  - Typically include detailed comment headers (SYNOPSIS, DESCRIPTION, AUTHOR, DATE_GENERATED, PROGRAM_INTENT, etc.)
  - Return structured output as PSCustomObjects that can be piped to Format-List or Export-Csv
  - May include parameters for additional functionality (e.g., `-ExportCsv` switches)

- **Bash Directory**: Linux-focused scripts for environment configuration and system utilities
  - Placeholder README and Notes.md exist; actual scripts are planned
  - Intended for Ubuntu and other Linux distributions

## Running Scripts

### PowerShell Scripts

```powershell
# Run directly (may require execution policy adjustment)
.\Qwen_powershell_20260614.PS1

# With optional parameters
.\Qwen_powershell_20260614.PS1 -ExportCsv

# If execution policy error occurs, set policy for current user (recommended):
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

### Bash Scripts

```bash
# Make scripts executable
chmod +x script_name.sh

# Run the script
./script_name.sh
```

## Key Conventions

1. **Script Documentation**: All scripts include comprehensive comment-based headers at the top that document:
   - SYNOPSIS (one-line description)
   - DESCRIPTION (detailed explanation)
   - AUTHOR and DATE_GENERATED
   - PROGRAM_INTENT (purpose and use case)
   - INPUTS and OUTPUTS

2. **Sample Output**: Scripts include documented sample output in README files to show users what to expect when running the script.

3. **Git Considerations**: Remember that Git does not track empty directories. Always include at least one file (README.md, .gitkeep, etc.) in any new folder structure to ensure directories persist in the repository.

4. **CSV Export**: PowerShell scripts may support CSV export via optional parameters for integration with data analysis workflows.

## Before Making Changes

- **Windows Scripts**: Test PowerShell scripts on Windows 11 or similar; scripts rely on WMI/CIM which may vary across Windows versions
- **Linux Scripts**: Test Bash scripts on Ubuntu or other distributions mentioned in README
- **Compatibility**: Note any specific OS requirements in script headers and main README
- **Documentation**: Update relevant README files in the script's directory when adding or modifying scripts

## Testing Your Changes

- **PowerShell**: Run scripts with and without optional parameters to verify behavior
- **Output Format**: Verify that script output matches the sample output documented in README files
- **CSV Export** (if applicable): Verify that exported CSV files are well-formatted and contain expected data
