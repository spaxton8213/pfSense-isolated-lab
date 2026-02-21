# pfSense-isolated-lab
pfSense-based virtual router used to simulate an isolated enterprise-style network environment supporting Windows Server 2025 and Windows 10 clients.


## Overview
This project documents the design and setup of an isolated virtual lab environment
used to safely simulate enterprise-style Windows infrastructure.

## Purpose
The lab is intentionally segmented from the physical home network using VirtualBox NAT
to reduce risk and allow safe experimentation with Windows Server and directory services.

## Architecture
- Virtual router: pfSense
- WAN interface: VirtualBox NAT (outbound connectivity without direct LAN exposure)
- LAN interface: Internal virtual network
- Systems: Windows 10, Windows Server 2022

## Subnet & Design Decisions
Although the lab is isolated from the physical network using VirtualBox NAT, the internal
addressing was intentionally subnetted as if the router were being introduced into an
existing /24 network. This was done to practice realistic subnet planning and address
allocation scenarios commonly encountered in live environments.

## Current Status
The base lab environment has been deployed and validated.
Active Directory configuration is currently in progress.
