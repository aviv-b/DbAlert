# DbAlert
- Scheduler tool for DBA's to create alerts and monitor databases.
- Create custom alerts by given custom sql query. 
- Local files configuration.
- Build in logger.
- Sending email on alerts. Supporting Smtp & Exchange server.
- Supporting all rdbms databases with odbc connection. For more information see 'OdbcConnString' section below.		

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
- TriggerValue - An string value compared against 'queryCondition' result if they equals then alert message will send.
- AlertMessage - The alert message. 
- Active  - Enable or disable the alert operation. 
- Mails  - List of recipients email addresses.

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
- Mail in gibrish - Make sure 'appSettings.json' file encoding is uft8.
- Any other issues will saved on 'log.txt' file.

## Recommendation
- Create sql user with limited access for read only authentication.
- Create mail address spesific for alerts only.

## Written
- .net framework 4.7.2

## OS
- Windows 7 and above.
- Windows server 2008 R2 and above.

