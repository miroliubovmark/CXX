This is md file

Create folder_max and folder_min

```bash
$ cd /usr/local
$ mkdir folder_max folder_min
```

Create users
```bash
$ useradd user_max_1
$ useradd user_min_2
```

Create groups

```bash
$ groupadd group_max
$ groupadd group_min
```

Add users to groups and check

```bash
$ usermod -a -G group_max user_max_1
$ usermod -a -G group_min user_min_1

$ members group_max
user_max_1
$ members group_min
user_min_1
```


Для пользователей из группы *_max дать полный доступ на директории *_max и *_min. Для пользователей группы *_min дать полный доступ только на директорию *_min

```bash
$ chmod a=rwx folder_min
$ chmod o-w folder_max
$ chmod o-w folder_max
```


Create script

```bash
date | tee output.log
```

Check

```bash
$ cat date 
date | tee output.log
```




2. Docker

Create Dockerfile

```bash
FROM ubuntu:18.04

RUN echo "INIT"
RUN apt update
RUN apt install nano

ADD date .
```


Create iso file

```bash
$ docker build -t myubuntu .
```

Run myubuntu

```bash
$ sudo docker run -it myubuntu
[sudo] password for mark: 
root@e3c72ccb6b43:/# ./date
Fri Mar 17 22:23:18 UTC 2023
root@e3c72ccb6b43:/# 
```



3. Git

Clone repository from github

```bash
$ git clone 
```


