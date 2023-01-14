---
id: 79gsse589fc1zxffxa9zesc
title: Parts of an Ip Address in Detail
desc: ''
updated: 1673712560412
created: 1673421974010
---

 

-   A Subnet mask is a 32-bit number that masks an IP address.

-   Also divides the IP address into network address and host address.

>  
>
> ![Eg: 1101 1000 · 0000 0011 · 1000 0000 · 0000 1100 Mask: 1111 1111 · 1111 1111 · 1111 1111 · 00000000 NW: 1101 1000 · 0000 0011 · 1000 0000 · 0000 0000 IP Subnet Mask Network Part 216 · 3 · 128 · 12 255 · 255 · 255 · 0 Host Part ( 216 · 3 · 128 · 12 ) ( 255 · 255 · 255 · 0 ) ( 216 · 3 · 128 · 0 ) ](021_Subnet_Mask_000.png){width="4.291666666666667in" height="1.7291666666666667in"}

 

 

-   Broadcast address is the last host address

    -   Broadcast Address - 11111111


-   Network address is the first host address

    -   Network Address - 00000000

-   Calculate the amount of host on a network

    -   2\^n
