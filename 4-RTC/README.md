# LAB: Route-Target Constraints

## About

Goal of this lab: Configure RTC

## Configure RTC Sessions

Spine1 and Spine2 need to receive all routes

Leaf1-4 only need to receive the "interesting" routes

## Check the iBGP EVPN Sessions

```cli

show bgp neighbors

show bgp rt-membership summary

show bgp rt-membership

show bgp rt-membership floodlist

show bgp rt-membership floodlist 112:112

```

Note that if you have the time you can configure additional Layer 2 services and reissue the commands above.