# pptp-note

server:

https://help.ubuntu.com/community/PPTPServer
sudo apt-get install pptpd
 /etc/pptpd.conf
localip 192.168.0.1
remoteip 192.168.0.100-200

 /etc/ppp/chap-secrets
# client        server  secret                  IP addresses
username * myPassword *
 
client:

pptpsetup --create vpn --server ** --username ** --password ** --encrypt --start

 centos
  modprobe nf_conntrack_pptp
  modprobe nf_conntrack_proto_gre


troubleshooting:
if MS-CHAPv2 mutual authentication failed.
connect using windows client once, then linux can connect
