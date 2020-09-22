# AutoScanner
- 1.Install ipset
- 2.Creat a new banlist
## ipset create banlist (name) hash:net
- 3.Drop connection
## iptables -I INPUT -m set --match-set banlist src -p tcp --destination-port 80 -j DROP
## iptables -I INPUT -m set --match-set banlist src -p tcp --destination-port 443 -j DROP

- 4.run this python code automatically
## crontab -u root -e
## */1 * * * * python3 /xxxx.py
