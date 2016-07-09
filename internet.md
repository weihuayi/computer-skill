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



