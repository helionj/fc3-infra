# Keycloak

## Import/Export

### Exporting realm with Docker

```shell
$ docker exec -u root -t -i <container_id> /bin/bash
$ /opt/keycloak/bin/kc.sh export --realm fc3-codeflix --file /tmp/codeflix-realm.json
$ docker cp <container_id>:/tmp/codeflix-realm.json ./
```

### Importing realm with Docker

```shell
$ docker exec -u root -t -i <container_id> /bin/bash
$ docker cp ./codeflix-realm.json <container_id>:/tmp
$ /opt/keycloak/bin/kc.sh import --file /tmp/codeflix-realm.json
```