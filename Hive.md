# Learning-BigData

1. Download apache-hive-x.y.z-bin.tar.gz file.
2. Set environment variable. change .bashrc file for permanent change
    export HIVE_HOME=~/sw/apache-hive-x.y.z-bin
    export PATH=$PATH:$HIVE_HOME/bin
3. Type hive in command line , opens the hive hive shell.
4. By default hive reads from local file system.

Commands: (commands are case insensitive)

a. show TABLES;
b. CREATE TABLE records (year STRING, temperature INT, quality INT)
    ROW FORMAT DELIMITED
    FIELDS TERMINATED BY '\t'; 
    (Hive expects there to be three fields in each row, corresponding to the table columns, with fields 
     separated by tabs and rows by newlines)
c. LOAD DATA LOCAL INPATH 'input/ncdc/micro-tab/sample.txt'
    OVERWRITE INTO TABLE records;
d. hive> select * from records;
    OK
    1950	0	1
    1950	22	1
    1950	-11	1
    1949	111	1
    1949	78	1
    (Hive transforms this query into a job, which it executes on our behalf, then prints the results to the console.)


    
