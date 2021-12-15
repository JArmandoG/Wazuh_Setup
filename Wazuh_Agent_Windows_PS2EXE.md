## Convert .ps1 script to .exe

Tool used: [PS2EXE](https://www.powershellgallery.com/packages/ps2exe/1.0.10)

Use provided wazuh installation PS script:

```powershell
Invoke-WebRequest -Uri https://packages.wazuh.com/4.x/windows/wazuh-agent-4.2.4-1.msi -OutFile wazuh-agent-4.2.4.msi; ./wazuh-agent-4.2.4.msi /q    WAZUH_MANAGER='coqv7avkc7r9.cloud.wazuh.com' WAZUH_REGISTRATION_SERVER='coqv7avkc7r9.cloud.wazuh.com' WAZUH_REGISTRATION_PASSWORD='********************************'
```

1.- Install PS2EXE:

```powershell
Install-Module ps2exe
```

2.- Convert .ps1 to .exe:

```powershell
Invoke-ps2exe .input_script.ps1 .output.exe
```
