### SQLite3

Another important point is where are we going to storage the data we will receive from the Raspberry. There are a lot of options, and of course we will receive a service that we can consume (web server), so we can retrieve or post/get any information in the cloud. At this moment, we will introduce a lite database called SQLite3. The first time will be to check if it is already installed in your distribution.

```bash
$ sqlite3 -–version
> 3.7.13 2012-07-17 17:46:21 65035912264e3acbced5a3b 
```

If SQLite3 is not installed, run the next command:

```bash
$ sudo apt-get install sqlite3
```

#### Creating a DB

The first step will be to create the schema of the DB, which basically means what columns (and their types we will have) and put some data in it. Let’s do that.

```bash
$ cd /home/pi/testDir/ 
$ nano temperature.sql
create table temp (temp int, timest varchar(12));
insert into temp values (9, '2013-11-15 14:03:17');
insert into temp values (8, '2013-11-16 14:03:17');
insert into temp values (7, '2013-11-17 14:03:17'); 
insert into temp values (7, '2013-11-18 14:03:17'); 
insert into temp values (8, '2013-11-19 14:03:17'); 
insert into temp values (9, '2013-11-20 14:03:17'); 
insert into temp values (7, '2013-11-21 14:03:17'); 
insert into temp values (8, '2013-11-22 14:03:17');
```

#The date should be a DateStamp field, but for this moment we will use a String.

At this moment we haven’t populated or created any database. However, we can use the file that we just created to do that.

```bash
$ sqlite3 temperature.db < temperature.sql
```

Now that the DB is created, we are able to use sqlite3 to retrieve the information contained on the DB.
Making queries to the DB

```bash
$ sqlite3 temperature.db 
sqlite> .head on
sqlite> .mode column 
sqlite> select * from temp;
```

You can see the image of the process on the terminal.