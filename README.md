safematix/docker-owncloud
=======

[![Automated Build](http://img.shields.io/badge/automated-build-green.svg)](https://hub.docker.com/r/safematix/owncloud)
[![GPLv3 Licensed](http://img.shields.io/badge/license-GPLv3-green.svg)](https://tldrlegal.com/license/gnu-general-public-license-v3-(gpl-3))

### Usage

To run it:

    $ docker run --detach --restart always --name owncloud -publish 80:80 -publish 443:443 --link mariadb:mysql --volume /srv/owncloud/data:/var/www/html/data --volume /srv/owncloud/config:/var/www/html/config safematix/owncloud

Then start any containers you want proxied with an redis link

    $ docker run -d --name owncloud -publish 80:80 -publish 443:443 --link mariadb:mysql --link redis:redis --volume /srv/owncloud/data:/var/www/html/data --volume /srv/owncloud/config:/var/www/html/config safematix/owncloud

## License

This repo is released under the GPLv3 License. See the bundled LICENSE file for details.
