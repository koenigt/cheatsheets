# Case sensitive search

```
find /datafs/opt/IBM/ -name "*.jar"
```

# Case insensitive search

```
find /datafs/opt/IBM/ -iname "*.jar"
```

# find files older (lastmodified) than 90 days

```
find /datafs/opt/IBM/WebSphere/Profiles/base/logs/sqms* -name "*.log" -type f -mtime +90
```

# find files older (lastmodified) than 90 days dedicated formatting

```
find /datafs/opt/IBM/WebSphere/Profiles/base/logs/sqms* -name "*.log" -type f -mtime +90 -printf "%t\t %p \n"
```

# find files older (lastmodified) than 90 days and delete

```
find /datafs/opt/IBM/WebSphere/Profiles/base/logs/sqms* -name "*.log" -type f -mtime +90 -delete
```
see
- https://www.linode.com/docs/tools-reference/tools/find-files-in-linux-using-the-command-line/
- https://www.computerhope.com/unix/ufind.htm
