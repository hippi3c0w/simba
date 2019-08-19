![](images/simba.png)

# simba
Simba is a free tool that can be used to make server monitoring as an usual sysadmin task. In order to make it easier, we have compiled in only one program, the basics commands to do server monitoring such as:
- Check /var/run/[service]/[service].pid 
- Check status of a service via /etc/init.d
- Check files via tree command
- Fail2ban (must be installed and configured into the server
- Check suid binaries via find
- Use top command

The usage of this software is.
- s: Shows you info about a service. You must specify the service name
- f: Shows you info about the files created or modified in each home directory. You can specify whatever you want
- b: Shows you info about banned IPs via Fail2ban service (you must have installed and configure it). You must choos 'ban' or 'unban'
- u: Shows you info about unwanted SUID or SGID binaries. You can specify whatever.
- h: Shows you info about how to use simba software
- t: Shows you info about top command. You must specify top status (running, sleeping, zombie or all).
Examples:
```simba -t running
   simba -t sleeping
   simba -t zombie
   simba -t all
```

Another examples
```
simba -s apache2 -f home -b ban
simba -b unban -t running -u suid -s apache2
```
# Features
- Check /var/run/[service]/[service].pid 
- Check status of a service via /etc/init.d
- Check files via tree command
- Fail2ban (must be installed and configured into the server
- Check suid binaries via find
- Use top command

# Install

```git clone https://github.com/hippi3c0w/simba.git
   cd simba
   cp -pv simba /usr/bin
   ```
Or you can use *partea* software

```
partera -u hippi3c0w -r simba
```
# Disclaimer
It only can be use in GNU/Linux distros


