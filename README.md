# Argus Media Pipeline Service

The Argus Media Pipeline Service manages RTMP streams between ingress and egress clients.

## Usage

install dependencies:
```
make deps 
```

NOTE: The required nginx.conf is included at the root level of this repository for reference; check or edit /etc/nginx/nginx.conf accordingly. Then:
```
make prep
```

build pipeline library binaries:
```
make build
```

After running `make prep` you'll need to open a second terminal window to continue.

run application: 
```
make run
```

stream to the service:
```
make stream
```
ingest the stream with VLC:
    1. Media > Open Network Stream 

    2. Use `rtmp://localhost/outgoing/myRestream` as the network URL