## Synopsis

This project contains PowerShell scripts that allows you to perform various operations with SQL Server Reporting Services. In order to use the scripts included in this project successfully, please download/clone the entire project as there are dependencies between the scripts. 

All of our scripts were written with the assumption that you will be executing them against SQL Server 2016 Reporting Services default instance (i.e. mssqlserver). However, we understand this may not be the case for you. So for each script, you will see that we have provided a way for you to specify the name and/or version of your SQL Server Reporting Services instance name. Sometimes the version of your SQL Server instance is also required. If you do not provide one, we will assume that you want to execute this against the default instance.    

## Installation

You can either download this repository as a Zip file or clone this repository on your machine. Unfortunately, at the moment, we do not have an installer that will install all our commands into your PowerShell environment permanently. 

Every time you launch PowerShell or start a new PowerShell session, you MUST run the following command. This will load up all our commands into your environment and allow you to run any of the commands listed in "List of Commands" section within the PowerShell session. 
    
    . Setup.ps1 

## List of commands

The following is a list of commands which are available for you to use once you follow the steps in Installation section. In order to view detailed information of how to use any of the following commands, please run "Get-Help *command_name*". 

|Command|Description|
|-------|-----------|
|Backup-RSEncryptionKey|This command backs up the encryption key used by SQL Server Reporting Services to protect sensitive content.|
|Grant-AccessOnCatalogItem|This command grants access on catalog item to users or groups.|
|Grant-AccessToRS|This command grants access to SQL Server Reporting Services to users or groups.|
|New-RSConfigurationSettingObject|This command creates a new RSConfigurationSettingObject which is used to interact with the WMI Provider.|
|New-RSWebServiceProxy|This command creates a new Web Service Proxy which is used to interact with the SOAP Endpoint.|
|Register-PowerBI|This command registers Power BI information with SQL Server Reporting Services.|
|Restore-RSEncryptionKey|This command restores encryption key on to the SQL Server Reporting Services.|
|Revoke-AccessOnCatalogItem|This command revokes access on catalog item from users or groups.|
|Revoke-AccessToRS|This command revokes access on SQL Server Reporting Services from users or groups.|
|Set-RSEmailSettingsAsBasicAuth|This command configures the SQL Server Reporting Services email settings to use basic authentication.|
|Set-RSEmailSettingsAsNoAuth|This command configures the SQL Server Reporting Services email settings to use no authentication.|
|Set-RSEmailSettingsAsNTLMAuth|This command configures the SQL Server Reporting Services email settings to use NTLM authentication.|

## SQL Server Versions

Some of the commands listed above allow you to optionally specify the version of your SQL Server Reporting Services instance. The following is a list of versions associated to each SQL Server Reporting Services release.

|SQL Server Release|Version|
|------------------|-------|
|SQL Server 2012|11|
|SQL Server 2014|12|
|SQL Server 2016|13|

## Motivation

The motivation behind this project was to help users perform SQL Server Reporting Services operations via the command line. 

## API Reference

All of the APIs used by this project are publicly available. There are 2 types of APIs used in this repository: SOAP and WMI. You can find more details about the SOAP API at https://msdn.microsoft.com/en-us/library/ms154052.aspx and the WMI API at https://msdn.microsoft.com/en-us/library/ms152836.aspx. In general, you will use SOAP API for operations you would perform using Report Server and Web Portal whereas you will use WMI API for operations you would perform using Reporting Services Configuration Manager. 

## Code of Conduct

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
