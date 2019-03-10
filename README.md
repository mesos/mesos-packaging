# Apache Mesos Packaging

Build scripts to create Apache Mesos packages with [FPM](https://github.com/jordansissel/fpm) for simple installation in a cluster.

Apache Mesos is a cluster manager that provides efficient resource isolation and sharing across distributed applications, or frameworks. It can run Hadoop, MPI, Hypertable, Spark (a new framework for low-latency interactive and iterative jobs), and other applications. Currently is in the Apache Incubator and going through rapid development, though stable enough for a production usage. See [Mesos website](http://incubator.apache.org/mesos/) for more details.

## Packaging Requirements

```bash
sudo apt-get install ruby ruby-dev python-dev autoconf automake git make libssl-dev libcurl3 libtool
sudo gem install fpm
```

## Mesos Requirements

Mesos has its own OS-level build requirements that need to be installed as well before building.

See [getting-started](https://mesos.apache.org/getting-started/) for more information.


## Setting the Maintainer

define in e.g. `~/.bash_profile` a `MAINTAINER` variable

```bash
export MAINTAINER="email@example.com"
```

## Setting `make` Options (optional)

```bash
export MAKEFLAGS=-j8
```

## Building deb or rpm Package

```bash
./build_mesos
```

## TODO

   * automatic restart of master/slave when upgrading
   * logrotate support
   * service autostart

## Authors

   * Tomas Barton
   * Srdjan Grubor <sgnn7@sgnn7.org>
