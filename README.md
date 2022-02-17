# DbAlert
- Alerts Scheduler Tool for DBA to monitor databases.
- Create alert by given custom sql query. 
- Json and local files configuration.
- Build in logger.
- Sending alerts to mail address: SMTP , Exchange server.
- Supporting all databases via odbc connection. For more information see 'OdbcConnString' section below.		

## Important Files
- AppSettings.json - Settings file.
- Log.txt - Log file.


## Log settings
- MaxDays - The log file will deleted after X days. 
- MaxMBSize - The log file will deleted after reaching X mb size.

## Alert settings
- Name 
- OdbcConnString -  ODBC string connection. Read more: https://www.connectionstrings.com/ 
- 
		   Note: Sql server supported via odbc connection by defualt.
		   For MySql / Infromix / Sqllite  etc,  Please download relevent odbc driver.  
		   
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
- Password  
- Active 


## Fix Problems: 
- Mail in gibrish - make sure 'appSettings.json' file encoding in uft8.
- Any other issues will saved on 'log.txt'.

## Recommendation
- Create sql user with limited access for read only authentication.
- Create mail box spesific for alerts only.

## Language
- C# .net freamwork 4.7.2
