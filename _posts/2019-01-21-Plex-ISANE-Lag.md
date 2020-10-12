---
layout: post
title:  "Plex ISANE Lag"
date:   2019-01-21 22:07:01 -0600
categories: plex ubuntu network lag
---
#2 Posibilities Network or DTS


Either the problem was caused by some files with DTS being unable to load(Didn't seem that way since some of the files didn't have DTS), or a networking issue (Large Send  Offload{LSO}).

Select Advanced tab. You will get a list filled with different options.
Select Large Send Offload V2 (IPv4) and set the value to Disabled
Do the same for Large Send Offload V2 (IPv6) if it is available





https://forums.plex.tv/t/massive-buffering-solved/155491/6