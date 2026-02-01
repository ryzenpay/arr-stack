# *arr-stack
Complete arr stack including:
- lidarr
- sonarr
- radarr
- bazarr
- prowlarr
- scraparr (optional) (kube)
- doplarr (optional) (kube)

## Installation

### Kubernetes
use the helm chart found at: `oci://harbor.ryzen.me/library/arr-stack` (ref in `/manifests/helmchart.yaml`)  
check out the values in `/charts/arr-stack/values.yaml`  

if using fleet, look at my example `/helmop.yaml`  

### Storage
i reccomend longhorn, which is what the `/manifests/storageclass.yaml` will define,  
in longhorn, attach a "media" tag to the drives you would like to store your media  
> or remove the media tag if u dont care about seperation  

### Docker Compose
1. copy `.env.example` to `.env`
2. fill in the values in `.env`
3. `docker compose up -d`

## Config
i dont recommend enabling "remove completed" from *arr download clients as they get stuck while qbittorrent begins seeding,  
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

> if using mullvad, use the custom port for torrenting (provided in web gui when generating config)  
> ^ should default to 51820  

## Prowlarr
https://prowlarr.com/

## Scraparr
https://github.com/thecfu/scraparr

## Doplarr
https://github.com/kiranshila/Doplarr

# TODO
-[x] helm chart  
-[ ] qbittorrent liveness check  
-[ ] configarr (https://configarr.de)  
-[x] scraparr (https://github.com/imgios/scraparr)  
-[ ] helm chart values documentation