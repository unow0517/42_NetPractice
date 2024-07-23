# 42_NetPractice
To learn about IP, Network 

## IP Address
IP is like an adress in internet world. Each device has their unique ID

## IPv4, IPv6
Two different protocol for IP address. IPv4 is 32bit, IPv6 is 128bit.

## How an IP is composed
`192.168.0.1` = `1100 0000.1010 1000.0000 0000.0000 0001`

**Octet** = a piece of number which is seperated by dots. Could range from 0 to 255.

## Subnet
With subnet masks, some devices are limited as to which other devices they can communicate with.  In cases where the IP addresses are not compatible based on the subnet masks, those devices are not allowed to communicate with each other.

A subnet mask of `255.255.255.0` means that the device can connect with any other device on the network with an IP address containing identical values in the first three octets. 

Devices in Local Network have identical subnet mask.

`/30` = `1111 1111.1111 1111.1111 1111.1111 1100` = `255.255.255.252`
 
## Reference
* https://medium.com/@su_bak/%EC%84%9C%EB%B8%8C%EB%84%B7-%EB%A7%88%EC%8A%A4%ED%81%AC-subnet-mask-%EB%9E%80-398ecdfd5c0d
* https://techdebt.tistory.com/34
* https://www.kollmorgen.com/en-us/developer-network/what-subnet-mask
