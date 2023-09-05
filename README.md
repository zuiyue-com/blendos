# blendos

## 常用设置
- /etc/systemd/system/fix-touchpad.service

````
[Unit]
Description=Restart psmouse module after suspend
After=suspend.target

[Service]
Type=oneshot
ExecStart=/bin/bash -c 'modprobe -r psmouse; modprobe psmouse'

[Install]
WantedBy=suspend.target
````

## todo 输入法

## Chrome

- wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
- sudo apt.u install ./google-chrome-stable_current_amd64.deb

## todo Clash

