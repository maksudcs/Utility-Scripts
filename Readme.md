# Utility Scripts readme



This repo contains some scripts that may come handy during development work. On what the different scripts specifically do take a look at their content, there is inline documentation.


## Installing PowerShell modules

Run the `AddCurrentPathToPSModulePath.ps1` script (you need admin privileges) to add the root of the respository to the `PSModulePath` environment variable. This will make PowerShell recognise this folder as one of the folders that contain PS modules. You only need to run this once - after that any changes made to these modules will be picked up automatically when a new PS console is opened.

In order to use these PowerShell scripts and modules you need to update to PowerShell 5.


## Developing PowerShell modules

Note that naturally you can also create Batch (.bat) or PowerShell (.ps1) scripts yourself that call these scripts when you repeatedly have to execute them with the same parameters.

1. Make a ModuleName folder.
2. Inside that folder make a ModuleName script with a ModuleName function (optionally you can use the `Cmdlet (advanced function)` snippet).
4. Ideally you should put your modules inside the repository's root folder, so after running `AddCurrentPathToPSModulePath.ps1` once the modules will be available on the system.


## Notes on developing scripts

- Always include appropriate documentation and usage examples in the header of the script on what the script does.
- Since people can create .bat files pointing to these scripts (as advised above) only change a script's path if it's absolutely inevitable, then communicate the change appropriately.