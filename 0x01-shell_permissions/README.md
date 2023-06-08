### 0-My name is Betty
Switch the current user to the user betty using **su** command.

### 1-Who am I
Print the effective username of the current user **whoami**

### 2-Groups
Print all the groups the current user is part of using command **id -Gn**

### 3-New owner
Change the owner of the file *hello* to the user *betty* using command **chown betty hello**

### 4-Empty!
Creating an empty file *hello* with the help of the command **touch**

### 5-Execute
Adds execute permission to the owner of the file hello, we use **chmod 700 hello**

### 6-Multiple permissions
Adds execute permission to the owner and the group owner, and read permission to other users, to the file hello, we use **chmod 754 hello**, 7 for execute, 5 for read and execute and 4 for read

### 7-Everybody
Adds execution permission to the owner, the group owner and the other users, **chmod 751 hell0**

### 8-James Bond
Sets the permission to the file *hello* as follows:
-Owner: no permission at all
-Group: no permission at all
-Other: all the permissions

### 9-John Doe
Sets the mode of the file *hello* to this: **-rwxr-x-wx**

### 10-Look in the mirror
Set the mode of the file *hello* the same as *olleh* mode.
```bash
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 42 Sep 20 14:45 10-mirror_permissions
-rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello
-rw-rw-r-- 1 julien julien  0 Sep 20 14:43 olleh
julien@ubuntu:/tmp/h$ ./10-mirror_permissions 
julien@ubuntu:/tmp/h$ ls -l
total 8
-rwxrw-r-- 1 julien julien 42 Sep 20 14:45 10-mirror_permissions
-rw-rw-r-- 1 julien julien 23 Sep 20 14:25 hello
-rw-rw-r-- 1 julien julien  0 Sep 20 14:43 olleh
julien@ubuntu:/tmp/h$ 
```

### 11-Directories
Adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users.
Regular files should not be changed.
```bash
julien@ubuntu:/tmp/h$ ls -l
total 20
-rwxrwxr-x 1 julien julien   24 Sep 20 14:53 11-directories_permissions
drwx------ 2 julien julien 4096 Sep 20 14:49 dir0
drwx------ 2 julien julien 4096 Sep 20 14:49 dir1
drwx------ 2 julien julien 4096 Sep 20 14:49 dir2
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$ ./11-directories_permissions 
julien@ubuntu:/tmp/h$ ls -l
total 20
-rwxrwxr-x 1 julien julien   24 Sep 20 14:53 11-directories_permissions
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir0
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir1
drwx--x--x 2 julien julien 4096 Sep 20 14:49 dir2
-rw-rw-r-- 1 julien julien   23 Sep 20 14:25 hello
julien@ubuntu:/tmp/h$
```

