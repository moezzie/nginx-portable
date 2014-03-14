nginx-portable
==============

nginx-portable is a portable version of the nginx web server for linux.  
At this point in time the package only contains nginx-1.4.6, so no fastcgi and mysql just yet.

#### About nginx

> nginx [engine x] is an HTTP and reverse proxy server, as well as a mail proxy server, written by Igor Sysoev  

You can read all about it on the [nginx website](http://nginx.org/en/)  

## Goals
What did i have in min when working on this project
* A standalone, pre-configured, portable, stable version of the nginx web server for linux
* Easily distributable package together with or as base for other products

## Dependencies
On Ubuntu installing the following packages should provide all the files necessary to build nginx
`sudo apt-get install build-essential libpcre3-dev libssl-dev`

## Getting started
1. Clone this repository
2. To compile a binary for your architecture issue `./compile`.
3. Run `sudo ./nginx-portable start` to start the server
4. Fire up your favorite browser and go to `http://localhost:8080`
Voila!

Congratulations, your nginx server is up and running.  
Now go on and add your own files to the `html` directory.

## Usage

#### The init script
The init script works pretty much exactly like nginx init.d script on Ubuntu.
```Usage: ./nginx-portable {start|stop|restart|reload}```

#### Configuration
If you need to change any of the default values you can find `nginx.conf` under
`conf/nginx.conf` in the nginx-portable directory.

Additional modules and flags can be added to/removed from the appropriate line in the `compile` file.

## Known issues
* This package has only been tested on Ubuntu Server 12.04 LTS 32bit and Ubuntu Server 13.10 64bit.
* The compile script currently does not work correctly under Mac OSX. You can get it to run by hardcoding the scripts absolute path to `BASEDIR` in the compile script.

If your find any bugs or have suggestions on how to improve nginx-portable, feel free to write up an issue here on GitHub or fork the repo to tinker with it yourself.

## Boring legal stuff

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.
