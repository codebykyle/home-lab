# Nginx Reverse Proxy

This automatically watches services and exposes them via nginx on some domain.

You can configure the domain in each service. I use PiHole as a DHCP server, assign the server a static IP address, and then use the built in DNS server to setup local domains.

# Running

`docker-compose up`

# Automatically exposing a service

In order to automatically expose a service, you must add the service to the `network-nginx-lan` network, and configure the `VIRTUAL_PORT` and `VIRTUAL_HOST` environment options

```yaml
services:
    your_service:
        environment:
            VIRTUAL_PORT: port_to_expose
            VIRTUAL_HOST: thewebsitename.lan
        networks:
            - network-nginx-lan
networks:
  network-nginx-lan:
    external:
      name: network-nginx-lan
```