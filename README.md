# DbAlert
Alerts Tool for DBA to monitor databases.

## Important Files
- AppSettings.json - Settings file.
- Log.txt - Log file.


## Log settings
- MaxDays - The log file will deleted after X days. 
- MaxMBSize - The log file will deleted after reaching X mb size.

## Alert settings
- Name - The log file will deleted after X days. 
- OdbcConnString - odbc string connection. Read more: https://www.connectionstrings.com/ 
							* recommendation: 
								 - Use windows odbc connection. 
								 - Use sql read only user authentication.
- QueryCondition  - Sql query condition for alert. 
- TriggerValue - An string value comparred against queryCondition result if they equals Alert message will send.
- AlertMessage - The Alert Message. 
- Active  - Enable / Disable the alert operation. 
- Mails  - List of repcients mail boxes.

## SMTP settings
- Server 
- Address 
- Port 
- Username
- Password 
- Active 

## Exchange settings
- Server 
- Address 
- Username
- Password  - * recommand creating mail account spesific for alerts only !! 
- Active 


## Fix Problems: 
- Mail in gibrish - make sure 'appSettings.json' file encoding in uft8.
- Any other issues will saved on 'log.txt'.


# Language
- C# .net freamwork 4.7.2
