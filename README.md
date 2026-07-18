# Homelab
```mermaid
flowchart TB

Internet((Internet))
TPLink Router[Router]
Unifi Switch[Managed Switch]

Internet --> Router
Router --> Switch

Switch --> Proxmox
Switch --> Synology

subgraph Proxmox Host
    Windows[Windows Server VM]
    Docker[Docker VM]
    Future[Kubernetes<br/>Future]
end

subgraph Synology NAS
    Media[Media Storage]
    Backup[(Future Backup Storage)]
end

Laptop[Workstation]
TV[Smart TV]
Phone[Mobile Devices]

Laptop --> SMB
TV --> Media
Phone --> Media

```
