# systemd-units
A collection of systemd unit files.

## Setup
```shell
$ sudo ln -s /path/to/systemd-units/lib/systemd/system/* /lib/systemd/system
$ sudo ln -s /path/to/systemd-units/lib/systemd/user/*   /lib/systemd/user
$ sudo systemctl daemon-reload
$ systemctl --user daemon-reload
```
