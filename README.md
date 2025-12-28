```
bash <(curl -fsSL https://raw.githubusercontent.com/wibusantun/zivpn/main/zivpn.sh)
```
```
bash <(curl -fsSL https://raw.githubusercontent.com/wibusantun/zivpn/main/uninstall.sh)
```
```
edit bagian before.rules di etc/ufw
*nat
:PREROUTING ACCEPT [0:0]

-A PREROUTING -p udp --dport 6000:19999 -j DNAT --to-destination :5667

COMMIT
```
