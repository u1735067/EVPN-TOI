Labs for Arista ATD
-------------------

These labs have been built for the setup used in Arista Test Drive composed of the following device:
- 2 Spine Switches
    - Spine1
    - Spine2
- 4 Leaf Switches
    - Leaf1
    - Leaf2
    - Leaf3
    - Leaf4
- 2 Hosts
    - Host1
    - Host2

![Lab Diagram](diagram.jpg)

The order of the labs is the following:
- [OSPF](1-OSPF): to configure the underlay
- [iBGP](2-iBGP): to configure the overlay
- [Services](3-Services): to exend a VLAN over the EVPN Fabric
- [RTC](4-RTC): to configure Route-Target Constraint
- [PVLAN](5-PVLAN): to configure a PVLAN domain over an EVPN VXLAN Fabric
- [L2 EVPN GW](6-L2&#32;EVPN&#32;GW) GW: to configure EVPN GWs and extend VLANs in a EVPN multi-domain
- [L3 EVPN GW](7-L3&#32;EVPN&#32;GW): to configure EVPN GWs and extend a VRF in a EVPN multi-domain
- [EVPN Filtering](8-EVPN&#32;Filtering): to filter and optimize EVPN routes
- [Maintenance Mode](9-Maintenance&#32;Mode): to test maitenance mode

Note that the labs need to be completed in the order described above as the configuration are merged from one exercice to another.
When you start the Arista ATD, do not choose any proposed Lab. Start with the basic configuration of the devices.

See below the main IP addresses used for the devices.

| Interfaces    | Spine1    | Spine2   | Leaf1      | Leaf2       | Leaf3       | Leaf4       | Remote Leaf (Host1) |
| -----------   | ----------| ---------| -----------| ----------- | ----------- | ----------- | ----------- |
| Loopback0     | 10.0.0.1  | 10.0.0.2 | 10.0.0.11  | 10.0.0.12   | 10.0.0.13   | 10.0.0.14   | 10.0.0.21   |
| Loopback1     | NA        | NA       | 10.0.1.11  | 10.0.1.11   | 10.0.1.13   | 10.0.1.13   | 10.0.1.21   |
| Loopback2     | 10.0.2.1  | 10.0.2.2 | 10.0.2.11  | 10.0.2.12   | 10.0.2.13   | 10.0.2.14   | NA          |
| MLAG (V4094)  | NA        | NA       | 169.254.0.1| 169.254.0.2 | 169.254.0.1 | 169.254.0.2 | NA          |
| MLAG Domain  | NA        | NA       | 12 | 12 | 34 | 34 | NA |