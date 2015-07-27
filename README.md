maxscale-docker
===============

This project is a Docker container for MariaDB MaxScale.

Base [docker image](http://www.docker.io) to run [MaxScale](https://mariadb.com/products/mariadb-maxscale).

    MariaDB MaxScale is an open-source, database-centric proxy that works with MariaDB Enterprise, MariaDB Enterprise Cluster, MariaDB 5.5, MariaDB 10 and Oracle MySQL®.
    It’s pluggable architecture is designed to increase flexibility and aid customization. Built upon a lightweight, high-speed networking core designed to facilitate throughput.
    MariaDB MaxScale runs between the client application and the database cluster offering connection and statement-based load balancing.
    MariaDB MaxScale allows scaling of an organization's database infrastructure while keeping the needs of DBAs, Developers and Data Architects in mind.

## Getting the container

The container can be pulled from the [Docker Hub](https://registry.hub.docker.com/u/dnshosting/maxscale/)
running

    docker pull dnshosting/maxscale

## Using the container

Run a single instance of MaxScale

    docker run -d dnshosting/maxscale

The default MaxScale configuration file can be replaced by a custom file
present into the host filesystem using a docker volume.
In e.g.

    docker run -d -v `pwd`/my-maxscale.cnf:/etc/maxscale.cnf dnshosting/maxscale

## Build the container

To create the image `dnshosting/maxscale`, execute the following command into
the `maxscale-docker` project root directory

    docker build -t dnshosting/maxscale .

## Thanks

* [MariaDB MaxScale](https://github.com/mariadb-corporation/MaxScale) - for giving us such an incredible tool
* [@MassimilianoPinto](https://github.com/MassimilianoPinto) - for his collaboration

## Contribute

Contributions are welcome.

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## License

Copyright 2015 Colt Engine S.r.l.
Licensed under the MIT License
