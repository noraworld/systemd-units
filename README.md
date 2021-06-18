# systemd-units
A collection of systemd unit files.

## Setup
```shell
sudo systemctl link $PWD/lib/systemd/system/*
sudo systemctl link $PWD/lib/systemd/user/*
sudo systemctl daemon-reload
systemctl --user daemon-reload
```
