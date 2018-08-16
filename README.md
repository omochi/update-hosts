# Function

- Update `/etc/hosts` by erb.
- Restart dnsmasq if it is installed.

# Install

copy `update-hosts` to `/usr/local/bin`.

# How to use

1. Write template at `/etc/hosts.erb`

```
##
# Host Database
#
# localhost is used to configure the loopback interface
# when the system is booting.  Do not change this entry.
##
127.0.0.1	localhost
255.255.255.255	broadcasthost
::1             localhost

<%= ip_address %> api-hogehoge.localdomain
<%= ip_address %> cms-hogehoge.localdomain
<%= ip_address %> res-hogehoge.localdomain
```

2. Run

```
$ sudo update-hosts
```

# Template

There variables are defined.

```
ip_address
```
