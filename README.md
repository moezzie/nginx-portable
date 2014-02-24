LEMPO - Portable Linux Web-Server
==============

lempo is a portable version of the nginx, mysql, php for linux.  

#### About nginx

> nginx [engine x] is an HTTP and reverse proxy server, as well as a mail proxy server, written by Igor Sysoev  

You can read all about it on the [nginx website](http://nginx.org/)  

## Features
* A standalone, pre-configured, portable web server for linux
* Easily distributable package together with or as base for other products

## Getting started
1. [Download lempo](https://github.com/agmanix/lempo/archive/master.zip)
2. To compile a binary for your architecture issue `./compile`.
3. Run `sudo ./server start` to start the server
4. Fire up your favorite browser and go to `http://localhost:8080`
Voila!

Congratulations, your nginx server is up and running.  
Now go on and add your own files to the `nginx/html` directory.

## Usage

#### The init script
The init script works pretty much exactly like init.d script on Ubuntu.
```Usage: ./server {start|stop|restart|reload}```

#### Configuration
If you need to change any of the default values you can find `nginx.conf` under
`nginx/conf/nginx.conf` in the lempo directory.

Additional modules and flags can be added to/removed from the appropriate line in the `compile` file.

## Known issues
* This package has only been tested on the 32bit version of Ubuntu 12.x/13.x.
* The compile script currently does not work correctly under Mac OSX. You can get it to run by hardcoding the scripts absolute path to `BASEDIR` in the compile script.

If your find any bugs or have suggestions on how to improve lempo, feel free to write up an issue here on GitHub or fork the repo to tinker with it yourself.

## History
### Version 0.1
* Updated nginx version to 1.5.10
* Added nginx dependencies to compile script (now it's really portable!) - openSSL, PCRE, zLib

### Version 0.0
* Forked from [moezzie/nginx-portable](https://github.com/moezzie/nginx-portable) 
