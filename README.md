# systemd-units
A collection of systemd unit files.

## Setup
```shell
cd systemd-units
sudo systemctl link $PWD/lib/systemd/system/*
systemctl --user link $PWD/lib/systemd/user/*
systemctl --user link $PWD/lib/systemd/user/observer/*
# I feel like they don't necessarily have to reboot automatically here because cron does that. On the contrary, automatic reboots have the side effect that some of them delete the changes in the repository.
# systemctl --user enable $PWD/lib/systemd/user/observer/*
sudo systemctl daemon-reload
systemctl --user daemon-reload
sudo ln -s $PWD/etc/systemd/timesyncd.conf.d /etc/systemd
sudo ln -s $PWD/etc/systemd/system.conf.d /etc/systemd
```

Note that the above commands should be executed every time a new file is added. Do not forget to enable new services if you need to.

## Check systemd configuration
```shell
systemd-analyze cat-config systemd/system.conf
systemd-analyze cat-config systemd/timesyncd.conf
```
