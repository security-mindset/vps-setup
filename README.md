# These playbooks allow you to configure a VPS in a secure way by adding the following tools:
- UFW firewall
- Iptables
- Mail notification 
- Logwatch
- Fail2Ban with mail notification
- Portsentry
- RKhunter
- Open VPN
- ClamAV
- SSH config
- Ipv6 settings 

# Prerequisites
Adapt the vars/default.yml file to your case
# Inventory
[infra]

xxx.xxx.xxx.xxxx
# Use playbook
- sudo chmod 777 main.sh
- ./main.sh

  # Fail2Ban commands
- sudo fail2ban-client set nginx-http-auth unbanip 111.111.111.111 
- sudo fail2ban-client set nginx-http-auth banip 111.111.111.111
- service fail2ban status
  -  sudo systemctl restart fail2ban
- systemctl status fail2ban
  - fail2ban-client status
-  fail2ban-regex /var/log/nginx/error.log /etc/fail2ban/filter.d/{{item}}
  -  tail -f /var/log/fail2ban.log #fail2ban log analysis
  