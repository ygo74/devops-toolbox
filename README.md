# devops-toolbox

Goals :  
* Ensure an operational environment to deploy codes on cloud providers.  
* Configure and use popular tools : Ansible, Powershell

Supported Cloud providers :
* Azure



## Visual studio Code Tips :
* Mardown Preview : CTLRL+SHIFT+V
* Markdwon Quick Reference : https://en.support.wordpress.com/markdown-quick-reference/  

## Visual Studio Code environment  


## Powershell tips
* Convert securestring to plain text  
```powershell
#Method 1
$UnsecurePassword = (New-Object PSCredential "user",$SecurePassword).GetNetworkCredential().Password  
$UnsecurePassword

#Method 2
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($SecurePassword)
$UnsecurePassword = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
$UnsecurePassword
```
