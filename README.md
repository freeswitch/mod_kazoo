# mod_kazoo

Socket Controlled Event Handler module for FreeSWITCH

## Table of Contents

* [Table of Contents](#table-of-contents)
* [Build and install mod_kazoo](#build-and-install-mod_kazoo)

## Build and install mod_kazoo

Make sure you have `erlang-dev` package installed.

Change to a directory where the FreeSWITCH sources will be compiled

```
cd /usr/src
```

Clone the FreeSWITCH repository into the above directory

```
git clone https://github.com/signalwire/freeswitch.git
```

Perform an initial bootstrap of FreeSWITCH so that a `modules.conf` file is created

```
./bootstrap.sh
```

Add the mod_kazoo to `modules.conf` so that an out-of-source build will be performed

```
mod_kazoo|https://github.com/freeswitch/mod_kazoo.git -b master
```

Configure, build and install FreeSWITCH

```
./configure
make
make install
```

The following commands will build and install *only* mod_kazoo

```
make mod_kazoo
make mod_kazoo-install
```