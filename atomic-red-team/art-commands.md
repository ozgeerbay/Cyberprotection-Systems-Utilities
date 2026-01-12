# Atomic Red Team (ART) - Execution Reference

## Purpose
Provide reproducible commands to execute and inspect MITRE ATT&CK techniques using Atomic Red Team.

## Installation (Windows & Linux)
Run PowerShell 7:

```powershell
Install-Module -Name invoke-atomicredteam,powershell-yaml -Scope CurrentUser
IEX (IWR 'https://raw.githubusercontent.com/redcanaryco/invoke-atomicredteam/master/install-atomicsfolder.ps1' -UseBasicParsing);
Install-AtomicsFolder
```

Verify installation:
```powershell
Invoke-AtomicTest T1003 -ShowDetailsBrief
Invoke-AtomicTest T1003 -CheckPrereqs
```
## Technique execution examples 
### Exfiltration — T1048 (Linux)

```powershell
Invoke-AtomicTest T1048 -ShowDetailsBrief
Invoke-AtomicTest T1048 -TestNumbers 4
```

### Impact — T1486 (Windows)
Ransomware risk - review only:

```powershell
Invoke-AtomicTest T1486 -ShowDetailsBrief
```

If executed in lab context:
```powershell
Invoke-AtomicTest T1486 -TestNumbers 10
```

## Cleanup (when available)

```powershell
Invoke-AtomicTest <TECHNIQUE> -Cleanup
```













