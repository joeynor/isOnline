isOnline
========

Script for scheduled check of websites availability and reboot the machine. Suited for crontab job.
The idea is to help my machine to re-establish network and vpn connections.

## Config
1. Create ```emails.lst``` file and fill it with each email in new line (as in ```emails.lst.example```). leave an empty line in the end.
2. Create ```websites.lst``` file and fill it with each website in a new line (as in ```websites.lst.example```). leave an empty line in the end.

    Note that the script will follow url(s) with 301 (redirect). Config 1 is no longer a feature i need. So i comment it out, if you need it, uncomment
the section where it deals with the email 

## Add to crontab
Add the following lines to crontab config ($ crontab -e) 

```
THIS_IS_CRON=1
*/30 * * * * /path/to/isOnline/checker.sh
```

in this example crontab will run ```checker.sh``` every 30min.

by [ET][ET].
modified by [joeynor][joeynor]

[ET]: http://etcs.me
[joeynor]: http://rizal.mohdnor.name
