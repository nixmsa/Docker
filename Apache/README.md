<h1> Apache Docker Container</h1>
<pre>

mahsan@u22:~/Docker/Apache$ mysql -h 127.0.0.1 -u root -p -e "show variables like 'hostname';"
Enter password:
+---------------+--------------+
| Variable_name | Value        |
+---------------+--------------+
| hostname      | 7900d36b486d |
+---------------+--------------+
mahsan@u22:~/Docker/Apache$


mahsan@u22:~/Docker/Apache$ mysql -h 127.0.0.1 -u mahsan -p -e "show databases;"
Enter password:
+--------------------+
| Database           |
+--------------------+
| information_schema |
| msa_db             |
+--------------------+
mahsan@u22:~/Docker/Apache$

mahsan@u22:~/Docker/Apache$ docker-compose ps
    Name                  Command               State                    Ports
------------------------------------------------------------------------------------------------
apache_db_1    docker-entrypoint.sh mariadbd    Up      0.0.0.0:3306->3306/tcp,:::3306->3306/tcp
apache_web_1   /usr/sbin/apachectl -D FOR ...   Up      0.0.0.0:80->80/tcp,:::80->80/tcp
mahsan@u22:~/Docker/Apache$

mahsan@u22:~/Docker/Apache$ curl 127.0.0.1
All right reserved by 2022-2023 Muhammad Shahid Ahsan
mahsan@u22:~/Docker/Apache$


mahsan@u22:~/Docker/Apache$ docker-compose ps
    Name                  Command               State                    Ports
------------------------------------------------------------------------------------------------
apache_db_1    docker-entrypoint.sh mariadbd    Up      0.0.0.0:3306->3306/tcp,:::3306->3306/tcp
apache_web_1   /usr/sbin/apachectl -D FOR ...   Up      0.0.0.0:80->80/tcp,:::80->80/tcp
mahsan@u22:~/Docker/Apache$ docker-compose exec db /bin/bash
root@7900d36b486d:/#

mahsan@u22:~/Docker/Apache$ docker-compose stop
Stopping apache_web_1 ... done
Stopping apache_db_1  ... done
mahsan@u22:~/Docker/Apache$
mahsan@u22:~/Docker/Apache$ docker-compose up -d web
Starting apache_web_1 ... done
mahsan@u22:~/Docker/Apache$ docker-compose ps
    Name                  Command               State                 Ports
-----------------------------------------------------------------------------------------
apache_db_1    docker-entrypoint.sh mariadbd    Exit 0
apache_web_1   /usr/sbin/apachectl -D FOR ...   Up       0.0.0.0:80->80/tcp,:::80->80/tcp
mahsan@u22:~/Docker/Apache$ docker-compose rm
Going to remove apache_db_1
Are you sure? [yN] y
Removing apache_db_1 ... done
mahsan@u22:~/Docker/Apache$
</pre>
