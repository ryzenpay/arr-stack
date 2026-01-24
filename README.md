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