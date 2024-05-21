##### List the all DB's #####

    \l

#### Create a DB ####

    create database demodb;

#### Checkout to created database ####

    \c demodb

#### Delete DB ####

    drop database demodb;

#### Check list of tables ####

    step1: login to db => \c demodb
    \d

#### Create a table ####

    create table student(id int,name text,age int,address text);
    (or)
    create table station(
	st_id integer,
	st_name varchar(200),
	st_state varchar(200),
	st_city varchar(20)
    );

#### Delete a table ####

    single: drop table <tablename>; 
    multiple: drop table<tablename>,<tablename>;

#### Alter table ####
    Notes: 
    alter means modification of table we can rename or add colums on table
    step1: create a sample table on testdb

    create table station(
	st_id integer,
	st_name varchar(200),
	st_state varchar(200),
	st_city varchar(20)
    );

    step2: altering adding the another column in table

    alter table station
    add column latitude real;

    task2: drop table using alter let say i have 5 cloumns i do want drop one column

    alter table station
    drop column latitude;

    task3: rename columns
        alter table station
        rename column st_state to state_name;

    task4: rename tablename
        alter table station
        rename to new_station;