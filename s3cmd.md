####installation:
`` apt-get install s3cmd -y ``

####configuration
`` s3cmd —configure ``  
enter the access key and security code for aws.

####list s3 buckets
`` s3cmd ls ``

####copy files to s3
`` s3cmd -r put /home/user s3://bucket/location ``  
-r is for copying dirs

####sync files to s3
`` s3cmd -r sync /home/user s3://bucket/location ``

####add s3cmd to crontab
`` crontab -e ``
and in the new screen add `` 0 5 * * * s3cmd -r sync /home/user s3://bucket/location `` to run the command daily at 5am.
ctrl+o to save, confirm save and ctrl+x to exit

OR  

`` echo '0 5 * * * s3cmd -r sync /home/user s3://bucket/location' >> crontab ``
to append the command at the end of the crontab.

###add s3cmd to root user’s crontab
`` sudo crontab -e ``  
will let you edit the root user’s crontab

Notes:
---
- **/home/user vs. /home/user/**  
/home/user means the ‘user’ directory and /home/user/ means ‘all files in the user dir’.
- the **-r** flag is for copying directories
