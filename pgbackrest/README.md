Zabbix Monitoring of pgbackrest via 'pgbackrest info --output=json' 

automatic triggers on general pgbackrest status

automatic trigger and items on repositories and backups

will monitor database and repo sizes and relevant metadata


To activate you need to add the following line to your zabbix_agent/agent2 config file or config directory
```
UserParameter=pgbackrest.info.get, /usr/bin/pgbackrest info --output=json
```

you also need to give zabbix permissions to run the pgbackrest command, usually via
```
# usermod -a -G postgres zabbix
```
