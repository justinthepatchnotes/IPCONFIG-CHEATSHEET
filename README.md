# ipconfig Cheatsheet

`ipconfig` is a command used in Windows to display and manage network settings.  

## Basic Usage  
- `ipconfig` – Displays the current IP configuration of a Windows machine.  
- Used for troubleshooting connectivity issues.  

![ipconfig](https://i.imgur.com/OgV5SME.png)

## ipconfig Commands Cheat Sheet  

| Command                  | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| `ipconfig /all`          | Displays detailed information for all network adapters, including MAC addresses, DHCP, and DNS settings. |
| `ipconfig /release`      | Releases the current IP address assigned by DHCP.                           |
| `ipconfig /renew`        | Requests a new IP address from the DHCP server. Useful for fixing connectivity issues. |
| `ipconfig /flushdns`     | Clears the DNS resolver cache. Helps resolve domain name resolution problems. |
| ![ipconfig /flushdns](https://i.imgur.com/UCbdijW.png) | |
| `ipconfig /displaydns`   | Displays the current DNS cache entries.                                      |
| ![ipconfig /displaydns](https://i.imgur.com/45f8nT6.png) | |
| `ipconfig /registerdns`  | Refreshes DNS registration and renews DHCP leases. Helps in domain environments. |



## Key Outputs of `ipconfig`  

- **IPv4 Address** - The primary address used for most network communication (e.g., `192.168.1.10`).  
- **Subnet Mask** - Defines the network portion of the IP address (`255.255.255.0` for most home networks).  
- **Default Gateway** - The router's IP address, which directs traffic outside the local network (e.g., `192.168.1.1`).  
- **IPv6 Address** - A newer protocol designed to replace IPv4, but still not widely used in most home and corporate networks.  

## IPv4 vs. IPv6 - What's Important?  

- **IPv4** (e.g., `192.168.1.10`) is still dominant in most networks.  
- **IPv6** (e.g., `fe80::1`) is future-proof but not crucial to memorize for basic IT roles.  
- **Subnet Mask** helps define network boundaries.  
- **Default Gateway** is essential for external network communication.  

## When to Use `ipconfig` in a Job?  

### No Internet Access?  
- Run `ipconfig /all` to check if you have a valid IP address.  
- If the IP starts with `169.254.x.x`, it means your device failed to get an IP from DHCP.  
- Use `ipconfig /release` and `ipconfig /renew` to request a new one.  

### Can’t Access a Website, but Others Work?  
- Run `ipconfig /flushdns` to clear outdated DNS records.  
