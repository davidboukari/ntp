# ntp

* https://thebackroomtech.com/2019/01/17/configure-centos-to-sync-with-ntp-time-servers/
```

# yum install ntp ntpdate

If yum is not installed, just run the following command: sudo apt install yum. Once that’s installed we need to start and enable the ntpd service.

# systemctl start ntpd

# systemctl enable ntpd

# systemctl status ntpd

Now that that’s out of the way let’s run the following command to configure the NTP Servers.

# ntpdate -u -s 0.centos.pool.ntp.org 1.centos.pool.ntp.org 2.centos.pool.ntp.org

What we’re doing is telling the ntpdate to use an unprivileged port for outgoing packets with the -u switch and to write logging output to the system syslog facility using the -s switch.

# systemctl restart ntpd

```
