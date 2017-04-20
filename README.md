## About

This package installs a NEM Infrastructure Server on your ubuntu system.
The service runs under user `nem`, and is controlled by systemd:

  * `systemctl start nem-nis` to start  
  * `systemctl status nem-nis` to check status
  * `systemctl stop nem-nis` to stop

Database and logs are in /var/lib/nem/nem/nis
config files are:

  *  /opt/nem/package/nis/config-user.properties : to be created by user
  * /opt/nem/package/nis/config.properties : default config. Should not be touched by user, but used as a reference for config-user.properties
  * /etc/default/nem-nis: for memory allocation


## Installation

As root:
```
echo "deb https://rb2nem.github.io/nem-nis-apt/ xenial main" > /etc/apt/sources.list.d/nem-nis.list
curl  https://rb2nem.github.io/nem-nis-apt/pub.key | apt-key add -
apt update
apt install nem-nis
```
