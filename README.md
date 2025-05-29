# Sing-box
#添加定时更新,和重启更新
(crontab -l 2>/dev/null; echo "0 2 * * * /root/tun_debian.sh"; echo "@reboot /root/tun_debian.sh") | crontab -
#查看
crontab -l
#删除定时
crontab -l | grep -v "tun_debian" | crontab -
#注意：如果你的后端没有科学环境，规则地址前记得添加镜像否则无法拉取。   例如：  
https://ghp.ci/https://raw.githubusercontent.com/qichiyuhub/rule/refs/heads/main/config/singbox/config_tproxy.json
