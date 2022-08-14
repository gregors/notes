# Tcpdump

## filter out ICMP
 -i interface
 -X show hexdump

echo=reply
```shell
sudo  tcpdump -i eth0 -X “icmp[0] == 0”
```

echo-request
```shell
sudo  tcpdump -i eth0 -X "icmp[0] == 8"
```

## ICMP

0 Echo Reply
3 Destination Unreachable
4 Source Quench
5 Redirect
8 Echo
11 Time Exceeded

