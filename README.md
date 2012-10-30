nginx-portable
==============

nginx-portable is a portable version of the nginx web server for linux.  
At this point in time the package only contains nginx-1.2.4, so no fastcgi and mysql just yet.

#### About nginx

> nginx [engine x] is an HTTP and reverse proxy server, as well as a mail proxy server, written by Igor Sysoev  

You can read all about it on the [nginx website](http://nginx.org/en/)  

## Goals
What did i have in min when working on this project
* A standalone, pre-configured, portable, stable version of the nginx web server for linux
* Easily shipable together with or as base for other products

## Getting started
1. Clone this repository
2. Run `cd nginx-portable` and then `sudo ./nginx start`
3. Fire up your favorite browser and go to `http://localhost:8080`

Congratulations, your nginx server is up and running.  
Now go on and add your own files to the `html` directory.

## Usage

#### The init script
The init script works pretty much exactly like nginx init.d script on Ubuntu. In fact, it is a modified version of that file.
```Usage: ./nginx {start|stop|status|restart|reload|force-reload|upgrade|configtest}```

#### Configuration
If you need to change any of the default settings you can find `nginx.conf` under
`usr/local/nginx/conf/` in the nginx-portable directory.

## Known issues
* This package has only been tested on the 32bit server version of Ubuntu 12.04.

If your find any bugs or have suggestions on how to improve nginx-portable, feel free to write up an issue here on GitHub or fork the repo to tinker with it yourself.

## Boring legal stuff

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.