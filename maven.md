# update versions of a selected artifact
```
mvn versions:use-latest-versions -Dincludes=group.msg.playground:* -DallowMajorUpdates=true
````

# set versions of a module (run on the parent to update all modules too)
```
mvn versions:set -DnewVersion=2.50.1-SNAPSHOT
```

# Checking for new dependency updates
```
mvn versions:display-dependency-updates
```