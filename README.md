# coolweather

A customized weather app with a widget.

建立三张表，Province、City、County，分别
用于存放省、市、县的各种数据信息，三张表的建表语句分别如下。

Province：
create table Province (
id integer primary key autoincrement,
province_name text,
province_code text)
其中 id 是自增长主键，province_name 表示省名，province_code 表示省级代号。


City：
create table City (
id integer primary key autoincrement,
city_name text,
city_code text,
province_id integer)
其中 id 是自增长主键，city_name 表示城市名，city_code 表示市级代号，province_id 是
City 表关联 Province 表的外键。


County：
create table County (
id integer primary key autoincrement,
county_name text,
county_code text,
city_id integer)
其中 id 是自增长主键，county_name 表示县名，county_code 表示县级代号，city_id 是
County 表关联 City 表的外键。
