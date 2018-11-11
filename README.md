THE GOAL

Consolidate main MongoDB and system health metrics in one report.
Useful for routine daily and weekly MongoDB checks.

Report provides:
- Basic OS-level parameters: disk space, hostname,IP Address, Date & Time ,load average, memory utilization 
- Important MongoDB statistics : Instance Status , Uptime, MongoDB Connection detail,threads_connected,MongoDB Asserts Status,MongoDB Instance Database List

Regular asserts: these are as a result of an operation failure. For example in a schema if a string value is provided to an integer field hence resulting in failure reading the BSON document.
Warning asserts: these are often alerts on some issue but are not having much impact on its operation. For example when you upgrade your MongoDB you might be alerted using deprecated functions.
Msg asserts: they are as a result of internal server exceptions such as slow network or if the server is not active.
User asserts: like regular asserts, these errors arise when executing a command but they are often returned to the client. For example if there are duplicate keys, inadequate disk space or no access to write into the database. You will opt to check your application to fix these errors.
Rollovers asserts: The number of times that the rollover counters have rolled over since the last time the MongoDB process started

Report example: 
CONFIGURING AND RUNNING
1. Edit MongoDB credentials in mysqlhealthchecks.sh
2. Run ./mongodb-healthreport.sh
3. Enjoy!

Script will automatically send report to email address given in script.

Report will be emailed to you. Useful when running script via cron.

DOCUMENTATION
version 1.0
