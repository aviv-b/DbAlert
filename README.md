# DbAlert
Alerts Tool for DBA to monitor databases.

## Files
- AppSettings.json
- Log.txt 


## Log settings
- maxDays - The log file will deleted after X days. 
- maxMBSize - The log file will deleted after reaching X mb size.

## Alert settings
- name - The log file will deleted after X days. 
- odbcConnString - odbc string connection. Read more: https://www.connectionstrings.com/ 
							* recommendation: 
								 - Use windows odbc connection. 
								 - Use sql read only user authtication.
- queryCondition  - Sql query condition for alert. 
- triggerValue - An string value comparred against queryCondition result if they equals Alert message will send.
- alertMessage - The Alert Message. 
- active  - Enable / Disable the alert operation 
			- true  
			- false
- mails  - List of repcients mail boxes.

## SMTP settings
- server 
- address 
- port 
- username
- password 
- active 

## Exchange settings



# Language
- C# .net freamwork 4.7.2
