## JellySeer
OIDC redirect url: https://seer.media.ryzen.me/login?provider=keycloak&callback=true

## Jellyfin
### Menu Links
```
sed -i 's#"menuLinks": \[\]#"menuLinks": [\
    {\
      "name": "Request",\
      "url": "https://seer.media.ryzen.me"\
    }\
  ]#' config.json
```

## Arr Auth
redirect url:
- http://sonarr.media.ryzen.me/_oauth
- http://radarr.media.ryzen.me/_oauth
- http://lidarr.media.ryzen.me/_oauth
- http://readarr.media.ryzen.me/_oauth
- http://bazarr.media.ryzen.me/_oauth
- http://prowlarr.media.ryzen.me/_oauth
ensure you disable "local authentication required" in *arr