# Docker PowerDNS
This repository contains a Docker container for running the PowerDNS Authorative nameserver.

It is based on Ubuntu 16.04 and uses the static release from [downloads.powerdns.com](https://downloads.powerdns.com/releases/) and uses GPG to verify the signature of PowerDNS.

## Running
PowerDNS will look for */etc/powerdns/pdns.conf* and use it as the configuration. Using a mapping you can override this file and change the PowerDNS configuration:


    docker run -v /home/user/pdns.conf:/etc/powerdns/pdns.conf pdns


*NOTE:* By default there are NO backends configured. You will have to configure the [backends](https://docs.powerdns.com/md/authoritative/#backends) manually in the *pdns.conf* configuration file.

## License

The MIT License (MIT). Please see [License File](LICENSE) for more information.
