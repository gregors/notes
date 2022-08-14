# Tcpdump

## filter out ICMP
 -i interface
 -X show hexdump

```shell
sudo  tcpdump -i eth0 -X "icmp[0] == 8"
```
