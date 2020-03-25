### Cron Note
===================

#### Global Cron File
**Path:** `/etc/crontab` **Format**
```
Example of job definition:
.---------------- minute (0 - 59)
|  .------------- hour (0 - 23)
|  |  .---------- day of month (1 - 31)
|  |  |  .------- month (1 - 12) OR jan,feb,mar,apr ...
|  |  |  |  .---- day of week (0 - 6) (Sunday=0 or 7) OR sun,mon,tue,wed,thu,fri,sat
|  |  |  |  |
*  *  *  *  * user-name command to be executed
```
#### User Cron File
**Path:** `/var/spool/cron/{USERNAME}` **Format**
```
Example of job definition:
.---------------- minute (0 - 59)
|  .------------- hour (0 - 23)
|  |  .---------- day of month (1 - 31)
|  |  |  .------- month (1 - 12) OR jan,feb,mar,apr ...
|  |  |  |  .---- day of week (0 - 6) (Sunday=0 or 7) OR sun,mon,tue,wed,thu,fri,sat
|  |  |  |  |
*  *  *  *  * command to be executed
```

#### Switch Use In Shell Script
**Run one command:** `su - oracle -c command`
**Run a script file:** `su - oracle -s /bin/bash shell.sh`

#### Replace content in file
sed -i 's/abc/xxx/g' file
or
sed -i 's?abc?xxx?g' file
or 
sed -i "s/abc/xxx/g" file

#### Delete line in file
sed -i '/aaa/d' tmp.txt
or
sed -i '/.*patch.*/d' zhanhao


