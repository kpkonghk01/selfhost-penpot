# Setup log

[Ref](https://help.penpot.app/technical-guide/getting-started/)

```sh
curl -o docker-compose.yaml https://raw.githubusercontent.com/penpot/penpot/main/docker/images/docker-compose.yaml
```

setup volumes:

```yaml
  penpot_postgres_v15:
    # custom settings
    driver: local
    driver_opts:
      type: 'none'
      o: 'bind'
      device: './volumes/db'
    external: false
  penpot_assets:
    # custom settings
    driver: local
    driver_opts:
      type: 'none'
      o: 'bind'
      device: './volumes/assets'
```

```sh
docker compose up -d
```
