# Home Lab

These are various services running on my primary home lab server setup in my office.

## Management Script
There is a small management script for quickly turning on and off services and getting things setup. 

Make the management script executable:

`chmod +x manage`

Help Pages:

`./manage`

`./manage services`

`./manage networks`

Start all services and networks:

`./manage up`

Stop all services and networks:

`./manage down`

Recreate all services and networks:

`./manage restart`
