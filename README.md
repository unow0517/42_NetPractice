# 42_NetPractice
To learn about IP, Network 

## IP Address
IP is like an adress in internet world. Each device has their unique ID

## IPv4, IPv6
Two different protocol for IP address. IPv4 is 32bit, IPv6 is 128bit.

## How an IP is composed
`192.168.0.1` = `1100 0000.1010 1000.0000 0000.0000 0001`

**Octet** = a piece of number which is seperated by dots. Could range from 0 to 255.

## Subnet Mask
With subnet masks, some devices are limited as to which other devices they can communicate with.  In cases where the IP addresses are not compatible based on the subnet masks, those devices are not allowed to communicate with each other.

A subnet mask of `255.255.255.0` means that the device can connect with any other device on the network with an IP address containing identical values in the first three octets. 

Devices in Local Network have identical subnet mask.

`/30` = `1111 1111.1111 1111.1111 1111.1111 1100` = `255.255.255.252`

For example, when IP address is `102.4.31.57` and Subnet Mask is `255.255.255.0` then Network address is `102.4.31.0`, Host address is `0.0.0.57`.

*Network address = address of the network, which is composed of hosts.
*Host address* = Address of end device, terminal (I am not sure if these terms are exactly identical to each other, but I understood like this).

If you execute Bitwise AND IP address and Subnet Mask, then you can get network address
## Some Special Addresses
`127.0.0.0`~`127.255.255.255` indicates the device itself, so it cannot be used in local network.

`192.168.0.0`~`192.168.255.255` : private IP address and it is not used on the Internet.

`172.16.0.0`~`172.31.255.255` : in the private range, but routable.

`10.0.0.0`~`10.255.255.255` : private IP address

## Good to know for the examples
`192` = `1100 0000`

`224` = `1110 0000`

Mask `255.255.255.224 (1111 1111.1111 1111.1111 1111.1110 0000)` means that, first 27 digits of addresses in this subnet should be identical. Details in https://www.kollmorgen.com/en-us/developer-network/what-subnet-mask

## Question about the examples
Level 2 : why A1 cannot have `192.168.77.192`? -> From Bitwise AND, network address is 192.168.77.192. The broadcast address is 192.168.77.223. 

broadcast address = convert 224 `1110 0000` = 31 `0001 1111`, then `192.168.223(192 + 31)` is the broadcast address. 


## Reference
* https://medium.com/@su_bak/%EC%84%9C%EB%B8%8C%EB%84%B7-%EB%A7%88%EC%8A%A4%ED%81%AC-subnet-mask-%EB%9E%80-398ecdfd5c0d
* https://techdebt.tistory.com/34
* https://www.kollmorgen.com/en-us/developer-network/what-subnet-mask
