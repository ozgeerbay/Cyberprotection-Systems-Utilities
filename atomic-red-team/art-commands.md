# Atomic Red Team (ART) - Execution Reference

## Purpose
Provide reproducible commands to execute and inspect MITRE ATT&CK techniques using Atomic Red Team.

## Installation (Windows & Linux)
Run PowerShell 7:

```powershell
Install-Module -Name invoke-atomicredteam,powershell-yaml -Scope CurrentUser
IEX (IWR 'https://raw.githubusercontent.com/redcanaryco/invoke-atomicredteam/master/install-atomicsfolder.ps1' -UseBasicParsing);
Install-AtomicsFolder
