# 3proxy
Dockerized 3proxy. (HTTP, SOCKS)

3proxy is tiny  proxy server.

This repo is modified based on [rb-dock8s/3proxy](https://github.com/rb-dock8s/3proxy).

Add little changed for customized port.

## Environment variables

|Env| Description | Default |
|:-:|:-:| :-: |
| ADMIN | The port of configuration page | 8080 |
| HTTP | The port of http proxy | 3128 |
| SOCKS | The port of socks proxy | 1080 |
| PROXY_LOGIN | The username of proxy auth. (required) | N/A |
| PROXY_PASSWORD | The password of proxy auth. (required) | N/A |
| PROXY_VERSION | The version of 3proxy | 0.8.13 |

## Example usage
```sh
$ docker run --name 3proxy -d -p 8088:8088 --env SOCKS="8088" --env PROXY_LOGIN="123456" --env PROXY_PASSWORD="123456" aquamars00/3proxy

$ curl --socks5 123456:123456@localhost:8088 ifconfig.co

```