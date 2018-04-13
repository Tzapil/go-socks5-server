# go-socks5-proxy

Simple socks5 server using go-socks5 with auth

# Start container with proxy
```docker run -d --name socks5-proxy -p 1080:1080 -e PROXY_USER=<PROXY_USER> -e PROXY_PASSWORD=<PROXY_PASSWORD> serjs/go-socks5-proxy```

where

```<PROXY_USER>``` - username to authenticate

```<PROXY_PASSWORD>``` - password to authenticate

# Test running service
```curl --socks5 <docker machine ip>:1080 -U <PROXY_USER>:<PROXY_PASSWORD> https://ifcfg.me``` - result must show docker host ip (for bridged network)