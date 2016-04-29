# Docker PowerDNS
This repository contains a Docker container for running the PowerDNS Authorative
nameserver.

It is based on Ubuntu 16.04 and uses the static release from [downloads.powerdns.com](https://downloads.powerdns.com/releases/)
and uses GPG to verify the signature of PowerDNS.

# Running
PowerDNS will look for */etc/powerdns/pdns.conf* and use it as the configuration. Using a mapping you can override this file and
change the PowerDNS configuration:

<pre>docker run -v /home/user/pdns.conf:/etc/powerdns/pdns.conf pdns</pre>

