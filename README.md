# systemd-units
A collection of systemd unit files.

## Setup
```shell
cd systemd-units
sudo systemctl link $PWD/lib/systemd/system/*
systemctl --user link $PWD/lib/systemd/user/*
sudo systemctl daemon-reload
systemctl --user daemon-reload
```

Note that the above commands should be executed every time a new file is added.
