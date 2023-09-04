# blendos
常用设置

- /etc/systemd/system/fix-touchpad.service

····
[Unit]
Description=Restart psmouse module after suspend
After=suspend.target

[Service]
Type=oneshot
ExecStart=/bin/bash -c 'modprobe -r psmouse; modprobe psmouse'

[Install]
WantedBy=suspend.target
····


