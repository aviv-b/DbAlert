# DbAlert
- Alerts Scheduler Tool for DBA to monitor databases.
- Create custom alerts by given custom sql query. 
- Local files configuration.
- Build in logger.
- Sending alerts into mail address. Supporting:  Smtp & Exchange server.
- Supporting all rdbms databases via odbc connection. For more information see 'OdbcConnString' section below.		

## Important files
- AppSettings.json - Settings file.
- Log.txt - Log file.


## Log settings
- MaxDays - The log file will deleted after X days. 
- MaxMBSize - The log file will deleted after reaching X mb size.

## Alert settings
- Name 
- OdbcConnString -  ODBC string connection. Read more: https://www.connectionstrings.com/ 
 
		   Notes: 
		   - Sql server is supported by default.
		   - MySql / IBM Informix / Sqlite etc,  Please download relevant odbc driver.  
		   
- QueryCondition  - Sql query condition for alert. 
- TriggerValue - An string value compared against 'queryCondition' result if they equals then alert message will be send.
- AlertMessage - The Alert Message. 
- Active  - Enable or Disable the alert operation. 
- Mails  - List of repcients mail address.

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


## Known issues 
- Mail in gibrish - make sure 'appSettings.json' file encoding in uft8.
- Any other issues will saved on 'log.txt'.

## Recommendation
- Create sql user with limited access for read only authentication.
- Create mail address spesific for alerts only.

## Language
- C# .net freamwork 4.7.2

## Os
- Windows 7 and above.
- Windows server R2 2008 and above.

