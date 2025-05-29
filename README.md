# Sing-box
#添加定时更新,和重启更新
(crontab -l 2>/dev/null; echo "0 2 * * * /root/tun_debian.sh"; echo "@reboot /root/tun_debian.sh") | crontab -
#查看
crontab -l
#删除定时
crontab -l | grep -v "tun_debian" | crontab -
