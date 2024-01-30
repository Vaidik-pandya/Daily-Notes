Daily Notes : Day 98
Apk pentesting - Part 7

SQLite DBs;
Most of the applications will use internal SQLite databases to save information. During the pentest take a look to the databases created, the names of tables and columns and all the data saved because you could find sensitive information (which would be a vulnerability).
Databases should be located in /data/data/the.package.name/databases like /data/data/com.mwr.example.sieve/databases
If the database is saving confidential information and is encrypted but you can find the password inside the application it's still a vulnerability.
Enumerate the tables using .tables and enumerate the columns of the tables doing .schema <table_name>

 Drozer (Exploit Activities, Content Providers and Services):
Drozer allows you to assume the role of an Android app and interact with other apps. It can do anything that an installed application can do, such as make use of Android’s Inter-Process Communication (IPC) mechanism and interact with the underlying operating system. From Drozer Guide.
Drozer is s useful tool to exploit exported activities, exported services and Content Providers as you will learn in the following sections.