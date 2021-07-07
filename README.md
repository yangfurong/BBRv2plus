# BBRv2+ prototype

*We note that this prototype has been tested in Ubuntu 18.04.5. For more detailed info about the testbed, please refer to our paper.*

### Compile BBRv2 alpha kernel

- Kernel:  https://github.com/google/bbr/tree/v2alpha
- Tag: v2alpha-2019-11-22
- Commit ID: 55105fea34f330062943c65d1dc85774f9fd532f
- Compiling instructions: https://github.com/google/bbr/blob/v2alpha/README.md
- Change ICSK_CA_PRIV_SIZE to 400 in /include/net/inet_connection_sock.h

### Compile BBRv2+

`make`

### Install BBRv2+

`sudo insmod tcp_bbr2plus.ko`

### Test BBRv2+

```
iperf -s -i1
iperf -c 127.0.0.1 -i1 -Z bbr2plus
```

### Change BBRv2+'s design parameters
```
cd /sys/module/tcp_bbr2plus/parameters

# change the values of files
```



