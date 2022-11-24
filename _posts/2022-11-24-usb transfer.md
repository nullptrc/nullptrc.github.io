---
layout: post
title:  "USB data transfer"
date:   2022-11-24 13:28:00 +0800
categories: USB transfer
---

# USB data transfer

This article will analysis the USB data transfer in a top-down view.

## transfer type

1. control transfer

   - setup stage

     setup transition

   - data stage

     bulk transition

   - status stage

     bulk transition

2. bulk transfer

   - bulk transition

3. interrupt transfer

   - interrupt transition

4. isochronous transfer

   - isochronous transition

## transition type

1. bulk transition
2. interrupt transition
3. isochronous transition
4. setup transition

all transitions are consisted of following packets:

- one leading token packet
- several data packets
- one tailing handshake packet

## packet

A packet has several fields, listing as below:

- SOP
- SYNC
- PID(Packet ID)
- DATA(optional)
- CRC
- EOP

## Examples

![image-20221124123543185](/assets/image-20221124123543185.png)