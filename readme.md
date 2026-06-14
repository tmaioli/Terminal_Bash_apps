Today's date is 6-9-2026 and we are using Microsoft's Intelligent Terminal

20261614: Uploaded PS script for System Information, test Qwen3-Coder, very impressed.

This is a test/demo setup for evaluating AI-generated PowerShell scripts for system diagnostics.

## Common Error: Execution Policy

If you encounter the following error when running the script:

```
You cannot run this script on the current system. For more information about running scripts and setting execution policy, see about_Execution_Policies at https://go.microsoft.com/fwlink/?LinkID=135170.
```

**Solution:** Run PowerShell as Administrator and execute one of the following commands to change the execution policy:

- For current user only (recommended):
  ```powershell
  Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
  ```

- For all users (requires Admin):
  ```powershell
  Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope LocalMachine
  ```

After setting the policy, you should be able to run the script successfully.
