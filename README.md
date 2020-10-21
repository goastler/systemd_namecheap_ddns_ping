# systemd_namecheap_ddns_ping

Systemd service and timer for pinging namecheap to update ddns records.

## Setup

- Anywhere you see my.domain.name should be replaced with your domain name.
- Likewise, my-password should be replaced with your ddns password (note this is NOT your account password, you can find the ddns password under the domain management tab).
- Rename the service and timer to something more meaningful for you (I usually use the domain name, i.e. www.example.com.service and www.example.com.timer). Make sure both are named the same apart from file extension.
- Copy both files into /etc/system/systemd
- Enable and start the timer, which will trigger the service as required
  - `systemctl enable <whatever you called your file>.timer`
  - `systemctl start <whatever you called your file>.timer`
