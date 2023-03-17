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
