MySQL Backups
---

#### backup all databases in one file (eventually add the option --add-locks):
```mysqldump -u username -p -–all-databases > file.sql```

#### backup all databases in one gzipped file:
```mysqldump -u username -p -–all-databases | gzip > file.sql.gz```

#### restore all databases:
```mysql -u username -p < file.sql ```
