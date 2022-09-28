# These playbooks allow you to configure a VPS in a secure way by adding the following tools:
- UFW firewall
- Iptables
- Mail notification 
- Logwatch
- Slack notifications
- Fail2Ban
- Portsentry
- RKhunter
- Open VPN
- ClamAV
- SSH config
- Ipv6 settings 

# Prerequisites
Adapt the vars/default.yml file to your case
# Invenyory
[infra]

xxx.xxx.xxx.xxxx
# Use playbook
- ansible-playbook  setup_vps.yaml -e "host=infra"

