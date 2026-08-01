---
title: Azure VPN Gateway
tags: [azure, azure-developer-associate, cloud, networking]
up: "[[azure]]"
---

# Azure VPN Gateway

## What is Azure VPN Gateway?
Azure VPN Gateway is specific type of virtual network gateway that sends encrypted traffic between your Azure virtual network and on-premises locations over the public internet. It enables hybrid connectivity between your cloud and on-premises infrastructure.

## Key Components
The VPN Gateway consists of two or more VMs deployed in a special subnet called the Gateway Subnet. These VMs contain routing tables and specific gateway services, though you cannot direcly configure or access these VMs.

## Gateway types
- VPN: To send encrypted traffic across the public internet.
- ExpressRoute: To send network traffic on a private connection. Is designed to exchange network routes and network traffic. Designed to improve performance between your on-premises network and your virtual network. It sends network traffic directly to virtual machines in the virtual network, bypassing the gateway.
## Types of VPN Connections
### Site to Site  (S2S)
- Connects your on-premises network to Azure via VPN tunnel
- Requires a VPN device or Window Server running RRAS on premises
- Good for hybrid scenarios where you need persistent connectivity
### Point to site (P2S)
- Connects individual client computers to your Azure virtual network
- Uses certificates or Azure Active Directory for authentication
- Ideal for remote workers or when you have few clients to connect
### VNet to VNet
- Connects Azure virtual networks to each other 
- Works across different regions and subscriptions
- Similar to S2S but entirely within Azure
- It requires a public IP address on both ends of the connection.
## Gateway SKUs and Performance
- Basic: Up to 100 Mbps, 10 S2S connections
- VpnGwl 1/2/3: Higgher throughput and more connections
- Higher SKUs support BGP (Border Gateway Protocol) routing protocol, BGP cannot be used with both policy-based and route-based VPN gateways, BGP can only be used with route-based VPN gateways

- Azure allows you to deploy your own VPN gateways or servers in Azure, either from the Azure Marketplace or by creating your own VPN routers.
- After you set yp your own VPN gateways or servers, you must configure user-defined routes in the virtual network to ensure that traffic is routed properly between the on-premises networks and the virtual network subnets.
- Azure generates different IPsec/IKE pre-shared keys to different VPN connections created for the same virtual network. This is done by default. However, you can use PowerShell cmdlets or the set VPN Gateway REST API to configure a custom key value.
- Azure VPN gateways support 16-bit ASNs.

## Related

- [[azure-migrate]] — hybrid connectivity is usually a migration prerequisite.
- [[azure-blueprint]] — vnet and gateway creation as an ARM template artifact.
- [[azure-monitor]] — gateway metrics and diagnostics.
