https://hub.docker.com/r/dragonbest520/oracle-xe-10g
docker pull dragonbest520/oracle-xe-10g
docker run --name oracle10g -d -p 49160:22 -p 1521:1521 -p 49162:8080  --mount source=oracle_xe_10g_vol,target=/usr/lib/oracle -e ORACLE_ALLOW_REMOTE=true   --restart=always dragonbest520/oracle-xe-10g

hostname: localhost
port: 1521
sid: xe
username: system
password: oracle

sqlplus system/oracle@localhost:1521/xe

ssh root@localhost -p 49160
password: admin

http://localhost:49162/apex
