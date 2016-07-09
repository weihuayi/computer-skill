# `mentohust` autostart


1. Open `/etc/rc.local`
```
sudo vim /etc/rc.local
```

2. Add the following lines before the `exit 0` line:

```
if [ -x /usr/bin/mentohust ]; then
/usr/bin/mentohust
fi
```

# Redirect the website address in system level


# Wifi 的重新启动

```
$ sudo ifconfig wlp9s0
$ sudo service network-manager restart
```



