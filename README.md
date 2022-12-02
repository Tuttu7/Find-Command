#### -mtime is handy, for example, if we want to find all the files from the current directory that have changed in the last 24 hours:

```
[tuttu@fedora test]$ find . -mtime -1
.
./tr.txt
./testing


[tuttu@fedora test]$ find . -type f -mtime -1
./tr.txt

```

#### There are times when we want to find the files that were modified based on a particular date. In order to fulfill this requirement, we have to explore another parameter, which has the following syntax:

```
[tuttu@fedora test]$ find . -type f -newermt 2022-12-02
./tr.txt


[tuttu@fedora test]$ find . -type d -newermt 2022-12-02
.
./testing


[tuttu@fedora test]$ find . -type f -newermt "-24 hours"
./tr.txt
```
