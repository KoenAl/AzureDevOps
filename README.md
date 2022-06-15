#  Azure DevOps Powershell pipeline for .NET Core API & SPA


Dont want to use standard default powershell tasks in Azure DevOps pipeline ? (to increase performance)

Not ready to make that switch to YAML? Want incremental functionality build in? Use this as as a reference. This is an incremental script based on the 

```powershell
$Last-Release
```
Incremental will be turned off if a new release is created

## Installation

Just copy paste the .ps1, create task groups.



## Usage

These scripts only use 2 azure devops environmental variables, because inline has a character limit the variables will be exported to wherever the deployment agent is running.

## Expected naming convention and hierachy

This pipeline only works if the following naming convention is used:

```powershell
#<STAGE>:<REGION>:<ARTIFACT>
#PROD:EU:Api-master-CI

```

## Known bugs

Currently there is a bug where Last-release is somehow the last-artifact. Will update this at some point.


```powershell

#Change these credentials
$azureAplicationId = ""
$azureTenantId = ""
$azurePassword = ConvertTo-SecureString "" -AsPlainText -Force
$psCred = New-Object System.Management.Automation.PSCredential($azureAplicationId , $azurePassword)
$subscription = ""

```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
Free to use as you'd like