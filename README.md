# My-project-file-code

mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| anirudh            |
| dbms               |
| information_schema |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
6 rows in set (0.04 sec)

mysql> use dbms
Database changed
mysql> show tables;
+----------------+
| Tables_in_dbms |
+----------------+
| admin          |
| businfo        |
| busschedule    |
| busstops       |
| routedetails   |
| ticketdetails  |
| usertable      |
+----------------+
7 rows in set (0.02 sec)

mysql> select * from admin;
+-----+------------+-------------+--------------+
| ID  | AgencyName | AgencyPhone | AgencyOffice |
+-----+------------+-------------+--------------+
| 111 | RTA        | 8009090     | Dubai        |
+-----+------------+-------------+--------------+
1 row in set (0.02 sec)

mysql> select * from businfo;
+-----------+------------+------------+------+---------------------+
| BusRegnNo | AgencyName | TotalSeats | AC   | LocationName        |
+-----------+------------+------------+------+---------------------+
| 13B       | RTA        |         55 |    1 | Gold Souq Bus stn   |
| 91A       | RTA        |         55 |    1 | Gold Souq Bus stn   |
| X02       | RTA        |         55 |    1 | Al Ghubaiba Bus stn |
| X13       | RTA        |         55 |    1 | LuLu Village        |
| X23       | RTA        |         55 |    1 | AL Karama Bus stn   |
| X92       | RTA        |         55 |    1 | AL Ghubaiba Bus stn |
| X92       | RTA        |         55 |    1 | AL Ghubaiba Bus stn |
+-----------+------------+------------+------+---------------------+
7 rows in set (0.01 sec)

mysql> select * from busschedule;
+-----------+---------+----------+-----------+------+---------------+------------+
| BusRegnNo | RouteID | DriverID | StartTime | Fare | ReservedSeats | TravelTime |
+-----------+---------+----------+-----------+------+---------------+------------+
| 13B       |    2341 |    52074 | 12:30     |   20 |            12 | 30min      |
| 91A       |    4576 |    30035 | 2:35      |   25 |             5 | 23min      |
| X02       |    1876 |    56734 | 12:40     |   20 |             2 | 35min      |
| X13       |    1234 |    34598 | 12:55     |   23 |             5 | 1hr 27min  |
| X22       |    4567 |    10939 | 1:00      |   20 |            13 | 55min      |
| X23       |    6794 |    20973 | 1:10      |   25 |             9 | 52min      |
| X92       |    2938 |    47392 | 1:15      |   23 |             4 | 2hr 24min  |
+-----------+---------+----------+-----------+------+---------------+------------+
7 rows in set (0.01 sec)

mysql> select * from busstops;
+---------+----------------------------+------------+
| RouteID | IntermediateStops          | StopNumber |
+---------+----------------------------+------------+
| D89     | Qusais                     | 1          |
| E11     | Al karama bus station      | 2          |
| D73     | Capital hotel              | 3          |
| D89     | Emirates Metro Bus Stop 2  | 4          |
| D62     | Al Ghubaiba Bus station 45 | 5          |
| F23     | Centrepoint Metro station  | 6          |
| G34     | Al Maktoum Intl Airport    | 7          |
+---------+----------------------------+------------+
7 rows in set (0.01 sec)

mysql> select * from routedetails;
+-----------+---------+---------------------+------------------------+-------------------------+
| BusRegnNo | RouteID | RouteName           | Source                 | Destination             |
+-----------+---------+---------------------+------------------------+-------------------------+
| 13B       |  D89    | Airport Road        | Gold Souq Bus stn      | Al Qusais Bus stn       |
| 91A       | E11     | Sheikh Zayed road   | Gold Souq Bus stn      | Jebel Ali Bus stn       |
| X02       | D73     | Al Mustaqbai street | Al Ghubaiba Bus Stn    | Al Satwa                |
| X13       | D89     | Al Maktoum road     | LuLu Village           | Al Satwa Bus Stn        |
| X22       | D62     | Beirut st           | Al Qusais Ind'l Area 2 | Buisness Bay MS         |
| X23       | F23     | Al Quds Road        | Al Karama Bus Stn      | Dubai Outsourcing       |
| X92       | D34     | Al Amal             | Al Ghubaiba Bus Stn    | Dubai investment Park 1 |
+-----------+---------+---------------------+------------------------+-------------------------+
7 rows in set (0.01 sec)

mysql> select * from ticketdetails;
+-----------+--------+----------------------------+
| BusRegnNo | SeatNo | Email                      |
+-----------+--------+----------------------------+
| 13B       |      3 | venugopal.komala@gmail.com |
| 13B       |      4 | Amrith.sus@gmail.com       |
| 13B       |      2 | sai.emani@gmail.com        |
+-----------+--------+----------------------------+
3 rows in set (0.01 sec)

