Below events found in Application logs in Active Directory, filterd with __Event Sources: ESENT__ are found related to database changes in Windows 2019 Active Directory Servers

Event ID | Description
--- | ---
Event ID 216 | A database location change was detected
Event ID 325 | The database engine created a new database
Event ID 326 | The database enginer attached a database
Event ID 327 | The database enginer detached a database

# Indications
1. Multiple (~20) of the event of interest occuring at the same time
2. Event ID 325 with a logical file path (eg. C:\) instead of namepipe
3. There should more but needs to be tested


# Reference
https://www.youtube.com/watch?v=rioVumJB0Fo&list=WL&index=26
