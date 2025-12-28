```
bash <(curl -fsSL https://raw.githubusercontent.com/wibusantun/zivpn/main/zivpn.sh)
```
```
bash <(curl -fsSL https://raw.githubusercontent.com/wibusantun/zivpn/main/uninstall.sh)
```
supaya ufw berhasil edit before.rules di etc/ufw
lihat bagian ini saja ada ruang kosong
#
# rules.before
#
# Rules that should be run before the ufw command line added rules. Custom
# rules should be added to one of these chains:
#   ufw-before-input
#   ufw-before-output
#   ufw-before-forward
# edit seperti dibawah
*nat
:PREROUTING ACCEPT [0:0]

-A PREROUTING -p udp --dport 6000:19999 -j DNAT --to-destination :5667

COMMIT
# Don't delete these required lines, otherwise there will be errors
dan selanjutnya bla bla
```