mysql> select * from usertable;
+-------+---------+--------+----------------------------+-------------+-----------+----------+---------------------------+
| ID    | Name    | Gender | Email                      | Password    | Phone     | Usertype | Address                   |
+-------+---------+--------+----------------------------+-------------+-----------+----------+---------------------------+
| 11114 | Samson  | M      | samsonjoie@gmail.com       | 000b        | 506768906 | user     | home                      |
| 11115 | Anirudh | M      | anirudh.e23@gmail.com      | 00b         | 561879012 | user     | Carrefour                 |
| 11116 | aryan   | M      | aryan@gmail.com            | 0b          | 505674086 | user     | windows                   |
| 11117 | Sai     | M      | sai.emani@gmail.com        | Krishna$9$9 | 561879002 | user     | carrefour market          |
| 11118 | Venu    | M      | venugopal.komala@gmail.com | Govinda$9   | 507248906 | user     | Carrefour Market Building |
| 11121 | Komala  | F      | komala.emani@gmail.com     | Krishna9    | 505764086 | user     | office                    |
| 11122 | Amrith  | M      | Amrith.sus@gmail.com       | Amoung.us23 | 522953344 | user     | sushome                   |
+-------+---------+--------+----------------------------+-------------+-----------+----------+---------------------------+
7 rows in set (0.01 sec)

mysql> desc admin;
+--------------+-----------------+------+-----+---------+----------------+
| Field        | Type            | Null | Key | Default | Extra          |
+--------------+-----------------+------+-----+---------+----------------+
| ID           | bigint unsigned | NO   | PRI | NULL    | auto_increment |
| AgencyName   | varchar(35)     | NO   |     | NULL    |                |
| AgencyPhone  | varchar(10)     | YES  |     | NULL    |                |
| AgencyOffice | varchar(50)     | YES  |     | NULL    |                |
+--------------+-----------------+------+-----+---------+----------------+
4 rows in set (0.01 sec)

mysql> desc businfo;
+--------------+--------------+------+-----+---------+-------+
| Field        | Type         | Null | Key | Default | Extra |
+--------------+--------------+------+-----+---------+-------+
| BusRegnNo    | varchar(15)  | NO   |     | NULL    |       |
| AgencyName   | varchar(35)  | NO   |     | NULL    |       |
| TotalSeats   | int          | YES  |     | NULL    |       |
| AC           | decimal(1,0) | YES  |     | NULL    |       |
| LocationName | varchar(20)  | YES  |     | NULL    |       |
+--------------+--------------+------+-----+---------+-------+
5 rows in set (0.00 sec)

mysql> desc busschedule;
+---------------+--------------+------+-----+---------+-------+
| Field         | Type         | Null | Key | Default | Extra |
+---------------+--------------+------+-----+---------+-------+
| BusRegnNo     | varchar(15)  | NO   |     | NULL    |       |
| RouteID       | int          | YES  |     | NULL    |       |
| DriverID      | int          | YES  |     | NULL    |       |
| StartTime     | varchar(20)  | YES  |     | NULL    |       |
| Fare          | int          | YES  |     | NULL    |       |
| ReservedSeats | int          | YES  |     | NULL    |       |
| TravelTime    | varchar(100) | YES  |     | NULL    |       |
+---------------+--------------+------+-----+---------+-------+
7 rows in set (0.00 sec)

mysql> desc busstops;
+-------------------+--------------+------+-----+---------+-------+
| Field             | Type         | Null | Key | Default | Extra |
+-------------------+--------------+------+-----+---------+-------+
| RouteID           | varchar(100) | YES  |     | NULL    |       |
| IntermediateStops | varchar(100) | YES  |     | NULL    |       |
| StopNumber        | varchar(100) | YES  |     | NULL    |       |
+-------------------+--------------+------+-----+---------+-------+
3 rows in set (0.00 sec)

mysql> desc routedetails;
+-------------+--------------+------+-----+---------+-------+
| Field       | Type         | Null | Key | Default | Extra |
+-------------+--------------+------+-----+---------+-------+
| BusRegnNo   | varchar(100) | YES  |     | NULL    |       |
| RouteID     | varchar(100) | YES  |     | NULL    |       |
| RouteName   | varchar(100) | YES  |     | NULL    |       |
| Source      | varchar(100) | YES  |     | NULL    |       |
| Destination | varchar(100) | YES  |     | NULL    |       |
+-------------+--------------+------+-----+---------+-------+
5 rows in set (0.00 sec)

mysql> desc ticketdetails;
+-----------+--------------+------+-----+---------+-------+
| Field     | Type         | Null | Key | Default | Extra |
+-----------+--------------+------+-----+---------+-------+
| BusRegnNo | varchar(100) | YES  |     | NULL    |       |
| SeatNo    | int          | YES  |     | NULL    |       |
| Email     | varchar(100) | YES  |     | NULL    |       |
+-----------+--------------+------+-----+---------+-------+
3 rows in set (0.00 sec)

mysql> desc usertable;
+----------+-----------------+------+-----+---------+----------------+
| Field    | Type            | Null | Key | Default | Extra          |
+----------+-----------------+------+-----+---------+----------------+
| ID       | bigint unsigned | NO   | PRI | NULL    | auto_increment |
| Name     | varchar(30)     | YES  |     | NULL    |                |
| Gender   | varchar(7)      | YES  |     | NULL    |                |
| Email    | varchar(40)     | NO   | UNI | NULL    |                |
| Password | varchar(15)     | NO   |     | NULL    |                |
| Phone    | decimal(10,0)   | YES  |     | NULL    |                |
| Usertype | varchar(10)     | YES  |     | NULL    |                |
| Address  | varchar(100)    | YES  |     | NULL    |                |
+----------+-----------------+------+-----+---------+----------------+
8 rows in set (0.00 sec)
