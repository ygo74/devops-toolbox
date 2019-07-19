# Powershell tips
## Convert securestring to plain text
```powershell
#Method 1
$UnsecurePassword = (New-Object PSCredential "user",$SecurePassword).GetNetworkCredential().Password
$UnsecurePassword

#Method 2
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($SecurePassword)
$UnsecurePassword = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
$UnsecurePassword
```

## Winrm
```powershell
winrm set winrm/config/service @{AllowUnencrypted="true"}
winrm set winrm/config/service/auth @{Basic="true"}
```

## Script Analyser

### Supress rules
[Diagnostics.CodeAnalysis.SuppressMessageAttribute("PSAvoidDefaultValueForMandatoryParameter", "" )]

## Persistent Modify environment variable 

```Powershell
# Get current value
$CurrentValue = [Environment]::GetEnvironmentVariable("PSModulePath", "Machine")
# Modify current value with your folder
[Environment]::SetEnvironmentVariable("PSModulePath", $CurrentValue + ";D:\devel\github\devops-toolbox\cloud\azure\powershell\modules\MESF_Azure", "Machine")
```
> :warning:  
> __Restart your development editor or powershell session__
