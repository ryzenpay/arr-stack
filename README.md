## Setup
this currently runs on me ubuntu server running rke2 with rancher  
easiest install with `treafik, longhorn and rancher/fleet` is to install the `gitops.yaml`  
ex: `kubectl apply -f gitops.yaml`  
> or paste it in through rancher UI  

### Storage
i reccomend longhorn, which is what the `manifests/storageclass.yaml` will define,  
in longhorn, attach a "media" tag to the drives you would like to store your media  
> or remove the media tag if u dont care about seperation  

## Config
i dont reccomend enabling "remove completed" from *arr download clients as they get stuck while qbittorrent begins seeding,  
to then prevent qbittorrent from taking all space, set seeding policies in tools -> options -> qbittorrent -> seeding limits  

## Lidarr
https://lidarr.audio  

## Radarr
https://radarr.video  

## Readarr
https://readarr.com  

## Sonarr
https://sonarr.tv  

## Wireguard
https://www.linuxserver.io/blog/routing-docker-host-and-container-traffic-through-wireguard  

## qBitTorrent
https://docs.linuxserver.io/images/docker-qbittorrent/  


## Networking

### QBitTorrent
if using mullvad, use the custom port for torrenting (provided in web gui when generating config)  
^ should default to 51820  

### Docker
*arr -> qbitorrent = gluetun:8080  
*arr -> *arr = localhost:<port>  

## Kubernetes
for some reason, when fleet controlling media-qbit, it just stops workign :shrug:  

# TODO
-[ ] helm chart
-[ ] qbittorrent liveness check