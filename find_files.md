At Servers, we often need to find the files, **which are like 30 days old** and need to delete them. Generally logs are gigabytes in size, and at times, it really makes sense to delete the logs to relaim disk space. 

Off course, it goes without saying, as sys admins, those logs being deleted should not be deleted blindly, rather an archiving solution should be in place. 

Still, if it is really need of the time delete the 30 days old files, following command line fu should be implemented. 

```
ForFiles /p "C:\inetpub\logs\LogFiles\W3SVC2" /M *.log* /D -30 /C "cmd /c del /f /q @file"
```
The following are options to modify in this command
/p - give the path to where the operations need to be done.  We could give the IIS Folder, or any other tolder here.
/M is the wild card to select files which needs to be performed action on. In the above command, it was log in extension.
/D gives the day range. Further complex Dates could be changed and read using **ForFiles /?**
/C is the command to run the operation. @file is variable which is used to delete the file. 
 
You can always check for reading the help files of MS DOS
