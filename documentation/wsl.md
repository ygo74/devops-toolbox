
Get-WindowsOptionalFeature -Online



Enable-WindowsOptionalFeature -FeatureName Microsoft-Windows-Subsystem-Linux -Online

$ProgressPreference = 'SilentlyContinue'
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1804 -OutFile Ubuntu-1804.appx -UseBasicParsing
Add-AppxPackage .\Ubuntu-1804.appx
# For wsl2
Enable-WindowsOptionalFeature -FeatureName VirtualMachinePlatform -Online

