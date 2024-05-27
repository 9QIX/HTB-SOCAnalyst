# Skills Assessment

To keep you sharp, your SOC manager has assigned you the task of analyzing older attack logs and providing answers to specific questions.

Navigate to the bottom of this section and click on Click here to spawn the target system!

RDP to [Target IP] using the provided credentials, examine the logs located in the C:\Logs\* directories, and answer the questions below.

```bash
z0x9n@htb[/htb]$ xfreerdp /u:Administrator /p:'HTB\_@cad3my_lab_W1n10_r00t!@0' /v:[Target IP] /dynamic-resolution
```

## Questions

Answer the question(s) below to complete this Section and earn cubes!

### Question 1

+3 By examining the logs located in the `C:\Logs\DLLHijack` directory, determine the process responsible for executing a DLL hijacking attack. Enter the process name as your answer.

**Answer format:** `_.exe`

1. Open saved `.evtx` file from `C:\Logs\DLLHijack`.
2. Filter `wininet.dll`
3. Check for `Image:` part.
4. Answer: `Dism.exe`

### Question 2

+2 By examining the logs located in the `C:\Logs\PowershellExec` directory, determine the process that executed unmanaged PowerShell code. Enter the process name as your answer.

**Answer format:** `_.exe`

1. Open saved `.evtx` file from `C:\Logs\PowershellExec`.
2. Filter `clr.dll`
3. Check for `Image:` part.
4. Answer: `Calculator.exe`

### Question 3

+3 By examining the logs located in the `C:\Logs\PowershellExec` directory, determine the process that injected into the process that executed unmanaged PowerShell code. Enter the process name as your answer.

**Answer format:** `_.exe`

### Question 4

+2 By examining the logs located in the `C:\Logs\Dump` directory, determine the process that performed an LSASS dump. Enter the process name as your answer.

**Answer format:** `_.exe`

### Question 5

+1 By examining the logs located in the `C:\Logs\Dump` directory, determine if an ill-intended login took place after the LSASS dump.

**Answer format:** Yes or No

### Question 6

+2 By examining the logs located in the `C:\Logs\StrangePPID` directory, determine a process that was used to temporarily execute code based on a strange parent-child relationship. Enter the process name as your answer.

**Answer format:** `_.exe`
