# The Docker Image of [xtaci/kcptun](https://github.com/xtaci/kcptun) for ARM Architecture

## Usage

### Server

```
docker run -d \
--name kcp-server \
-p 29900:29900/udp \
posoo/kcptun \
/kcptun/server_linux_arm<VERSION> -l :29900 -t ss-server:8080 -mode fast -crypt none -nocomp -dscp 46
```

The `<VERSION>` value can be 5, 6 or 7.

### Client

```
docker run -d \
--name kcp-client \
p- 12948:12948 \
posoo/kcptun \
/kcptun/client_linux_arm<VERSION> -l :12948 -r [kcp-server]:191 -mode fast -crypt none -nocomp -dscp 46
```

The `<VERSION>` value can be 5, 6 or 7.

