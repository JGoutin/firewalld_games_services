# Firewalld games services

These services can be used to easily allow access to some multiplayer games on 
Linux systems that use Firewalld as firewall (Like Fedora, CentOS, ...).

This is suitable for workstations running games, or dedicated game servers.

## Games

Services are provided for the games listed below.

If a dedicated server is freely available, a link is provided. Games always run in their Linux version if it exists; otherwise, this is specified.

* Eco ([Setting up server](https://wiki.play.eco/en/Setting_Up_a_Server))
* Empire Earth[^win]
* Enshrouded ([Setting up server](https://enshrouded.zendesk.com/hc/en-us/articles/16056312924957-Dedicated-Server-FAQ))
* Factorio ([Dedicated headless Linux amd64 server download](https://factorio.com/get-download/latest/headless/linux64)).
* Minecraft Java Edition (Dedicated server can be downloaded from [here](https://www.minecraft.net/en-us/download/server))
* Project Zomboid ([Setting up server](https://pzwiki.net/wiki/Dedicated_server))
* Stellaris
* Streets of Rogue
* Terraria (Dedicated server can be downloaded from [here](https://www.terraria.org/))
* Vintage Story (Dedicated server available on client download page)

[^win]: Windows version running with [Wine](https://www.winehq.org/).

## Usage

To install a service, copy its XML file into `/etc/firewalld/services` 
(or `/usr/lib/firewalld/services`).
 
To enable a service, run the following commands 
(`SERVICE` needs to be replaced by the service name):
```bash
sudo firewall-cmd --add-service=SERVICE --permanent
sudo firewall-cmd --reload
```
 
To disable a service, run the following commands:
```bash
sudo firewall-cmd --remove-service=SERVICE --permanent
sudo firewall-cmd --reload
```

To uninstall the service, simply delete the XML file.
