# Nginx Reverse Proxy

This automatically watches services and exposes them via nginx on some domain.

You can configure the domain in each service. I use PiHole as a DHCP server, assign the server a static IP address, and then use the built in DNS server to setup local domains.

# Running

`docker-compose up`