# DHCP Lab 3 – DHCP Relay

## Objective

Configure a DHCP server to provide IP addresses to clients on two different networks using DHCP relay.

## Network Topology

- 1 Router
- 2 Switches
- 10 Client Devices
  - 8 PCs
  - 2 Laptops
- 1 DHCP Server

## Network Configuration

### Sales Network

- Network: `192.168.10.0/24`
- Default Gateway: `192.168.10.1`
- DHCP Server: `192.168.10.2`
- DHCP Range: `192.168.10.100 – 192.168.10.149`

### IT Network

- Network: `192.168.20.0/24`
- Default Gateway: `192.168.20.1`
- DHCP Range: `192.168.20.100 – 192.168.20.149`

## DHCP Relay Configuration

The router was configured to forward DHCP requests from the IT network to the DHCP server:

`ip helper-address 192.168.10.2`

## Testing and Verification

- Sales clients successfully received IP addresses through DHCP.
- IT clients successfully received IP addresses through DHCP relay.
- IT clients received addresses from the `192.168.20.0/24` network.
- Clients successfully reached their default gateway.
- Clients successfully communicated with the DHCP server.
- Connectivity was verified using ping.

## Skills Demonstrated

- DHCP configuration
- Multiple IP networks
- DHCP scopes
- DHCP relay
- IP addressing
- Default gateways
- Router interface configuration
- Network connectivity testing
- Basic Cisco IOS CLI
- Network troubleshooting

## Tools Used

- Cisco Packet Tracer
- Cisco IOS

## Result

Successfully configured and verified DHCP services across two different networks using DHCP relay.
