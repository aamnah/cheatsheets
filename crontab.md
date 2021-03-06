

**List crontab entries** 
`` crontab -l ``

**Edit crontab** 
`` crontab -e ``

**Edit root user’s crontab** 
`` sudo crontab -e ``

**Delete crontab** 
`` crontab -r ``

**Confirm and delete crontab** 
`` crontab -i ``


Format
---

| minute | hour | day of month | month | day of week |
|---|---|---|---|---|
| 0-59 | 0-23 | 1-31 | 1-12 (or names) | 0-7 (0 or 7 is Sun, or use names) |

A field may be an **asterisk** ( * ), which always stands for "first through last".

**Ranges** of numbers are allowed. Ranges are two numbers separated with a hyphen. The specified range is inclusive; for example, **8-11** for an "hours" entry specifies execution at hours 8, 9, 10 and 11.

**Lists** are allowed. A list is a set of numbers (or ranges) separated by commas. Examples: "**1,2,5,9**", "**0-4,8-12**".

**Names** are allowed. **Mon, Sun, Sat** and such for days and **Jun, Apr, Jan** and such for months.

Examples
---
```5 0 * * *``` = Daily at 12:05am  
```0 5 * * *``` = Daily at 5am  
```15 14 1 * *``` = Run at 2:15pm on the first of every month  
```0 22 * * 1-5``` = Run at 10pm on weekdays  
```5 4 * * sun``` = Run at 5 after 4 every Sunday  
```23 0-23/2 * * *``` = Run 23 mins after midnight, 2am, 4am, ... everyday.  

####Backup all databases in gzip file daily at 12am.
```0 0 * * * mysqldump -u username -p -–all-databases | gzip > file.sql.gz```

####Sync /home/usr to Amazon S3 via s3cmd every Sunday at 3am.
```0 3 * * sun s3cmd -r sync /home/user s3://bucket/location```


Notes
---
- For the commands that require **sudo** to run, adding them to a regular user's crontab would be a problem (because of having to enter the password for them to run). In cases like these, you can add the commands to the root user's crontab so it'd already have sudo status.

---
**Source:** [List / Display all cron jobs](http://www.cyberciti.biz/faq/linux-show-what-cron-jobs-are-setup/), [Crontab usage](http://www.computerhope.com/unix/ucrontab.htm)