```shell
sudo ln -s $(pwd)/noraworld /etc/sysconfig
sudo ln -s $(pwd)/diary.service /etc/systemd/system
sudo ln -s $(pwd)/mastodon-*.service /etc/systemd/system
sudo systemctl daemon-reload
```
