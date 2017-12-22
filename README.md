# DNSCrpyt Magisk Module

Up to date NDK builds of DNSCrypt from https://github.com/jedisct1/dnscrypt-proxy

### To use

Install with Magisk or TWRP

Remove and set proxy from Access Point Names

The DNSCrypt proxy will start on boot binding to port 53

There is currently an issue with tethering.  Stop the proxy then tether works.


From shell on device: 

```bash
# get IP currently used resolver 
hostip -r 127.0.0.1 resolver.dnscrypt.org
​
# start DNSCrypt
dnscrypt enable 

# stop DNSCrypt 
dnscrypt disable 
```

To test visit https://www.dnsleaktest.com/ and do standard test.   

You must see one and only one DNSCrypt resolver and it must have the same IP as from the hostip command above. 

### To Do

Simple GUI for start/stop/test proxy and to update resolvers and maybe choose which resolver(s) to use or favour.

Could restart proxy every hour to randomize proxy.

### Toolchain

Android clang version 5.0.300080 

NDK  16.1.4479499
