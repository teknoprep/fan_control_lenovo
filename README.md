# fan_control_lenovo
Lenovo Fan Control for ipmitool on SR655 v3

Should work on other servers



## service setup
root@vm241:/etc/systemd/system# cat cpu_temp_monitor.service 

[Unit]
Description=CPU Temperature Monitor Service
After=network.target

[Service]
Type=simple
ExecStart=/usr/local/bin/cpu_temp_monitor.py
Restart=always
User=root

[Install]
WantedBy=multi-user.target
